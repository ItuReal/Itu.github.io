---
title: Labs
layout: page
permalink: /labs/
icon: fas fa-flask
order: 5
---

Certification notes and lab writeups with practical detection and response takeaways.

{% assign lab_posts = site.posts | where_exp: "post", "post.categories contains 'labs'" %}

{% if lab_posts.size > 0 %}
## Latest Lab Writeups

{% for post in lab_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
No posts yet. Add your first lab walkthrough in `_posts`.
{% endif %}

