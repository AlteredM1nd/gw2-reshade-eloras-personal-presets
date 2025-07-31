---
title: Hardware Recommendations & Performance
nav_order: 7
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: Hardware Recommendations & Performance start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: Hardware Recommendations & Performance end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for Hardware Recommendations & Performance -->
{% endif %}