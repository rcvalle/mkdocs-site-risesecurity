---
hide:
  - footer
title: Auxiliary modules
---

Metasploit
==========

These are the auxiliary modules we developed that are part of Metasploit:

## Auxiliary modules

{%- for module in modules %}
{%- if module.name.startswith("auxiliary/") %}
### {{ module.name }}

<aside class="mdx-font-size-small" markdown>
:material-calendar:{ title="Published" } {{ module.published.strftime("%b %-d, %Y") }}
{%- if module.updated %}
· :material-calendar-check:{ title="Updated" } {{ module.updated.strftime("%b %-d, %Y") }}
{%- endif %}
{%- if module.vulnerabilities %}
· :material-bug:{ title="Vulnerabilities" } {{ ", ".join(module.vulnerabilities) }}
{%- endif -%}
</aside>

{{ module.description }}

:material-download:{ title="Download" } [{{ module.name.split("/")[-1] }}.rb](https://github.com/risesecurity/metasploit/raw/HEAD/modules/{{ module.name }}.rb)
· :material-link:{ title="Link" } [View on Rapid7 Database](https://www.rapid7.com/db/modules/{{ module.name }})
{%- endif %}
{%- endfor %}
