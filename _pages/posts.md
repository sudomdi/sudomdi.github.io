---
layout: single
author_profile: true
title: Posts
permalink: /posts
---

<ul>
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    <h3>{{ currentdate }}</h3>
    {% assign date = currentdate %} 
  {% endif %}
    <a href="{{ post.url }}">{{ post.title }}</a>
    <br>
{% endfor %}
</ul>