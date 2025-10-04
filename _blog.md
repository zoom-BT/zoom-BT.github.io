---
layout: collection
title: "Blog"
permalink: /blog/
collection: posts
entries_layout: grid
classes: wide
author_profile: true
---

# 📚 Articles & Retours d'Expérience

## Articles Récents

<div class="posts-grid">
{% assign recent_posts = site.posts | sort: 'date' | reverse | limit: 3 %}
{% for post in recent_posts %}
  <div class="post-card">
    {% if post.header.teaser %}
      <img src="{{ post.header.teaser }}" alt="{{ post.title }}">
    {% endif %}
    <div class="post-content">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-meta">
        <time>{{ post.date | date: "%d/%m/%Y" }}</time>
        {% if post.categories %}
          • {{ post.categories | join: ', ' }}
        {% endif %}
      </p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ post.url }}" class="read-more">Lire la suite →</a>
    </div>
  </div>
{% endfor %}
</div>

## Catégories

<div class="categories-list">
{% for category in site.categories %}
  <a href="/categories/{{ category[0] | slugify }}" class="category-tag">
    {{ category[0] }} ({{ category[1].size }})
  </a>
{% endfor %}
</div>

## Tous les Articles

<div class="posts-grid">
{% for post in site.posts %}
  <div class="post-card">
    <div class="post-content">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-meta">
        <time>{{ post.date | date: "%d/%m/%Y" }}</time>
        {% if post.categories %}
          • {{ post.categories | join: ', ' }}
        {% endif %}
      </p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </div>
  </div>
{% endfor %}
</div>