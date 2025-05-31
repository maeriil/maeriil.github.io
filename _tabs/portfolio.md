---
layout: page
title: Portfolio
permalink: /portfolio/
icon: fas fa-briefcase
order: 5
---

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "portfolio" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
