---
layout: post
title: The Quest for a Missing Ruby Gem
date: 2018-05-12 14:00:06 +0100
tags: ruby jekyll
---

My Jekyll environment was running smoothly...for less than a week. I still do not know how I have managed to break it because I have most certainly not touched any of my gems but today as I've tried to run jekyll serve this popped up.

```bash
Could not find 'listen' (~ 3.0) among 55 total gem(s) (Gem::MissingSpecError)
```

After a quick `$ gem install listen` we have moved on to the next error message.

```bash
Dependency Error: Yikes! It looks like you don't have jekyll-watch or one of its dependencies installed.
In order to use Jekyll as currently configured, you'll need to install this gem.
The full error message from Ruby is: 'cannot load such file --ruby_dep/warning'
```

Clue some furious googling and here is what worked for me:
Problem wasn't the missing jekyll-watch gem but what you see further in the Ruby error message: ruby_dep was missing.

1, Confirm that it's missing by listing all your gems:
`$ bundle show`

2, Try to install it with: `$ bundle install`

If you still cannot see it on the list of installed bundles continue.

3, delete gemfile.lock

4, Install bundles again: `$ bundle install`
