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
		  			<div class="card-copy">
						<h2>{{ post.title }}</h2>
						<p>{{post.description}}</p>
					</div>
				</div>
		  	</li>
	  	</a>
	{% endfor %}

</ul>
