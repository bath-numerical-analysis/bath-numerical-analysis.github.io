---
title: Research
layout: single
sidebar:
  nav: "research"
permalink: /research/
classes: wide 
---
We are very active in each of the following research topics - click for further descriptions.

{% assign sorted = site.research | sort: 'title'  %}

<ul class="two_column" >
  {% for X in sorted %}
      <a class="btn btn--inverse" href = "{{site.url}}{{site.baseurl}}{{X.url}}">{{X.title}}</a>
    <br/>
  {% endfor %}
</ul>
