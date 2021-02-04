---
title: Adding a Dynamic Now Page in Jekyll
description: "Make an auto-updating now page on a static site like Jekyll, Hugo, 11ty or Gatsby"
syntax: true
category: tech-guide
tags: jekyll 
permalink: /blog/dynamic-now-page
---

I love the [now page movement](https://sive.rs/nowff). It's such a better way to stay up to date with people than social media. 

But, there are a few things I don't like about just using the same static page again and again. You don't share it via RSS and lose what your "now" was in the past. You could get around this with some manual work, but what's the fun in that? 

The dynamic now page I created is for Jekyll, but will work with only minor modifications in 11ty, Hugo and Gatsby. Updating your now page is the same as writing a regular post, just add `category: now` to your YAML front matter. 

What you get automatically: 
- Your `/now` page updates 
- The update is published in your RSS feed
- Your `/now` page has a list of "previous now pages" 
- The main list of posts doesn't include your now updates 
- You can even have a Now RSS feed

This can all be done on a static site!

## Create a Now Page 

If you don't already have a now page, create a page that with url `/now`. 

To get the content from your most recent now page, all you need is this code: 

{% highlight Liquid %}
{% raw %}{{ site.categories.now[0].content }}{% endraw %}
{% endhighlight %}

To make a list of your previous now posts, add this: 

{% highlight Liquid %}
{% raw %}{% for post in site.categories.now offset: 1 %}

[{{post.title}}]({{post.url}})

{% endfor %}{% endraw %}
{% endhighlight %}

The `offset: 1`  excludes the current now page from the list of previous ones. 

You’re done as far as functionality goes&thinsp;—&thinsp;everything else is cosmetic. 

## Adding a dynamic title 

Giving your `/now` page a dynamic title is a nice touch. You can't add dynamic text directly to YAML, but there's a workaround. 

Add this variable to your now page's front matter: 

{% highlight YAML %}
nowPage: true
{% endhighlight %}

And put this conditional into the `<h1>` tags of the template your using for your now page: 

{% highlight Liquid %}
{% raw %}<h1>{%- if page.nowPage -%}
{{ site.categories.now[0].title }}
{%- else -%}{{ page.title }}{%- endif -%}</h1>{% endraw %}
{% endhighlight %}

I use my post template because I have the date prominently displayed, which makes more sense than a dateless page template.

## Excluding from the post list 

Since I post now updates every six weeks or so, they'd quickly overwhelm my main list of posts on my `/blog` page. One conditional fixes that: 

{% highlight Liquid %}{% raw %}
{% for post in site.posts %}
	{% unless post.categories contains "now" %}

	[{{post.title}}]({{post.url}})

	{% endunless %}
{% endfor %}{% endraw %}
{% endhighlight %}

## Setting up RSS 

If you already have an RSS feed for all of your posts, you're good to go. If not, [install the feed plugin first](https://github.com/jekyll/jekyll-feed).

<section markdown="1" class="aside">
### RSS Requires Unique File Names

For the Jekyll Feed plugin to recognize posts as new, the file name (excluding the date) needs to be unique. Thus `2020-06-01-now.md` and `2020-08-01-now.md` are the same post to an RSS feed.

Go with something like `2020-06-01-now-june-2020.md` and `2020-08-01-now-august-2020.md` to avoid this. 
</section>

If you want a specific RSS feed just for your now posts, add this to your `_config.yml` file: 

{% highlight YAML %}
feed: 
  categories: 
    - now 
{% endhighlight %}

In addition to including now posts in your regular feed, you'll get a now only feed at `/feed/now.xml`. 

## See it live

This works on my [now page](/now) ([view the source code](https://github.com/derekkedziora/derekkedziora.com/blob/main/_pages/now.md)) 

My [Jekyll demo site](https://demo.derekkedziora.com) has less code, so is easier to copy from. Or have a look at the [source code](https://github.com/derekkedziora/derekkedziora.com) of this site. 

You can always [get in touch](/about#contact) with me directly with questions or to show me your dynamic now page. 

