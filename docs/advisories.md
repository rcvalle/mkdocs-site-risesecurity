---
hide:
  - footer
---

Advisories
==========

These are the advisories we published:

{%- for advisory in advisories %}
### {{ advisory.name }}

<aside class="mdx-font-size-small" markdown>
:material-calendar:{ title="Published" } {{ advisory.published.strftime("%b %-d, %Y") }}
{%- if advisory.updated %}
· :material-calendar-check:{ title="Updated" } {{ advisory.updated.strftime("%b %-d, %Y") }}
{%- endif %}
</aside>

---

{{ advisory.description }}

:material-download:{ title="Download" } [{{ advisory.filename }}]({{ advisory.url }})
{%- for resource in advisory.resources %}
· :material-link:{ title="Link" } [{{ resource.name }}]({{ resource.url }})
{%- endfor %}
{%- endfor %}
