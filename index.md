---
layout: home
author_profile: true
classes:
  - landing
  - dark-theme
---

{% include figure image_path="/assets/images/balbino.jpg" alt="Balbino Tchoutzine" class="profile-img" %}

# Hello! Je suis **Balbino Tchoutzine**

Étudiant en Génie Informatique passionné par l'Intelligence Artificielle et le Traitement du Langage Naturel. Je m'intéresse particulièrement à l'application de ces technologies dans le contexte africain.

## Domaines d'expertise

- 🤖 Intelligence Artificielle
- 🔤 Traitement du Langage Naturel (NLP)
- 💻 Développement Web
- 📊 Machine Learning

## Projets récents

{% assign projects = site.projects | sort: 'date' | reverse | limit: 3 %}
<div class="grid__wrapper">
  {% for project in projects %}
    {% include project-card.html %}
  {% endfor %}
</div>

## Derniers articles

{% assign posts = site.posts | sort: 'date' | reverse | limit: 3 %}
<div class="grid__wrapper">
  {% for post in posts %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

[Voir tous les articles](/articles/){: .btn .btn--primary}
[Voir tous les projets](/projects/){: .btn .btn--info}