---
layout: page
title: Blog
permalink: /blog/
---

<h2 class="list-title">Blog</h2>

<ul class="blog-list">

	{% for post in site.posts %}
		<a href="{{ site.baseurl }}{{ post.url }}">
		  	<li>
		  		<div class="card">
		  			<div class="card-copy">
						<h2>{{ post.title }}</h2>
						<p>{{post.description}}</p>
						<span class="date">{{post.date | date: "%B %e, %Y" }}</span>
					</div>
				</div>
		  	</li>
	  	</a>
	{% endfor %}

</ul>
