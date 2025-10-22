---
title: Blog
layout: default
nav_order: 2
---

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts %}
## [{{ post.title }}]({{ post.url }}) 
{{post.summary}}
<!-- — {{ post.date | date: "%b %d, %Y"}} -->
{% endfor %}