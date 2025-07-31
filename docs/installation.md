---
title: Installation Instructions
nav_order: 4
parent: Sections
---

{% capture __slice_raw %}{% include_relative README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: Installation Instructions start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: Installation Instructions end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for Installation Instructions -->
{% endif %}