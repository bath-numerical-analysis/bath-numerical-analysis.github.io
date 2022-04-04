---
layout: single
sidebar: 
  nav: "events"
title: Bath Numerical Analysis seminar - upcoming
permalink: /events/current_seminars.html
classes: wide
---
{% assign sorted = site.categories["bnaseminar"]   %}


<div id="archives">
    {% for post in sorted limit: 1 %}
   {{post.content}}
   {% endfor %}
</div>

{% include future-date.html %}
