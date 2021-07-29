---
layout: post
title: 
background: 
---

<br>

<img src= "/assets/img/musings.png" class="img-fluid"/>
<ul>
  {% for post in site.posts %}
  	{% if post.categories contains 'musings' %}
	    <li>
	      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
	      {{ post.excerpt }}
	    </li>
	{% endif %}   
  {% endfor %}
</ul>