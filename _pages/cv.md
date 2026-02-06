---
layout: default
title: "CV"
permalink: /cv/
---

{% assign profile = site.data.profile %}

<section class="section section--hero">
  <div class="section__header">
    <h1>Curriculum Vitae</h1>
    <p class="lead">Download the full CV or browse the highlights below.</p>
    <a class="button button--primary" href="{{ profile.cv_link }}">Download CV (PDF)</a>
  </div>
</section>

<section class="section">
  <div class="split">
    <div>
      <h2>Appointments</h2>
      <ul class="check-list">
        <li>TODO: Current position, institution, dates.</li>
        <li>TODO: Previous position, institution, dates.</li>
      </ul>
    </div>
    <div>
      <h2>Education</h2>
      <ul class="check-list">
        <li>TODO: Degree, institution, year.</li>
        <li>TODO: Degree, institution, year.</li>
      </ul>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="split">
    <div>
      <h2>Selected Awards</h2>
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
