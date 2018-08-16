---
layout: post
title:  What's the Weather Like? - fCC Challenge
date:   2017-10-21 11:15:06 +0100
tags: [freeCodeCamp, build]
excerpt: "<p>Building a single page app using a simple weather API was one of the fCC challenges. Read on for the user story and what gave me a headache.</p>"
---

Since I have decided to become a Developer I have been studying on freeCodeCamp. It’s an amazing, free online bootcamp with some pretty challenging lessons and build challenges.

### Weather API

#### User stories

1. I can see the weather in my current location.
2. I can see a different icon or background image (e.g. snowy mountain, hot desert) depending on the weather.
3. I can push a button to toggle between Fahrenheit and Celsius.

#### The build

This was a real kicker. My first time working with JSON and my very first GET request to an API. FreeCodeCamp has the tendency to give you a task that they may have not equipped you fully for before to handle. You need to be able to articulate your problems and then do a LOT of research to solve them.

In the end I've managed to throw it together with only a few bugs left:

1. The location error handling was non-existent. UPDATE: I have now managed to fix this with the help of the MDN docs on `navigator.geolocation`.
2. Fixed footer is not so fixed. My original fixed footer lacked left and right padding. UPDATE: all fixed and padded.

[![weather app]({{ site.url }}/assets/img/project_weather "is it raining again?")](/projects/fcc-weather/)

### Next on

Creating a single-page app working with [Twitch's API]({{ site.baseurl }}{% link _posts/2017-11-03-fcc-twitch.md %}).