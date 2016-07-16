---
layout: page
title: 100 Days of Code
permalink: /
sitemap: false
---

# I'm participating in the #100DaysOfCode challenge.

<br />

<div style="text-align: center; margin: 0 auto;"><img src="https://cloud.githubusercontent.com/assets/6895471/16893000/85e34c0e-4adc-11e6-9dfc-2c359d2a4d05.png" /></div>

<br /><br />

# RECENT POSTS

{% assign categories = site.categories | sort %}

<div id="index">
  {% for category in categories %}
    {% assign sorted_posts = site.posts %}
    {% for post in sorted_posts %}
      {% if post.categories contains category[0]%}
        <h3><a href="{{ site.github.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
        <h4>{{ post.excerpt }}</h4>
      {%endif%}
    {% endfor %}
  {% endfor %}
</div>
