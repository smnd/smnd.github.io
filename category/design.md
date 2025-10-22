---
title: Design
layout: default
nav_order: 4
parent: Blog
category: design
---

{% assign posts = site.posts | where_exp: "p", "p.categories contains page.category" | sort: 'date' | reverse %}
{% for post in posts %}
## [{{ post.title }}]({{ post.url }}) 
<!-- — {{ post.date | date: "%b %d, %Y"}} -->
{{post.summary}}
{% endfor %}