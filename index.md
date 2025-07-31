---
title: Home
nav_order: 0
layout: default
has_children: true
---

{% capture readme_content %}
{% include_relative README.md %}
{% endcapture %}

{%- comment -%}
Disable auto ToC on the homepage by stripping any generated ToC markup.
Just the Docs can auto-generate a ToC based on headings; this removes a leading ToC block if present.
{%- endcomment -%}
{%- assign rendered = readme_content | markdownify -%}
{%- assign rendered_no_toc = rendered
  | replace: '<nav class="toc">','<nav class="toc" hidden>'
  | replace: '<div class="toc">','<div class="toc" hidden>'
  | replace: '<h2 id="table-of-contents">Table of contents</h2>',''
-%}
{{ rendered_no_toc }}