---
title: Welcome
---

# Personal Posts
{% for post in site.posts %}
{% if post.tags contains "personal" %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}

# Professional Posts
{% for post in site.posts %}
{% if post.tags contains "professional" %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}
