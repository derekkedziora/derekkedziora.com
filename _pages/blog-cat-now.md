---
title: "Blog: Now Updates"
description: "The list of all of now updates."
og-type: website
permalink: /blog/category/now
nav: blog
---

{% for post in site.categories.now %}
{%- include blog-listing.html -%}
{% endfor %}