---
title: Writing
description: "All of the posts in Derek’s Digital Garden"
og-type: website
permalink: /blog
nav: blog
display-post-type: true 
---

{% for post in site.posts %}
{% unless post.categories contains "unlisted" %}
{% include blog-listing.html %}
{% endunless %}
{% endfor %}