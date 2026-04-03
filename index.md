---
layout: single
classes: wide
title: "The People’s Ledger"
author_profile: false
---

<!-- ========================= -->
<!--  PRIMARY FEATURED STORY   -->
<!-- ========================= -->

{% assign primary = site.posts | where: "featured", "primary" | first %}
{% if primary %}
<div class="featured-primary" style="margin-bottom: 3rem;">

  <div style="display: flex; flex-wrap: wrap; gap: 2rem; align-items: flex-start;">
    
    <div style="flex: 1 1 350px; min-width: 300px;">
      <img src="{{ primary.header.image }}" alt="{{ primary.title }}" style="width: 100%; border-radius: 6px;">
    </div>

    <div style="flex: 2 1 400px; min-width: 300px;">
      <h2 style="margin-top: 0;">{{ primary.title }}</h2>
      <p>{{ primary.excerpt }}</p>
      <a href="{{ primary.url }}" class="btn btn--primary">Read Full Story →</a>
    </div>

  </div>
</div>
{% endif %}

---

<!-- ========================= -->
<!--  SECONDARY FEATURED STORIES -->
<!-- ========================= -->

{% assign secondary = site.posts | where: "featured", "secondary" | slice: 0, 2 %}
{% if secondary.size > 0 %}
<div class="secondary-stories" style="display: flex; flex-wrap: wrap; gap: 2rem; margin-bottom: 3rem;">

  {% for story in secondary %}
  <div style="flex: 1 1 300px; min-width: 280px;">

    <img src="{{ story.header.image }}" alt="{{ story.title }}" style="width: 100%; border-radius: 6px; margin-bottom: 1rem;">

    <h3 style="margin-top: 0;">{{ story.title }}</h3>
    <p>{{ story.excerpt }}</p>
    <a href="{{ story.url }}" class="btn btn--small">Read →</a>

  </div>
  {% endfor %}

</div>
{% endif %}

---

<!-- ========================= -->
<!--  SECTION BLOCKS           -->
<!-- ========================= -->

## Ledger File
A structured, evidence‑driven breakdown of a single issue or public decision.

{% assign ledger_post = site.categories.ledger-file | first %}
{% if ledger_post %}
**Latest:** [{{ ledger_post.title }}]({{ ledger_post.url }})
{% endif %}

[Visit Ledger File →](/ledger-file/)

---

## People’s Brief
Short, clear explainers that break down complex issues.

{% assign brief_post = site.categories.peoples-brief | first %}
{% if brief_post %}
**Latest:** [{{ brief_post.title }}]({{ brief_post.url }})
{% endif %}

[Visit People’s Brief →](/peoples-brief/)

---

## Weekly Record
A roundup of key governance, corporate, and economic developments.

{% assign weekly_post = site.categories.weekly-record | first %}
{% if weekly_post %}
**Latest:** [{{ weekly_post.title }}]({{ weekly_post.url }})
{% endif %}

[Visit Weekly Record →](/weekly-record/)

---

## Investigations
Deep, document‑driven reporting on systems, institutions, and public decisions.

{% assign inv_post = site.categories.investigations | first %}
{% if inv_post %}
**Latest:** [{{ inv_post.title }}]({{ inv_post.url }})
{% endif %}

[Visit Investigations →](/investigations/)

---

## Editorials
Considered viewpoints grounded in evidence and written to elevate public understanding.

{% assign ed_post = site.categories.editorials | first %}
{% if ed_post %}
**Latest:** [{{ ed_post.title }}]({{ ed_post.url }})
{% endif %}

[Visit Editorials →](/editorials/)

---

## Projects
Long‑term civic research, data work, and public‑interest initiatives.

{% assign proj_post = site.categories.projects | first %}
{% if proj_post %}
**Latest:** [{{ proj_post.title }}]({{ proj_post.url }})
{% endif %}

[Visit Projects →](/projects/)
