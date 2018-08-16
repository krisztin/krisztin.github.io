---
layout: post
title:  Are you local?
date:   2018-05-10 11:15:06 +0100
tags: [lamp, docker]
---

At some point during your developer life you will realise testing code in a dev environment, or worst, on stage is maybe not the best idea...and also not very fast.

At work we use Docker which is great...when it works. Unfortunately, mine breaks intermittently and it’s a bit of a developing X-File what actually trips it up. Basically, it stops syncing my code after anything between 1-5 minutes at which point you have to do the good old IT magic solution of turning it off and on again.

{% include img.html file='itcrowdonoff.jpg' alt='it crowd gag'
caption="Have I? Well yes. Several times." -%}

At home, for a while now, I have been using MAMP. Don’t judge me, I was a strictly Windows gal up until a few weeks ago. After my switch to Ubuntu I went on a furious Googling journey about Virtual Machines and other local dev environments. Somehow I had a hard time wrapping my head around _why_ I would need Virtualbox and Vagrant to run a Linux machine for me when I was already running Linux. I kid you not, at one point I have googled ‘do I need virtual machine for local environment on Linux?’.
In case you are wondering, the answer is yes and I’ll just save myself the embarrassment and will not tell you how long this conclusion has taken me.

To my defence I had _no idea_ what an actual local environment did, how it worked or anything. Docker at this point was just magic (it still is at times). Retrospectively, it was probably not a good idea to try to set something up of what I had no understanding.

#### Hey, I know this place!
Anyhow, being familiar with the thing and having managed to make it work before, I went with MAMP. It sort of worked but then it didn’t really. On Windows I got used to having a nice GUI where I could stop/start my server and check the logs with a click. The Ubuntu version also has a GUI but I have never managed to make it work so I could save it as a shortcut. Trust me, when you get to the point where you have to google how to create a shortcut after hours of struggling and with the knowledge that this took you less than 30 minutes on Windows, you kinda loose the determination to make the thing work. Also, I resigned myself to the fact that on Ubuntu one has to live without GUIs and command line everything. In the name of throwing away my crutches I have purged the sucker and moved on.

#### The lightbulb moment
Whilst trying to make MAMP work, I did look into what it actually was and found LAMP. Installed Apache, MySQL and PHP and hey presto, it worked. Well, when I say worked, I should say works as it’s continuously running. I could switch everything off in the command line but I am still a Windows person at heart and refuse to switch things on and off unless they have a button. Plus, I don’t really see that anything is running, because again: no GUI. Blissful ignorance.

#### Is LAMP enough?
This was the point when I started understanding local (or really any) environments. I got that we are basically trying to emulate the server environment so that we don’t bump into issues stemming from the server being on PHP 5 whilst we are on 7 locally.
So the answer to the question is: depends. If you have a single product you are working on with one set environment then everything should be fine. But then the moment you take up another job that needs a different version of MySQL for instance, you are screwed.

#### Moving into containers
Wanting to work on widely different projects (Drupal, WordPress, Jekyll and whatever else I feel like) and not wanting to sacrifice my entire SSD to the Vagrant gods I have decided the next step on my Linux machine will be to make Docker work.
During one of our Golden Times (an afternoon allocated to doing a task of your choosing that is not a ticket but could improve the product) I dived into the [Docker Labs](https://github.com/docker/labs) and went through how to create a docker image and docker file. The end result was a Python cat .gif app and a slightly better understanding of how Docker works.