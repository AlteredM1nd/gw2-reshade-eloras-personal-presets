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
Step 2: Replace the markdown image table in the raw README content
with our custom HTML grid. This ensures the GitHub Pages site gets
the clickable, correctly-pathed grid, while the README on GitHub.com
retains its original markdown table.
{%- endcomment -%}
{%- assign content_with_previews = readme_raw
  | replace_regex: '(?s)<!-- PREVIEWS_START -->.*?<!-- PREVIEWS_END -->', previews_html
-%}

{%- comment -%}
Step 3: Now, render the modified content as HTML and strip the auto-inserted ToC.
{%- endcomment -%}
{%- assign rendered = content_with_previews | markdownify -%}
{%- assign without_heading = rendered
  | replace_regex: '(?is)<h2[^>]*>\\s*Table of contents\\s*</h2>\\s*(<ul[\\s\\S]*?</ul>|<ol[\\s\\S]*?</ol>|<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>)',''
-%}
{%- assign without_containers = without_heading
  | replace_regex: '(?is)<nav[^>]*class="toc"[^>]*>[\\s\\S]*?</nav>',''
  | replace_regex: '(?is)<div[^>]*class="toc"[^>]*>[\\s\\S]*?</div>',''
-%}

{{ without_containers }}