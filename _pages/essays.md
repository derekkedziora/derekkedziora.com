---
title: Writing
description: "The list of all of my long-form blog posts."
og-type: website
permalink: /blog/essays
nav: blog
---

{% for post in site.posts %}
{% unless post.categories contains "unlisted" or post.categories contains "now" or post.categories contains "note"%}
{% include blog-listing.html %}
{% endunless %}
{% endfor %}