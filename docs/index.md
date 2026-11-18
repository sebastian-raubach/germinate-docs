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


{% if site.funders %}
<section class="funders-section">
  <h2>Funders & Partners</h2>
  <div class="funder-grid">
    {% for funder in site.funders %}
      <a href="{{ funder.url }}" target="_blank" rel="noopener" class="funder-item" title="{{ funder.name }}">
        <img src="{{ funder.logo | relative_url }}" alt="{{ funder.name }}">
      </a>
    {% endfor %}
  </div>
</section>
{% endif %}