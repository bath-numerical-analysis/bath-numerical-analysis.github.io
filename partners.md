---
title: Partners
layout: single
sidebar:
  nav: "research"
permalink: /research/partners.html
---

<h4><a id="Bath">In Bath</a></h4>

<ul  class="two_column">
{% for partner in site.data.partners_bath %}
  <li>
    <a class="btn btn--inverse" href="{{partner.url}}">
      {{ partner.title }}
    </a>
  </li>
{% endfor %}
</ul>

<h4><a id="Beyond">And beyond</a></h4>
<ul  class="two_column">
{% for partner in site.data.partners_outside %}
  <li>
    <a class="btn btn--inverse" href="{{partner.url}}">
      {{ partner.title }}
    </a>
  </li>
{% endfor %}
</ul>
