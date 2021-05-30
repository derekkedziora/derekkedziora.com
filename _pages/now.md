---
title: "Now" 
description: "What I'm currently up to"
nowPage: true
permalink: /now
layout: post
---

{%- include now-blurb.html -%}

{{ site.categories.now[0].content }}

<p class="aside" markdown="1">Want a similar dynamic now page? Here's [how mine works](/blog/dynamic-now-page).</p>

## Previous Updates

{% assign display-post-type = false %}
{% for post in site.categories.now offset: 1 %}
{%- include blog-listing.html -%}
{% endfor %}
