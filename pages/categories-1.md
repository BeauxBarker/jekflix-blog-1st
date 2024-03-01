---
layout: page
menu: true
date: 2024-03-01 15:18:36
title: Categories
permalink: /categories/
---
<h1>{{ page.title }}</h1>


<ul>
{% for category in site.categories %}
  <li><a href="/category/{{ category | first | slugify }}">{{ category | first }}</a></li>
{% endfor %}
</ul>
