---
title: RSS Club
description: "This is my 'secret' page only for people on my RSS list"
permalink: /rss-club
nav: main
display-post-type: false
---

Welcome to the RSS only section. Check out the other cool kids in [RSS Club](https://daverupert.com/2018/01/welcome-to-rss-club/)

RSS is the last frontier of ye olde internet: no tracking, no algorithmic filter bubbles and pages load instantly. 


## RSS Only Posts 

{% assign display-post-type = false %}

{% for post in site.categories.rss-club %}

{% include blog-listing.html %}

{% endfor %}



