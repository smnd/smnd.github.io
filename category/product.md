---
title: Product
layout: default
nav_order: 3
parent: Blog
category: product
---

{% assign posts = site.posts | where_exp: "p", "p.categories contains page.category" | sort: 'date' | reverse %}
{% for post in posts %}
## [{{ post.title }}]({{ post.url }}) 
<!-- — {{ post.date | date: "%b %d, %Y"}} -->
{{post.summary}}
{% endfor %}