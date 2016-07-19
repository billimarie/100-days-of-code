---
layout: page
title: Day
permalink: /day/
sitemap: false
---

{% assign categories = site.categories | sort %}

<div id="index">

  {% for category in categories %}
    {% assign sorted_posts = site.posts | sort: 'title' %}
    {% for post in sorted_posts %}
      {% if post.categories contains category[0]%}
        <h3><a href="{{ site.github.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
      {%endif%}
    {% endfor %}
  {% endfor %}
</div>
