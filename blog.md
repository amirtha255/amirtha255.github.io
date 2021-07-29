---
layout: post
title: 
background: 
---

<img src="/assets/img/blog.png" class="img-fluid"/>


<hr width="60%">
<blockquote style="text-align: center;">
    <p>"It is important to draw wisdom from many different places. If you take it from only one place, it becomes rigid and stale." - General Iroh ATLA
</p>
</blockquote>
<hr width="60%">


<p> 
	<!--I write blogs when I want to share info which I had difficulty getting, to document my learning and experiences or just to get in the flow. -->
	<h3> Latest posts </h3>
</p>
<ul>
  {% for post in site.posts %}
  	{% if post.categories contains 'blog' %}
	    <li>
	      <a href="{{ post.url }}">{{ post.title }}</a>
	      {{ post.excerpt }}
	    </li>
	{% endif %}   
  {% endfor %}
</ul>
