---
layout: default
title: Blog
nav: blog
---

## Blog

{% if site.posts.size > 0 %}
{% for post in site.posts %}
<article class="blog-card">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p class="blog-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
  {% if post.excerpt %}
  <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
  {% endif %}
</article>
{% endfor %}
{% else %}
<p>No posts yet.</p>
{% endif %}

