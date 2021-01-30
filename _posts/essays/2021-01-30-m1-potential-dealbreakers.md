---
title: The M1 Has Potential Dealbreakers
description: Despite having some amazing, even revolutionary features, the new m1 Macs are far from being a finished product. 
category: essay
tags: apple
permalink: /blog/m1-potential-dealbreakers
date: 2021-01-30 10:20
---

The new M1 Macs are the darling of the internet, which is understandable. The battery life, speed and performance are incredible. 

My M1 MacBook Air is fast and silent, while my 15” work MacBook Pro is loud, hot and even sluggish. The former costs 1k, the latter 3k.

Software compatibility is mostly a non-issue. Rosetta x86 apps hum along just fine with Rosetta. If you have a specialized workflow, obviously check if the software you need [runs on an M1](https://isapplesiliconready.com). 

My only issue was getting homebrew and ruby to work without a bunch of annoying steps. Then I found [this workaround](https://medium.com/swlh/issues-installing-homebrew-on-new-macbook-m1-silicon-heres-how-to-fix-it-8b63921c7290): duplicate the terminal, set the duplicate to always run via Rosetta, and install homebrew and development stuff all via Rosetta. Once homebrew has less experimental Apple Silicon support, I’ll hop back to the original terminal. 

I’ve hit two major snags, one of which would make the M1 a dealbreaker were it the only Mac I had access to. 

Booting an M1 from recovery mode and doing a reset is bricking those running Big Sur 11.0. I had to reset my Air (it went into an infinite restart loop). Luckily, I’d already updated to Big Sur to 11.1, but [it was still a pain](https://support.apple.com/en-us/HT211983). 

I don’t see much incentive for Apple to fix this. Their new business model is to heavily push AppleCare&thinsp;—&thinsp;have a problem? Drop it off and pick up a new machine! 

Ukraine has no Apple Stores. If something happens to my MacBook, I’m up a crick. 

It turns out there’s a bug that breaks all third-party iOS apps when you sync a device with an M1. There’s [currently no fix](https://old.reddit.com/r/MacOS/comments/kf05pz/syncing_iphone_11_pro_max_or_ipad_pro_129_2020_to/). This would be a dealbreaker for me: most of my music is from [Bandcamp](/blog/the-bandcamp-model) and can only be loaded to the Music App via syncing with a Mac. In my case, I’m lucky enough to have a work Mac that I can use, but a brand new Mac *should* be able to sync with other Apple devices. 

I wonder if Apple testers even attempted this flow. There’s the assumption that people will only use Apple Music and backup their phones via iCloud. And it’s not in Apple’s interest to fix this any time soon. 

I still like my M1. But it feels ever so lightly less like my own computer than a device rented from Apple’s marketing department. It remains to be seen whether these bugs are going to ironed out or the beginning of an even stronger push to make Macs into iPads and Apple Subscription devices. 



