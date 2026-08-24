---
layout: page
title: Blog
permalink: /siteb/blog/
---

<div class="blog-archive">
{% assign current_year = "" %}

{% for post in site.posts %}
  {% assign post_year = post.date | date: "%Y" %}

  {% if post_year != current_year %}
    <h2>{{ post_year }}</h2>
    {% assign current_year = post_year %}
  {% endif %}

  <p>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <small>{{ post.date | date: "%B" }}</small>
  </p>
{% endfor %}
</div>

