---
title: Welcome
---

# Personal Posts by Date
{% assign posts_by_date = site.posts | where: "tags", "personal" | group_by_exp: "post", "post.date" %}
{% for date in posts_by_date %}
## {{ date.name | date: "%B %d, %Y" }}
{% for post in date.items %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}


# Professional Posts
# Personal Posts by Date
{% assign posts_by_date = site.posts | where: "tags", "professional" | group_by_exp: "post", "post.date" %}
{% for date in posts_by_date %}
## {{ date.name | date: "%B %d, %Y" }}
{% for post in date.items %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}