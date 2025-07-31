---
title: About This Preset
nav_order: 1
parent: Sections
---

{% include_relative ../_includes/slice.md %}
{% include_relative ../README.md %}
{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: About This Preset start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: About This Preset end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for About This Preset -->
{% endif %}