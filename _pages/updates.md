---
title: Writing
permalink: /blog/now
nav: blog
---

{% for post in site.categories.now %}
{% include blog-listing.html %}
{% endfor %}