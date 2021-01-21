{% set iter = body | markdown | split(pat="<hr />") %}
{% set cpt = 0 %}

{%- for codeblock in iter -%}
{%- set_global cpt = cpt + 1 -%}
### Number {{ cpt }}
{{ codeblock | safe }}
{%- endfor %}
