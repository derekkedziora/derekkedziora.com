---
title: Writing
permalink: /blog/updates
nav: blog
---

{% for post in site.categories.now %}
{% include blog-listing.html %}
{% endfor %}