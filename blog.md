---
layout: default
title: Blog
permalink: /blog/
redirect_from: "/blog.html"
---

# Blog

{% for item in site.posts %}
  <h2>{{ item.title }}</h2>
  <em>{{ item.date | date_to_long_string }}</em>

  {{ item.excerpt }}

  <a href="{{ item.url }}">Read more ></a>
{% endfor %}
