---
title: Thoughts
layout: default
nav_order: 2
---

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts %}
{{post.content}}
[{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%b %d, %Y" }}
{% endfor %}