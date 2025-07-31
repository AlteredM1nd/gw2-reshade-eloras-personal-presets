---
title: Home
nav_order: 0
layout: default
has_children: true
has_toc: false
---

{% capture readme_content %}
{% include_relative README.md %}
{% endcapture %}

{%- comment -%}
Strip any auto-inserted ToC block that may appear at the end of the rendered README content.
We remove the ToC heading and the entire following list/block via regex, and also hide any toc containers.
{%- endcomment -%}
{%- assign rendered = readme_content | markdownify -%}
{%- assign without_heading = rendered
  | replace_regex: '(?is)<h2[^>]*>\\s*Table of contents\\s*</h2>\\s*(<ul[\\s\\S]*?</ul>|<ol[\\s\\S]*?</ol>|<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>)',''
-%}
{%- assign without_containers = without_heading
  | replace_regex: '(?is)<nav[^>]*class="toc"[^>]*>[\\s\\S]*?</nav>',''
  | replace_regex: '(?is)<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>',''
-%}
{{ without_containers }}