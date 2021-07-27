---
layout: post
title: 
background: "/assets/img/projects.png"
---

<h1>Latest Projects</h1>

<ul>
  {% for post in site.posts %}
  	{% if post.categories contains 'project' %}
	    <li>
	      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
	      {{ post.excerpt }}
	    </li>
	{% endif %}   
  {% endfor %}
</ul>