---
layout: default
title: Organizers
description: "Organizing committee for AIRS 2026."
---

<section class="page-hero">
  <div class="container page-hero-inner">
    <p class="eyebrow">Organizing Committee</p>
    <h1>AIRS 2026 Organizers</h1>
    <p>The organizers bring expertise in distributed systems, ML infrastructure, cloud and high-performance computing, LLM agents, trustworthy AI, security, and privacy.</p>
  </div>
</section>

<section class="content">
  {% for person in site.data.organizers %}
  <article class="card organizer-profile">
    <div class="avatar">
      {% if person.photo %}
      <img src="{{ person.photo }}" alt="{{ person.name }}">
      {% else %}
      <span>{{ person.initials }}</span>
      {% endif %}
    </div>
    <div>
      <div class="role">{{ person.role }}</div>
      <h2>{{ person.name }}</h2>
      <p><strong>{{ person.affiliation }}</strong>{% if person.location %}<br>{{ person.location }}{% endif %}</p>
      {% if person.email %}
      <p>Email: <a href="mailto:{{ person.email }}">{{ person.email }}</a></p>
      {% endif %}
      {% if person.homepage %}
      <p>Homepage: <a href="{{ person.homepage }}">{{ person.homepage }}</a></p>
      {% endif %}
      <p>{{ person.bio }}</p>
    </div>
  </article>
  {% unless forloop.last %}<br>{% endunless %}
  {% endfor %}

  <h2>Main Contact</h2>
  <p>Qinbin Li, Huazhong University of Science and Technology. Email: <a href="mailto:qinbin@hust.edu.cn">qinbin@hust.edu.cn</a>.</p>
</section>
