---
title: License
nav_order: 9
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: License start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: License end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for License -->
{% endif %}