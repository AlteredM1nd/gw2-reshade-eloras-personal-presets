---
title: Home
nav_order: 0
layout: default
has_children: true
has_toc: false
---

{%- comment -%}
Step 1: Capture the raw content of README.md and the HTML for the preview grid.
{%- endcomment -%}
{% capture readme_raw %}
{% include_relative README.md %}
{% endcapture %}

{% capture previews_html %}
{% include previews-grid.html %}
{% endcapture %}

{%- comment -%}
Step 3: Render the modified content as HTML and strip the auto-inserted ToC if present.
Note: Use HTML entities in regex pattern because Liquid may HTML-escape when piping.
{%- endcomment -%}
{%- assign rendered = content_with_previews | markdownify -%}
{%- assign without_heading = rendered
  | replace_regex: '(?is)<h2[^>]*>\\s*Table of contents\\s*</h2>\\s*(<ul[\\s\\S]*?</ul>|<ol[\\s\\S]*?</ol>|<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>)', ''
-%}
{%- assign without_containers = without_heading
  | replace_regex: '(?is)<nav[^>]*class="toc"[^>]*>[\\s\\S]*?</nav>', ''
  | replace_regex: '(?is)<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>', ''
-%}

{{ without_containers }}