---
layout: post
title:  Switching to Jekyll
date:   2018-05-07 21:15:06 +0100
tags: [antics, jekyll]
---

After the great, [error message filled adventure of switching to Linux][switching-ubuntu], I have decided - in the name of nudging myself out of my comfort zones - to switch my blog to Jekyll.

In the long run I imagine this to be a great time saver. In the short one though, not so much...

After working for years with WordPress and now getting comfortable with Drupal, Jekyll feels like it's a step up instead of down in difficulty. But then again, I am used to doing things with GUIs.

In the spirit of these initial posts being more of a source of entertainment here is my most embarassing mistake I have made.

## Antics

My Jekyll site is using the Minima theme which is great but I wanted to tweak stuff and use this maybe as a little SASSxercise. So I looked for the sass files and found them in a seperate system folder. No problem, I can just add that folder to my workspace in VS Code and work on the two folders like so.

Yeah, no. My local site was not updating the CSS file for some reason (gee, I wonder why?) but when I made changes in the site's actual folder all was going well. After an embarassingly long time I realised that my setup was probably not right.

At this point I finally went and read the Jekyll Docs and lo and behold, I was wrong. It's a feeling I am getting very familiar with lately.

Copying the appropriate folders **into** my site's folder has done the trick in the end.


[switching-ubuntu]: {{ site.baseurl }}{% link _posts/2018-05-02-switch-to-ubuntu.markdown %}
