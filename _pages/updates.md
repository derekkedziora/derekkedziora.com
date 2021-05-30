---
title: Writing
description: "Updates about what I’ve been up to" 
permalink: /blog/now
nav: blog
---

{% for post in site.categories.now %}
{% include blog-listing.html %}
{% endfor %}