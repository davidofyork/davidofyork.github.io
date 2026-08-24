---
layout: page
title: Blog
permalink: /siteb/blog/
---


<ul>
{% for post in site.posts %}
  <li>
    <strong>{{ post.title }}</strong><br>
    post.url = {{ post.url }}<br>
    site.baseurl = {{ site.baseurl }}<br>
    link = {{ site.baseurl }}{{ post.url }}
  </li>
{% endfor %}
</ul>


<div class="blog-archive">
{% assign current_year = "" %}

{% for post in site.posts %}
  {% assign post_year = post.date | date: "%Y" %}

  {% if post_year != current_year %}
    <h2>{{ post_year }}</h2>
    {% assign current_year = post_year %}
  {% endif %}

  <p>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    <small>{{ post.date | date: "%B" }}</small>
  </p>
{% endfor %}
</div>

