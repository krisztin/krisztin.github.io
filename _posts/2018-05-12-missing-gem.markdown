---
layout: post
title:  The Quest for a Missing Ruby Gem
date:   2018-05-12 14:00:06 +0100
category: learn
tags: ruby jekyll
---

My Jekyll environment was running smoothly...for less than a week. I still do not know how I have managed to break it because I have most certainly not touched any of my gems but today as I've tried to run jekyll serve this popped up.

![First error message: Could not find 'listen' among gem(s)]({{ site.url }}/assets/img/nogem01.png)

After a quick
{% highlight shell_session %} $ gem install listen {% endhighlight %}
we have moved on to the next error message.

![Second error message: Cannot load such file -- ruby_dep/warning]({{ site.url }}/assets/img/nogem02.png)

Clue some furious googling and here is what worked for me:
Problem wasn't the missing jekyll-watch gem but what you see further in the Ruby error message: ruby_dep was missing.

1, Confirm that it's missing:
{% highlight shell_session %}$ bundle show{% endhighlight %}

2, Try to install it with
{% highlight shell_session %}$ bundle install{% endhighlight %}
If you still cannot see it on the list of installed bundles continue.

3, delete gemfile.lock

4, Install bundles again
{% highlight shell_session %}$ bundle install{% endhighlight %}