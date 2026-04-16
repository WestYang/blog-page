---
layout: page
title: 归档
permalink: /archive/
---

# 文章归档

{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y年%m月" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2 id="{{ currentdate }}">{{ currentdate }}</h2>
    <ul class="post-list">
    {% assign date = currentdate %}
  {% endif %}
  <li>
    <span class="post-meta">{{ post.date | date: "%d日" }}</span>
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
