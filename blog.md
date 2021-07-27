---
layout: post
title: 
background: "/assets/img/blog.png"
---
<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
  	{% if post.categories contains 'blog' %}
	    <li>
	      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
	      {{ post.excerpt }}
	    </li>
	{% endif %}   
  {% endfor %}
</ul>