---
layout: page
menu: true
date: 2024-03-01 15:18:36
title: Categories
permalink: /categories/
---
<h1>{{ page.title }}</h1>

<div class="categories-cards">
{% for category in site.categories %}
  <div class="category-card" style="background-image: url('https://source.unsplash.com/random/300x200?{{ category | first | slugify }}');">
    <a href="/category/{{ category | first | slugify }}">
      <h2>{{ category | first }}</h2>
    </a>
  </div>
{% endfor %}
</div>

<style>
.categories-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.category-card {
  width: 300px; /* Match Unsplash image width */
  height: 200px; /* Match Unsplash image height */
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10px; /* Optional: for rounded corners */
  box-shadow: 0 4px 6px rgba(0,0,0,0.1); /* Optional: for shadow effect */
}

.category-card h2 {
  color: white;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.5); /* Optional: to make text more readable over the image */
  margin: 0;
  padding: 10px;
  background: rgba(0,0,0,0.5); /* Optional: background behind text for readability */
  border-radius: 5px; /* Optional: if background behind text is used */
}
</style>
