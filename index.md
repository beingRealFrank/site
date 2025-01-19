---
title: Welcome
---

## Personal Posts 
{% assign posts_by_date = site.posts | where: "tags", "personal" | group_by_exp: "post", "post.date" %}
{% if posts_by_date.size == 0 %}
Nothing to see here.
{% else %}
{% for date in posts_by_date %}
### {{ date.name | date: "%B %d, %Y" }}
{% for post in date.items %}
- [{{ post.title }}]({{ post.url | relative_url }})
{{ post.excerpt }}[...(read more)]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}
{% endif %}


## Professional Posts
{% assign posts_by_date = site.posts | where: "tags", "professional" | group_by_exp: "post", "post.date" %}
{% if posts_by_date.size == 0 %}
Nothing to see here.
{% else %}
{% for date in posts_by_date %}
### {{ date.name | date: "%B %d, %Y" }}
{% for post in date.items %}
- [{{ post.title }}]({{ post.url | relative_url }})
{{ post.excerpt }}[...(read more)]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}
{% endif %}