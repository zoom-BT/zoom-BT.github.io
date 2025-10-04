---
layout: collection
title: "Projets"
collection: projects
entries_layout: grid
classes: wide
author_profile: true
sort_by: date
sort_order: reverse
---

## 🚀 Projets Phares

{% assign featured_projects = site.projects | where: "featured", true %}
<div class="projects-grid">
{% for project in featured_projects %}
  <div class="project-card">
    <img src="{{ project.header.image | default: '/assets/images/default-project.jpg' }}" alt="{{ project.title }}">
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p class="project-excerpt">{{ project.excerpt }}</p>
    <div class="project-tags">
      {% for tag in project.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>

## � Tous les Projets

<div class="projects-grid">
{% for project in site.projects %}
  <div class="project-card">
    <img src="{{ project.header.image | default: '/assets/images/default-project.jpg' }}" alt="{{ project.title }}">
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p class="project-excerpt">{{ project.excerpt }}</p>
    <div class="project-tech">
      {% for tech in project.technologies %}
        <span class="tech-tag">{{ tech }}</span>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>