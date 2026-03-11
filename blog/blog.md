---
layout: page
title: Blog
permalink: /blog/blog/
---

# Blog

<ul>
{% for post in site.posts %}
<li>
<a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ul>