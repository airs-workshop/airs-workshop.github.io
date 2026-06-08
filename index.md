---
layout: default
title: Home
description: "AIRS 2026 proposed ICPP workshop on agentic AI systems infrastructure, algorithms, and deployment."
---

<section class="hero">
  <div class="container hero-inner">
    <div class="hero-copy">
      <p class="eyebrow">Proposed half-day workshop for ICPP 2026</p>
      <h1>AIRS 2026</h1>
      <h2>{{ site.long_title }}</h2>
      <p>{{ site.tagline }}</p>
      <div class="hero-meta-grid" aria-label="Workshop facts">
        <div class="hero-fact">
          <span>Venue</span>
          <strong>{{ site.conference }}</strong>
        </div>
        <div class="hero-fact">
          <span>Location</span>
          <strong>{{ site.location }}</strong>
        </div>
        <div class="hero-fact">
          <span>Date</span>
          <strong>{{ site.workshop_date_short }}</strong>
        </div>
        <div class="hero-fact">
          <span>Format</span>
          <strong>Half-day workshop</strong>
        </div>
      </div>
    </div>
    <aside class="hero-facts" aria-label="Workshop focus">
      <div class="focus-panel">
        <div class="focus-card">
          <span>Workload</span>
          <strong>Dynamic and long-running</strong>
          <p>Agent workflows with changing control flow, tools, memory, and external services.</p>
        </div>
        <div class="focus-card">
          <span>Systems Layer</span>
          <strong>Runtime orchestration</strong>
          <p>Scheduling, placement, state management, sandboxing, serving, and observability.</p>
        </div>
        <div class="focus-card">
          <span>Deployment</span>
          <strong>Reliable and constrained</strong>
          <p>Real resource, latency, cost, reliability, privacy, and security requirements.</p>
        </div>
      </div>
    </aside>
  </div>
</section>

<section class="section tight">
  <div class="container">
    <div class="notice">
      <strong>Status:</strong> AIRS 2026 is a proposed workshop. Final workshop status, date, submission instructions, publication policy, and invited speakers will be announced after confirmation with the ICPP 2026 workshop chairs.
    </div>
  </div>
</section>

<section class="section">
  <div class="container grid two">
    <div class="section-header">
      <h2>Overview</h2>
      <p>Agentic AI is moving from demos and benchmarks into deployed systems that coordinate tools, models, data, and people under real operational constraints.</p>
      <p class="lead-claim">AIRS treats agentic AI as a first-class distributed systems workload: dynamic, stateful, tool-using, long-running, and deployed under real resource, reliability, and security constraints.</p>
    </div>
    <div class="overview-body">
      <p>That transition introduces systems challenges: scalable runtime infrastructure, parallel and distributed execution, orchestration, scheduling, memory and state management, LLM serving, secure tool execution, observability, reliability, and cost-performance tradeoffs.</p>
      <p>AIRS aims to bring together researchers and practitioners from parallel and distributed computing, ML systems, LLM agents, cloud systems, security, and trustworthy AI to define the systems foundations for reliable real-world agentic AI.</p>
      <ul class="pill-list overview-pills">
        <li>Infrastructure</li>
        <li>Runtime algorithms</li>
        <li>Deployment evidence</li>
      </ul>
    </div>
  </div>
</section>

<section class="section">
  <div class="container grid two">
    <div class="card">
      <h3>Important Dates</h3>
      <p class="card-note">Dates will be posted after confirmation with the ICPP 2026 workshop chairs.</p>
      <ul class="date-list">
        {% for item in site.data.dates %}
        <li>
          <span>{{ item.name }}</span>
          <strong>{{ item.date }}</strong>
        </li>
        {% endfor %}
      </ul>
    </div>
    <div class="card format-card">
      <h3>Workshop Format</h3>
      <p class="card-note">The workshop is planned as a compact half-day program with research talks and discussion.</p>
      <ul class="format-preview">
        <li>
          <span>Invited talks</span>
          <strong>Two talks on systems infrastructure and deployment.</strong>
        </li>
        <li>
          <span>Paper session</span>
          <strong>Peer-reviewed regular, short, work-in-progress, and vision papers.</strong>
        </li>
        <li>
          <span>Panel</span>
          <strong>Discussion on the systems roadmap for deployable agentic AI.</strong>
        </li>
        <li>
          <span>Audience</span>
          <strong>Researchers and practitioners across systems, ML infrastructure, and trustworthy AI.</strong>
        </li>
      </ul>
    </div>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-header">
      <h2>Topics</h2>
      <p>AIRS focuses on systems, infrastructure, and deployment for agentic AI.</p>
    </div>
    <ul class="topic-list">
      {% for topic in site.data.topics limit:8 %}
      <li>{{ topic }}</li>
      {% endfor %}
    </ul>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-header">
      <h2>Organizers</h2>
      <p>The organizing committee brings expertise across distributed systems, ML infrastructure, cloud and high-performance computing, LLM agents, trustworthy AI, security, and privacy.</p>
    </div>
    <div class="organizer-grid">
      {% for person in site.data.organizers %}
      <article class="card organizer-card">
        <div class="avatar small">
          {% if person.photo %}
          <img src="{{ person.photo }}" alt="{{ person.name }}">
          {% else %}
          <span>{{ person.initials }}</span>
          {% endif %}
        </div>
        <div class="role">{{ person.role }}</div>
        <h3>{{ person.name }}</h3>
        <p>{{ person.affiliation }}</p>
      </article>
      {% endfor %}
    </div>
  </div>
</section>
