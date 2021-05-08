---
title: Writing
permalink: /blog/notes
nav: blog
---

{% for post in site.categories.note %}
{% include blog-listing.html %}
{% endfor %}