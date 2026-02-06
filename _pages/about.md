---
layout: default
title: "About"
permalink: /about/
---

{% assign profile = site.data.profile %}

<section class="section section--hero">
  <div class="section__header">
    <h1>About</h1>
    <p class="lead">{{ profile.long_bio }}</p>
  </div>
</section>

<section class="section">
  <div class="split">
    <div>
      <h2>Affiliations</h2>
      <ul class="icon-list">
        {% for affiliation in profile.affiliations %}
        <li>{{ affiliation }}</li>
        {% endfor %}
      </ul>
    </div>
    <div>
      <h2>Research Interests</h2>
      <ul class="pill-list">
        {% for interest in profile.research_interests %}
        <li>{{ interest }}</li>
        {% endfor %}
      </ul>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="split">
    <div>
      <h2>Awards</h2>
      <ul class="check-list">
        {% for award in profile.awards %}
        <li>{{ award }}</li>
        {% endfor %}
      </ul>
    </div>
    <div>
      <h2>Service</h2>
      <ul class="check-list">
        {% for item in profile.service %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
    </div>
  </div>
</section>
