---
layout: page
title: Blog
permalink: /siteb/blog/
---

{% assign current_year = "" %}

{% for post in site.posts %}
  {% assign post_year = post.date | date: "%Y" %}

  {% if post_year != current_year %}
    <h2>{{ post_year }}</h2>
    {% assign current_year = post_year %}
  {% endif %}

  <div>
  <span>{{ post.date | date: "%B" }}</span>
  <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
</div>
{% endfor %}

