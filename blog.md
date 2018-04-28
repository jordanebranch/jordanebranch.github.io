---
layout: page
title: Blog
permalink: /blog/
---

<ul class="blog-list">

	<h2 class="list-title">Blog</h2>
	{% for post in site.posts %}
		<a href="{{ site.baseurl }}{{ post.url }}" target="_blank">
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
