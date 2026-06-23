---
layout: default
title: Organizers
description: "Organizing committee for AIRS 2026."
---

<section class="subpage-hero" aria-label="Organizing Committee">
  <img src="{{ '/imgs/fenpi.png' | relative_url }}" alt="Singapore skyline for AIRS 2026">
  <div class="subpage-hero-inner">
    <p class="kicker">Organizing Committee</p>
    <h1>AIRS 2026 Organizers</h1>
    <p class="subtitle">Distributed systems, ML infrastructure, privacy, security, and agentic AI systems.</p>
  </div>
</section>

<section class="content-section">
  <ul class="profile-list">
    {% for person in site.data.organizers %}
    <li>
      <h2>{{ person.name }} <span class="profile-separator">&mdash;</span> {{ person.affiliation }}</h2>
      <p>{{ person.bio }}</p>
      {% if person.email %}
      <p class="profile-email"><strong>Email:</strong> <a href="mailto:{{ person.email }}">{{ person.email }}</a></p>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>

<section class="content-section">
  <h2>Contact</h2>
  <p>For workshop inquiries, please contact the organizing team at <a href="mailto:qinbin@hust.edu.cn">qinbin@hust.edu.cn</a>.</p>
</section>
