---
title: FOV & Camera Tips
nav_order: 6
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: FOV & Camera Tips start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: FOV & Camera Tips end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for FOV & Camera Tips -->
{% endif %}