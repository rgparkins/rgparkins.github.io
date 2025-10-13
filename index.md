---
layout: default
title: Home
---


<div class="row justify-content-center">
<div class="col-lg-8">
{% for post in site.posts %}
<div class="card mb-4 shadow-sm">
<div class="card-body">
<h3 class="card-title"><a href="{{ post.url | relative_url }}" class="text-decoration-none text-dark">{{ post.title }}</a></h3>
<p class="card-text text-muted small mb-2">{{ post.date | date: "%B %d, %Y" }}</p>
<p class="card-text">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
<a href="{{ post.url | relative_url }}" class="btn btn-success btn-sm">Read More</a>
</div>
</div>
{% endfor %}
</div>
</div>