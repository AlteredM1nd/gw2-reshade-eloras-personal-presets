---
title: Required Effect Packages/Add-ons
nav_order: 3
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: Required Effect Packages/Add-ons start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: Required Effect Packages/Add-ons end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for Required Effect Packages/Add-ons -->
{% endif %}