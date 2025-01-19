---
layout: default
title: All Posts
permalink: /posts/
---

# All Posts
{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
