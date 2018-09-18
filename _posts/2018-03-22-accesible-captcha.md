---
layout: post
title: Do Accessible CAPTCHAs exist?
date: 2018-03-22 11:15:06 +0100
tags: [accessibility]
excerpt: "<p>Spoiler alert: the answer is no</p>"
---

### The challenge

Find an accessible CAPTCHA.

_Spoiler alert:_ there isn’t really one out there, unless you are ready to sacrifice security.

### The research

Went on a research journey through W3C, WebAim (web accessibility in mind) and Stackoverflow.
Conclusion: if we want to be perfectly accessible we should forget CAPTCHAs and use Honeypot.

#### CAPTCHAs

##### Invisible CAPTCHA

Most accessible of CAPTCHAs when it’s not triggered... however it seems it frequently goes off when using screen readers and assistive technology in which case it reverts back to noCAPTCHA/reCAPTCHA which is what we are trying to avoid as [these are both very inaccessible](https://webaim.org/discussion/mail_thread?thread=8034).

##### TextCAPTCHA

- One of the - if not the most - accessible form of CAPTCHA
- It is a security risk (a clever enough script can pass it)
- Relies on 7+ yr cognitive abilities
- Adds about 10-20 seconds to time spent on solving when someone’s first language is not English

#### Honeypot

Protects from random spam (which was our main issue) but not particularly secure.

_Recommended method:_
Field pulled off screen: needs to be correctly labeled (i.e. “do not fill in this field if you are a human”)

_Not recommended:_
display: none - this might be way too easy to bypass for some scripts.

### User testing

Once we have decided on trying out Honeypot it was time to implement it and try it out in the wild. This also meant doing some user testing with one of our colleagues who uses a screenreader. Long story short, it went swimmingly and our user was in fact well pleased with the experience.

### Pentesting

Being a very basic method of protection Honeypot has easily failed penetration testing as you could get through it easy via HTTP requests instead of using the website itself.

### What now?

A decision has to be made: do we value accessibility over the inconvenience of being relentlessly spammed?
