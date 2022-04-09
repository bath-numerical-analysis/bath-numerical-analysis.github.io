---
layout: single
title: Upcoming and recent events
permalink: /events/index.html
sidebar: 
  nav: "events"
---
<ul>
{% for post in site.posts limit: 3 %}
  <li><a class="btn btn--inverse" href="{{site.url}}{{site.baseurl}}{{post.url}}">  {{post.title}}
  </a>
  <div class="small"> {{post.excerpt}}
  </div></li>
{% endfor %}
</ul>
