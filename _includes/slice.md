{%- comment -%}
Slice include: extracts content between start/end HTML comments in a source file.
Usage:
  {% include slice.md file="README.md" start="<!-- SLICE: About start -->" end="<!-- SLICE: About end -->" %}
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