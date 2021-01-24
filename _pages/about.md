---
title: About Me
description: "Derek Kedziora is a UX writer, content strategist, geek, tinkerer and avid reader."   
about: true
permalink: /about
nav: about
--- 

<figure class="about-picture"><img src="" alt="" title="Derek Kedziora" id="aboutImg"><figcaption id="aboutImgCaption"></figcaption>
</figure>

<noscript>
<figure class="about-picture"><img src="hhttps://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/all-smiles_kemzfu.jpg" alt="" title="Derek Kedziora">
<figcaption>That’s me</figcaption></figure>
</noscript>

I’m a writer in tech: everything from UX writing, content strategy, marketing and documentation. Before that, I was English teacher. 

🤓&emsp;Geek<br>
🐈&emsp;Cat lover<br>
📚&emsp;Bookworm<br>
🧘&emsp;Meditator<br> 
🇺🇸&emsp;From the US<br>
🇺🇦&emsp;Live in Ukraine 

## Contact 

📫&emsp;{{ site.email }}

💬&emsp;You can find me on [LinkedIn](https://www.linkedin.com/in/derekkedziora/), [Twitter](https://twitter.com/derekkedziora) and [GitHub](https://github.com/derekkedziora). 

## RSS 

The [everything feed](/feed.xml) is for, well, everything. 

If that’s too cluttered, you can get only [longer posts](/feed/essays.xml), [shorter posts](/feed/stream.xml), [English guides](/feed/english-guide.xml) and [now updates](/feed/now.xml) separately. 

## Colophon 

This is a [small b blog](https://tomcritchlow.com/2018/02/23/small-b-blogging/). It's meant to be lighthearted, rough around the edges and an ongoing work in progress. 

I use [Jekyll](https://jekyllrb.com) to build a static site. View the [source code on GitHub](https://github.com/derekkedziora/derekkedziora.com) and [local change log](/change-log).

Matthew Butterick's [Practical Typography](https://practicaltypography.com) has heavily influenced my layout and typography choices. 

<script>
const photos = [
"https://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/all-smiles_kemzfu.jpg", 
"https://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/fancy_fulfpw.jpg", 
"https://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/office_nwywv8.jpg",
"https://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/pub-quiz_p2v4ia.jpg",
"https://res.cloudinary.com/derekkedziora/image/upload/v1611489228/About%20%28400x400%29/hello-kotik_xhykdo.jpg"
]

const captions = [
"That’s me",
"Looking fancy",
"An office smile",
"The Pub Quiz Master",
"I’m owned by a cat"
]

const selectedPhoto = Math.floor(Math.random() * photos.length)

document.getElementById("aboutImg").setAttribute("src", photos[selectedPhoto]);
document.getElementById("aboutImgCaption").innerHTML = captions[selectedPhoto];
</script>