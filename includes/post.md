{%- macro meta(name, username, email, published, updated) %}
<aside class="mdx-author" markdown>
![@{{ username }} avatar](https://www.gravatar.com/avatar/{{ email|md5sum }}.jpg?s=40 "@{{ username }} avatar")

<span>{{ name }} · [@{{ username }}](https://github.com/{{ username }})</span>
<span>
:material-calendar:{ title="Published" } {{ published.strftime("%b %-d, %Y") }}
{%- if updated %}
· :material-calendar-check:{ title="Updated" } {{ updated.strftime("%b %-d, %Y") }}
{%- endif %}
</span>
</aside>
{%- endmacro %}
