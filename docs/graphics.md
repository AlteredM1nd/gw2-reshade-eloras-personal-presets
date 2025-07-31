---
title: In-Game Graphics Settings (Recommended)
nav_order: 5
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: In-Game Graphics Settings (Recommended) start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: In-Game Graphics Settings (Recommended) end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for In-Game Graphics Settings (Recommended) -->
{% endif %}