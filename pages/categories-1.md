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
    {% assign slugified_category = category | first | slugify %}
    <!-- Debug: Display the slugified category -->
    <li>Slug: {{ slugified_category }} - <a href="/category/{{ slugified_category }}">{{ category | first }}</a></li>
  {% endfor %}
</ul>