---
layout: page
title: Blog
permalink: /siteb/blog/
---

{% assign current_year = "" %}

{% for post in site.posts %}
  {% assign post_year = post.date | date: "%Y" %}

  {% if post_year != current_year %}
    {% if current_year != "" %}
      </ul>
    {% endif %}

    <h2>{{ post_year }}</h2>
    <ul>
    {% assign current_year = post_year %}
  {% endif %}

  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <small>({{ post.date | date: "%B" }})</small>
  </li>
{% endfor %}

</ul>

