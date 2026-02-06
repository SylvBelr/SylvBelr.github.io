---
layout: default
title: "Contact"
permalink: /contact/
---

{% assign profile = site.data.profile %}

<section class="section section--hero">
  <div class="section__header">
    <h1>Contact</h1>
    <p class="lead">For collaborations, invited talks, or student supervision, please reach out.</p>
  </div>
</section>

<section class="section">
  <div class="contact-grid">
    <div class="contact-card">
      <h2>Email</h2>
      <p><a href="mailto:{{ profile.email }}">{{ profile.email }}</a></p>
    </div>
    <div class="contact-card">
      <h2>Office</h2>
      <p>{{ profile.contact.office }}</p>
    </div>
    <div class="contact-card">
      <h2>Phone</h2>
      <p>{{ profile.contact.phone }}</p>
    </div>
    <div class="contact-card">
      <h2>Availability</h2>
      <p>{{ profile.contact.availability }}</p>
    </div>
  </div>
</section>
