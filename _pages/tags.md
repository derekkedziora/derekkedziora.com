---
title: "Tags & Taxonomy"
description: "All of my blog posts sorted by tag"
nav: blog
permalink: /blog/tags
---

{% include search.html %}

<h2>Post types</h2>
<div class="tag-list">
<a href="/blog/category/essays">Essays ({{ site.categories.essay | size }})</a>
<a href="/blog/category/notes">Notes ({{ site.categories.note | size }})</a>
<a href="/blog/category/now">Now ({{ site.categories.now | size }})</a>
<a href="/blog/category/tech-guides">Tech guides ({{ site.categories.tech-guide | size }})</a>
<a href="/english">English guides ({{ site.categories.english-guide | size }})</a>
</div>

<h2>Tags</h2>

{% assign sortedTags = site.tags | sort %}

<div class="tag-list">
{% for tag in sortedTags %}
	<a href="#{{tag[0]}}">{{ tag[0] }}&nbsp;({{ tag[1] | size }})</a>
{% endfor %}
</div>

{% for tag in sortedTags %}

<section class="posts-by-tag">

<h2 id="{{ tag[0] }}">{{ tag[0] }}</h2>

{% for post in tag[1] %}
	{% include blog-listing.html %}
{% endfor %}

<p><a href="#" class="internal-link">All Tags &#8593;</a></p>

{% endfor %}
