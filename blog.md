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
		  			<img src="{{ site.baseurl }}/{{ post.image }}">
		  			<div class="card-copy">
						<h2>{{ post.title }}</h2>
						<p>{{post.description}}</p>
						<span class="date">{{post.date | date: "%B %e, %Y" }}</span>
					</div>
				</div>
		  	</li>
	  	</a>
  	{% endfor %}
	<!--{% for post in paginator.posts %}
		<a href="{{ site.baseurl }}{{ post.url }}">
		  	<li>
		  		<div class="card">
		  			<img src="{{ site.baseurl }}/{{ post.image }}">
		  			<div class="card-copy">
						<h2>{{ post.title }}</h2>
						<p>{{post.description}}</p>
						<span class="date">{{post.date | date: "%B %e, %Y" }}</span>
					</div>
				</div>
		  	</li>
	  	</a>
	{% endfor %}-->
	<!-- Pagination links -->
	<!--<div class="pagination">
	  	{% if paginator.previous_page %}
	    	<a href="{{ paginator.previous_page_path }}" class="previous">Previous</a>
	  	{% else %}
	  		<span class="previous off">Previous</span>
	  	{% endif %}
	  	{% if paginator.next_page %}<a href="{{ paginator.next_page_path }}" class="next">Next</a>
		{% else %}
	    	<span class="next off">Next</span>
	  	{% endif %}
	</div>-->
</ul>
