---
title: Staff
layout: single
sidebar: 
  nav: "people"
permalink: /people/
classes: wide
---
<ul id="two_col">
  {% assign sorted = site.members | sort: 'last'  %}
  {% for member in sorted %}
    <li >
      <div class="row">
        <div class="column1">
           <a href="{{ member.homepage }}">
           <img  src="/assets/pics/{{member.pic}} " id="two_col_img"/></a>
        </div>
        <div class="column2">
        <a class="btn btn--inverse" href="{{ member.homepage }}"> {{member.given}} {{ member.last}} </a>
        <p class="small">{{ member.research }}</p>
       </div>
      </div>
    </li>
  {% endfor %}
</ul>
