---
title: Recent Attacks
layout: page
permalink: /recent-attacks/
icon: fas fa-bolt
order: 4
---

Actionable analysis of recent incidents: supply chain abuse, crypto-related attacks, exploitable CVEs, and ransomware playbooks.

{% assign recent_posts = site.posts | where_exp: "post", "post.categories contains 'recent-attacks'" %}

{% if recent_posts.size > 0 %}
## Latest Recent Attacks Posts

{% for post in recent_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
No posts yet. Add your first rapid attack brief in `_posts`.
{% endif %}

