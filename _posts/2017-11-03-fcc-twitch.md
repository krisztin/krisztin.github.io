---
layout: post
title:  Who's Online? - fCC Challenge
date:   2017-11-03 11:15:06 +0100
category: [play]
tags: [freeCodeCamp, build]
---

Since I have decided to become a Developer I have been studying on freeCodeCamp. It’s an amazing, free online bootcamp with some pretty challenging lessons and challenges.

### User stories:

1. I can see whether Free Code Camp is currently streaming on Twitch.tv.
2. I can click the status output and be sent directly to the Free Code Camp's Twitch.tv channel.
3. If a Twitch user is currently streaming, I can see additional details about what they are streaming.

### What I have added:

1. Filtering buttons to show only online users.
2. Channel profile pictures.

I’ll be honest with you, this took me a **few** long days to figure out. I got completely stumped about how to make two concurrent JSON get requests within one function. [My previous JSON adventure with the weather API]({{ site.baseurl }}{% link _posts/2017-10-21-fcc-weather.md %})) was entirely useless and my knowledge of JS was quite inadequate at this point (it still is to be honest).

<p class="codepen" data-default-tab="js,result" data-embed-version="2" data-height="500" data-pen-title="Twitch" data-slug-hash="wrVWZJ" data-theme-id="0" data-user="krisztiiin">See the Pen <a href="https://codepen.io/krisztiiin/pen/wrVWZJ/">Twitch</a> by Kriszti (<a href="https://codepen.io/krisztiiin">@krisztiiin</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

### Challenges
**Two JSON GETs:** So yes, I knew how to make **a** - as in one, single - GET request thanks to the weather API challenge but now I've needed to make two, both the channels and streams data, to compile the resulting HTML output. It took me way too long to figure out that I could go with .done and then make the second request in that function.

**CSS:** The h2 element in my title class refused to align itself in the middle so I had to resort to defining the line-height.

**Fixed footer:** It ended up covering the content at the bottom of the page on smaller devices. Fixed it with adding a bottom margin to the body.