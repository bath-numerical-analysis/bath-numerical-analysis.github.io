---
title: Partners
layout: single
sidebar:
  nav: "research"
permalink: /research/partners.html
---

<h4><a id="Bath">In Bath</a></h4>

<ul  class="two_column">
{% assign sorted = site.data.partners_bath | sort: 'title' %}
{% for partner in sorted %}
  
    <a class="btn btn--inverse" href="{{partner.url}}">
      {{ partner.title }}
    </a> &nbsp;
  
{% endfor %}
</ul>

<h4><a id="Beyond">And beyond</a></h4>
<ul  class="two_column">
{% assign sorted2 = site.data.partners_outside | sort: 'title' %}
{% for partner in sorted2 %}
  
    <a class="btn btn--inverse" href="{{partner.url}}">
      {{ partner.title }}
     </a> &nbsp;
  
  
{% endfor %}
</ul>
