---
layout: page
title: Blog
permalink: /siteb/blog/
---

<ul>
{% for post in site.posts %}
  <li>
    TITLE: "{{ post.title }}" |
    URL: "{{ post.url }}"
  </li>
{% endfor %}
</ul>

