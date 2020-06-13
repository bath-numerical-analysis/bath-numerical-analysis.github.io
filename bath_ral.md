---
layout: single
sidebar: 
  nav: "events"
permalink: /events/bath_ral.html
---
{% assign sorted = site.categories["BathRAL"]    %}

<h4> Bath/RAL Day </h4>

{% for post in sorted%}<a class="btn btn--inverse" href="{{ post.url }}" href="{{ post.url }}" href="{{ site.baseurl }}{{ post.url }}">{{post.date | date_to_string}}</a>
{% endfor %}
