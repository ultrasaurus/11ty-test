---
layout: layout.liquid
title: Welcome to my blog
---

Here are all the posts:

{% for post in collections.blog %}
    <h2><a href="{{ post.url }}">{{ post.data.title }}</a></h2>
    <em>{{ post.date | date: "%Y-%m-%d" }}</em>
{% endfor %}