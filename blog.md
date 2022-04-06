---
layout: default
title: Blog
nav_order: 1000
search_exclude: true
---

# News, updates and events

<ul class="posts">
   {% for post in site.posts %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
   {% endfor %}
</ul>