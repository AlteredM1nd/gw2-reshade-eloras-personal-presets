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
Step 2: Replace the README previews block using explicit split markers instead of regex.
This avoids differences in regex engines/flags on GitHub Pages.
Markers in README.md must be exactly:
<!-- PREVIEWS_START -->
...table markdown...
<!-- PREVIEWS_END -->
{%- endcomment -%}
{%- assign split_on_start = readme_raw | split: "<!-- PREVIEWS_START -->" -%}
{%- if split_on_start.size > 1 -%}
  {%- assign head_part = split_on_start[0] -%}
  {%- assign after_start = split_on_start[1] -%}
  {%- assign split_on_end = after_start | split: "<!-- PREVIEWS_END -->" -%}
  {%- if split_on_end.size > 1 -%}
    {%- assign tail_part = split_on_end[1] -%}
    {%- capture content_with_previews -%}
{{ head_part }}{{ previews_html }}
{{ tail_part }}
    {%- endcapture -%}
  {%- else -%}
    {%- comment -%} Missing end marker; fall back to original content {%- endcomment -%}
    {%- assign content_with_previews = readme_raw -%}
  {%- endif -%}
{%- else -%}
  {%- comment -%} Missing start marker; fall back to original content {%- endcomment -%}
  {%- assign content_with_previews = readme_raw -%}
{%- endif -%}

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