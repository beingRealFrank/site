---
title: beingRealFrank - Useful Posts
permalink: /useful/
---

## <span style="border-bottom: 1px dashed;">Useful Posts</span>
{% assign posts_by_date = site.posts | where: "categories", "Useful" | group_by_exp: "post", "post.date" %}
{% if posts_by_date.size == 0 %}
Nothing to see here.
{% else %}
{% for date in posts_by_date %}
### {{ date.name | date: "%B %d, %Y" }}
{% for post in date.items %}
- [{{ post.title }}]({{ post.url | relative_url }})
{{ post.excerpt }}[(read more)]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}
{% endif %}