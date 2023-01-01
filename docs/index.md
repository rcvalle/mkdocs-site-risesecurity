---
hide:
  - footer
search:
  exclude: true
title: Blog
---

<style>
  .md-sidebar--secondary:not([hidden]) {
    visibility: hidden;
  }
</style>

<!-- {%- from 'post.md' import meta %} -->
{%- for post in posts %}
# {{ post.name }}

<!-- {{ meta(post.author.name, post.author.username, post.author.email, post.published, post.updated) }} -->
<aside class="mdx-font-size-small" markdown>
:material-calendar:{ title="Published" } {{ post.published.strftime("%b %-d, %Y") }}
{%- if post.updated %}
· :material-calendar-check:{ title="Updated" } {{ post.updated.strftime("%b %-d, %Y") }}
{%- endif %}
</aside>

---

{{ post.description }}

[:material-arrow-right: Continue reading]({{ post.url }})
{%- endfor %}
