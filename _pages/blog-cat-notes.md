---
title: "Blog: Notes"
description: "The list of all of short form posts."
og-type: website
permalink: /blog/category/notes
nav: blog
---

{% for post in site.categories.note %}
{%- include blog-listing.html -%}
{% endfor %}