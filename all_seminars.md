---
layout: single
sidebar: 
  nav: "events"
permalink: /events/all_seminars.html
---
<h1>Bath Numerical Analysis Seminar</h1>
  <p> This seminar series has been running continuously since 1986 and features a range of invited talks from distinguished visitors as well as internal talks by staff and students of the Department of Mathematical Sciences and other departments at the University of Bath.</p>

{% assign sorted = site.categories["bnaseminar"]  | sort:"year"  %}

{% for post in sorted %}<a class="btn btn--inverse" style="width: 45%"  href="{{site.url}}{{ site.baseurl }}{{ post.url }}">{{post.excerpt}}</a>{% endfor %}
