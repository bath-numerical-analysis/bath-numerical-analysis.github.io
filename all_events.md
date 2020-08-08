---
layout: single
sidebar: 
  nav: "events"
permalink: /events/all.html
toc: true
---
{% assign postsByYear =
    site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}

<div id="archives">
  {% for year in postsByYear %}
  <div class="archive-group">
  <h3><a id="{{year.name}}">{{ year.name }}</a></h3>
  {% for post in year.items %}
    <a class="btn btn--inverse" href="{{site.url}}{{site.baseurl}}{{ post.url }}">{{post.title}} </a>
    <p class="small"> {{post.excerpt}}
    </p>
   {% endfor %}
  </div>
{% endfor %}
</div>
