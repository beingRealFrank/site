---
title: Welcome
---

# Personal Posts
{% for post in site.posts %}
{% if post.tags contains "personal" %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endif %}
{% endfor %}

# Professional Posts
{% for post in site.posts %}
{% if post.tags contains "professional" %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}
