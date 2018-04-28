---
layout: page
title: Projects
permalink: /work/
---

<ul class="portfolio-list">

	<h2>Custom Editorial Stories</h2>
	{% for editorial-project in site.data.editorial-projects %}
		<a href="{{editorial-project.external_url}}" target="_blank">
		  	<li>
		  		<div class="card">
		  			<!--<div class="placeholder-image"></div>-->
					<img src="{{ site.baseurl }}/images/{{ editorial-project.image }}">
					<div class="card-copy">
						<h2>{{editorial-project.name}}</h2>
						<p>{{editorial-project.description}}</p>
					</div>
				</div>
		  	</li>
	  	</a>
	{% endfor %}

	<h2>Custom Editorial Graphics</h2>
	{% for editorial-graphic in site.data.editorial-graphics %}
		<a href="{{editorial-graphic.external_url}}" target="_blank">
		  	<li>
		  		<div class="card">
		  			<div class="placeholder-image"></div>
					<!--<img src="{{ site.baseurl }}/images/{{ project.image }}">-->
					<div class="card-copy">
						<h2>{{editorial-graphic.name}}</h2>
						<p>{{editorial-graphic.description}}</p>
					</div>
				</div>
		  	</li>
	  	</a>
	{% endfor %}

</ul>