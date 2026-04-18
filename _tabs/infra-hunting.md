---
title: Infra Hunting
layout: page
permalink: /infra-hunting/
icon: fas fa-network-wired
order: 2
---

Focused notes on attacker infrastructure patterns, pivoting workflows, and clustering methods.

{% assign infra_posts = site.posts | where_exp: "post", "post.categories contains 'infra-hunting'" %}

{% if infra_posts.size > 0 %}
## Latest Infra Hunting Posts

{% for post in infra_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
No posts yet. Add your first infra hunting writeup in `_posts`.
{% endif %}

