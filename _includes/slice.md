{%- comment -%}
Slice include: extracts content between start/end HTML comments in a source file.
Usage:
  {% include slice.md file="README.md" start="<!-- SLICE: About This Preset start -->" end="<!-- SLICE: About This Preset end -->" %}
Notes:
  - This include must use include_relative (safe mode). It resolves the path relative to the including file.
  - Therefore, pass file as a path relative to the including file, e.g. "../README.md" from docs/*.md
{%- endcomment -%}
{%- assign src = include.file | default: "README.md" -%}
{%- assign start = include.start -%}
{%- assign end = include.end -%}
{%- capture raw -%}{% include_relative {{ src }} %}{%- endcapture -%}
{%- assign parts = raw | split: start -%}
{%- if parts.size > 1 -%}
  {%- assign after = parts[1] -%}
  {%- assign seg = after | split: end | first -%}
  {{ seg | markdownify }}
{%- else -%}
  <!-- slice.md: start marker not found: {{ start }} -->
{%- endif -%}