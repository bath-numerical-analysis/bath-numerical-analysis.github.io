---
layout: single
---

{{ page.code }}

  {% for member in site.members %}
  {% if member.units contains page.code %}
       <a href="{{ member.homepage }}">
      {{member.given}} {{member.last}}</a>
      {% endif %}
  {% endfor %}

<p>

{{ page.content }}
</p>
