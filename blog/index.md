---
layout: page
title: Blog
---

<div class="wrapper">
{%- for post in site.posts -%}
    <article class="blog-listing">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <h3><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
        <p>
            <span class="post-tags">
            {% if post %}
                {% assign tags = post.tags %}
            {% endif %}
            {% for tag in tags %}
            <a href="{{site.baseurl}}/tags/#{{tag|slugize}}" class="post-tag">{{tag}}</a>
            {% unless forloop.last %}&nbsp;{% endunless %}
            {% endfor %}
            </span>
        </p>
        {{ post.excerpt }}
    </article>
{% endfor %}
</div>