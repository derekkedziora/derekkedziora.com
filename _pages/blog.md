---
title: Writing
description: "All of the posts in Derek’s Digital Garden"
og-type: website
permalink: /blog/all
nav: blog
---

{% for post in site.posts %}
{% unless post.categories contains "unlisted" %}
{% include blog-listing.html %}
{% endunless %}
{% endfor %}