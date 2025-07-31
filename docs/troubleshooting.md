---
title: Troubleshooting & FAQ
nav_order: 8
parent: Sections
---

{% capture __slice_raw %}{% include_relative ../README.md %}{% endcapture %}
{% assign __parts = __slice_raw | split: "<!-- SLICE: Troubleshooting & FAQ start -->" %}
{% if __parts.size > 1 %}
{% assign __after = __parts[1] %}
{% assign __seg = __after | split: "<!-- SLICE: Troubleshooting & FAQ end -->" | first %}
{{ __seg | markdownify }}
{% else %}
<!-- slice: start marker not found for Troubleshooting & FAQ -->
{% endif %}