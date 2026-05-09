---
layout: default
title: About
---

# About Me

This page tells you a little bit about me.

{% for post in site.posts limit:10 %}

<a href="{{ post.url }}">{{ post.title }}</a>

{% endfor %}
