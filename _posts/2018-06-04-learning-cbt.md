---
layout: post
title: How I deal with the unknown
date:   2018-06-04 15:15:06 +0100
tags: [rant, learning]
---

Starting over in your thirties is fun. You might think I am being sarcastic but, honestly, I am quite enjoying the journey so far. Other than the utter dread of the unknown of course. The sheer amount of things I need to know is a little bit intimidating at points.

## So how do you deal with the unknown induced dread?

Embrace it and enjoy the constant self-doubt, impostor syndrome and nervousness...now this was sarcasm.

Let me tell you how I really deal with it by telling you about my Compulsory Basic Training (CBT) to ride a motorbike. But Kriszti, you do realise you’re supposed to be writing about coding, right? Just bear with me, this will all make sense.

So, one day I have decided that I wanted to ride a motorbike. Bought a Honda MSX-125, got a provisional licence and booked a CBT. When it all started settling in and the excitement wore off all I was left with was one feeling: I was terrified.

{% include img.html file='motorbike.jpg' alt='my adorable Honda MSX-125'
caption='My precious' -%}

A CBT is a one day event at the end of which you are to ride in traffic for an hour. Meaning on the first day I have ever ridden a motorbike I was to pass the riding test as well. I don’t know about you but that sounds quite terrifying.

There were four of us students there - unsurprisingly, I was the only female but that’s a can of worms we are not opening today. Two chaps were there to renew their CBTs for the untempth time so they were fairly experienced. The third guy had a Driver’s Licence for a while so he wasn’t utterly clueless. And then there was me, the only newly motorised person. Yay.

## Prepare and hope for the best

As with everything else unknown I have done what works best for me: research. The weeks leading up to my CBT my search history became entirely about how to ride a motorbike. Every spare moment was spent reading about bikes and watching videos. LOTS of videos.

### Hey, here is some code!

I was curious just how much time I did dedicate to `freak out YouTubeing` so I dug up my history. Unfortunately, YouTube's history search function puts Bing to shame so I couldn't find all videos I have watched but I did find an old playlist that I have been through a few times over.

```js
// ran this in the console hence the vars

var times = Array.from(document.querySelectorAll('ytd-thumbnail-overlay-time-status-renderer'));

var seconds = times
  .map(time => time.innerText.toString().replace(/\s/g,''))
  .map((timeCode) => {
    const [mins, secs] = timeCode.split(':').map(parseFloat);
    return (mins * 60) + secs;
  })
  .reduce((total, seconds) => total + seconds);

var secondsLeft = seconds
var hours = Math.floor(secondsLeft / 3600)
secondsLeft %= 3600

var mins = Math.floor(secondsLeft / 60)
secondsLeft %= 60

console.log(hours, 'hours', mins, 'mins', secondsLeft, 'seconds')

18 "hours" 45 "mins" 11 "seconds"

```

`18 hours 45 minutes and 11 seconds`. And this was just one playlist. In my history I have found at least another day’s worth of videos on changing gears and how to master the clutch.

### Conclusion

Thanks to my diligent research, cyclist past and a great instructor I’ve passed. I did manage to stall once in the middle of a small T-intersection in traffic but we don’t talk about that, okay?

Afterwards, my instructor told me he was a bit weary that a newbie like me without ever having driven a car could pass. But he was very impressed with my progress and asked for my secret: **“I like to be prepared.”**

He was convinced I’d be back next year for my A1...I never went back. I got a Driver’s Licence instead.
