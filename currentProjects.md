---
layout: page
title: "Projects"
description: "Projects under 4I Labs"
header-img: "img/home-bg.jpg"
---


{% for page in site.pages %}{% if page.url contains "projects/" %}{% if page.title %}
	
<div class="jumbotron" style="background-image: url(../{{ page.img  }}); background-size: cover; ">
	<h2>{{ page.title }}</h2>
	<a href="{{ page.url | prepend: site.baseurl }}" class="btn btn-info" >Page</a>
	<a href="{{ page.docs }}" class="btn btn-info" >Docs</a>
	<button type="button" class="btn btn-info" data-toggle="collapse" data-target="#text{{ forloop.index }}">More</button>
	<div id="text{{ forloop.index }}" class="collapse"><p>{{ page.text }}</p></div>
</div>
{% endif %}{% endif %}{% endfor %}