---
layout: default
title: Blog
permalink: /blog/
---

<ul class="blog-list">

	<h2>Blog</h2>
	{% for post in site.posts %}
		<a href="{{ site.baseurl }}{{ post.url }}" target="_blank">
		  	<li>
		  		<div class="card">
					<h1>{{ post.title }}</h1>
					<p>{{post.description}}</p>
				</div>
		  	</li>
	  	</a>
	{% endfor %}

</ul>
