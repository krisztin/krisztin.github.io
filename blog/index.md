---
layout: page
title: Blog
---

{%- for post in site.posts -%}
    <article class="blog-listing">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
            </a>
        </h3>
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        {{ post.excerpt }}
    </article>
{% endfor %}