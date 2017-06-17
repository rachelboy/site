---
layout: cards
title: Blog posts in core
permalink: /blog/category/core
---
<div class="container">
<div class="row">
<div class="col">
<div class="card-columns blog">
{% for post in site.posts %}
{% if post.category == 'core' %}
<div class="card hover-shadow mb-3">
<a href="{{ post.url }}" title="{{ post.title | escape}}"><img class="card-img-top img-fluid" src="/img{{ post.url }}{{ post.img }}" alt="{{ post.caption }}"></a>
<div class="card-block">
<h4 class="card-title"><a href="{{ post.url }}" title="{{ post.title | escape}}">{{ post.title }}</a></h4>
</div>
<footer class="rounded-bottom">
On {{ post.date | date: '%B %d, %Y' }}
by <a href="/blog/author/{{ post.author }}" title="Browse other posts by this author">{{ post.author }}</a>
in <a href="/blog/category/{{ post.categories }}" title="Browse other posts in this category">{{ post.categories }}</a>
</footer>
</div>
{% endif %}
{% endfor %}
</div>
</div>
</div>
</div>
