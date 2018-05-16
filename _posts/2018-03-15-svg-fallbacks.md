---
layout: post
title:  SVGs and fallbacks
date:   2018-03-22 11:15:06 +0100
category: [work, learn]
tags: [svg, workflow]
---
One of my very first tickets (that was not testing) was to work with SVG icons. This was right after learning how to animate them on Treehouse so I was very keen. However, on Wellcome’s website we don’t animate and .svgs are in the background.

### The SVG workflow
1. Grab the file from the designer
2. [svgo](https://github.com/svg/svgo) that sucker
3. [use cartman](https://codepen.io/jakob-e/pen/doMoML)
4. copy into \|\| create a mixin not forgetting to change the fill

### Fallbacks
There is a very small minority of wellcome.ac.uk visitors who use old browsers with no .svg support. For them we need to maintain a fallback method which is an icon sprite .png file with an scss fragment dedicated to plotting every single icon’s position.
