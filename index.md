---
layout: default
title: "Home"
permalink: /
---

{% assign profile = site.data.profile %}

<section class="hero">
  <div class="hero__content">
    <p class="hero__eyebrow">Academic Research Portfolio</p>
    <h1 class="hero__title">{{ profile.name }}</h1>
    <p class="hero__subtitle">{{ profile.role }} · {{ profile.affiliation }}</p>
    <p class="hero__summary">{{ profile.hero_summary }}</p>
    <div class="hero__actions">
      <a class="button button--primary" href="{{ '/cv/' | relative_url }}">View CV</a>
      <a class="button button--outline" href="{{ '/contact/' | relative_url }}">Get in touch</a>
    </div>
  </div>
  <div class="hero__panel" aria-label="Research profile highlight">
    <div class="hero__panel-item">
      <h2>Research Focus</h2>
      <ul class="pill-list">
        {% for interest in profile.research_interests %}
        <li>{{ interest }}</li>
        {% endfor %}
      </ul>
    </div>
    <div class="hero__panel-item">
      <h2>Affiliations</h2>
      <ul class="icon-list">
        {% for affiliation in profile.affiliations %}
        <li>{{ affiliation }}</li>
        {% endfor %}
      </ul>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2>Research Snapshot</h2>
    <p>Current themes and project directions. Add or adjust items in <code>_pages/research.md</code>.</p>
  </div>
  <div class="card-grid">
    <article class="card">
      <h3>Project Cluster A</h3>
      <p>TODO: Summarize a flagship research stream and its open questions.</p>
    </article>
    <article class="card">
      <h3>Project Cluster B</h3>
      <p>TODO: Describe a complementary line of inquiry or dataset.</p>
    </article>
    <article class="card">
      <h3>Policy + Practice</h3>
      <p>TODO: Highlight how the research informs policy, industry, or public debates.</p>
    </article>
  </div>
</section>

<section class="section section--alt">
  <div class="section__header">
    <h2>Recent News</h2>
    <a class="text-link" href="{{ '/news/' | relative_url }}">All updates →</a>
  </div>
  <div class="timeline">
    {% for item in site.data.news %}
    <article class="timeline__item">
      <div class="timeline__date">{{ item.date | date: "%b %d, %Y" }}</div>
      <div class="timeline__content">
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
        {% if item.link and item.link != "" %}
        <a class="text-link" href="{{ item.link }}">Learn more</a>
        {% endif %}
      </div>
    </article>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2>Selected Publications</h2>
    <a class="text-link" href="{{ '/publications/' | relative_url }}">Full list →</a>
  </div>
  <div class="list-grid">
    {% for pub in site.data.publications limit:3 %}
    <article class="list-card">
      <p class="list-card__meta">{{ pub.type }} · {{ pub.year }}</p>
      <h3>{{ pub.title }}</h3>
      <p class="list-card__authors">{{ pub.authors }}</p>
      <p class="list-card__venue">{{ pub.venue }}</p>
    </article>
    {% endfor %}
  </div>
</section>

<section class="section section--cta">
  <div>
    <h2>Connect or collaborate</h2>
    <p>Open to research partnerships, invited talks, and graduate supervision opportunities.</p>
  </div>
  <a class="button button--primary" href="{{ '/contact/' | relative_url }}">Contact details</a>
</section>
