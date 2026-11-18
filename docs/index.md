---
layout: default
title: Home
---

<section class="hero">
  <h1>Germinate Documentation</h1>
  <p>Explore guides, data schemas, and workflows for managing plant genetic resources, phenotypic trials, and genotypic datasets.</p>
</section>

<h2>Core Functionality</h2>
<div class="card-grid">
  {% for item in site.nav_pages %}
    <a href="{{ item.url | relative_url }}" class="card">
      <h3>{{ item.title }}</h3>
      <p>{{ item.description }}</p>
    </a>
  {% endfor %}
</div>
