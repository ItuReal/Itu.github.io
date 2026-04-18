---
title: APT Tracking
layout: page
permalink: /apt-tracking/
icon: fas fa-crosshairs
order: 3
---

Campaign-level intelligence tracking with TTP updates, victimology, and operational trends.

{% assign apt_posts = site.posts | where_exp: "post", "post.categories contains 'apt-tracking'" %}

{% if apt_posts.size > 0 %}
## Latest APT Tracking Posts

{% for post in apt_posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
No posts yet. Add your first APT campaign note in `_posts`.
{% endif %}

