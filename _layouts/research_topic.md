---
layout: single
---
{{content}}

{% assign sorted = site.members | sort: 'last'  %}
{% for member in sorted %}
  {% if member.topics contains page.code %}
       <a class="btn btn--inverse" href="{{ member.homepage }}">
      {{member.given}} {{member.last}}</a>
      {% endif %}
{% endfor %}
