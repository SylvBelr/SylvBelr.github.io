---
layout: default
title: "News"
permalink: /news/
---

<section class="section section--hero">
  <div class="section__header">
    <h1>News &amp; Updates</h1>
    <p class="lead">Recent announcements, talks, grants, and media coverage.</p>
  </div>
</section>

<section class="section">
  <div class="timeline">
    {% for item in site.data.news %}
    <article class="timeline__item">
      <div class="timeline__date">{{ item.date | date: "%B %d, %Y" }}</div>
      <div class="timeline__content">
        <h2>{{ item.title }}</h2>
        <p>{{ item.description }}</p>
        {% if item.link and item.link != "" %}
        <a class="text-link" href="{{ item.link }}">Read more</a>
        {% endif %}
      </div>
    </article>
    {% endfor %}
  </div>
</section>
