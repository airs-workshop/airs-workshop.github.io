---
layout: default
title: Home
description: "AIRS 2026 proposed ICPP workshop on agentic AI systems infrastructure, algorithms, and deployment."
body_class: home-page
---

<section class="home-hero" aria-label="AIRS 2026 workshop overview">
  <img src="{{ '/imgs/fenpi.png' | relative_url }}" alt="Singapore skyline and Marina Bay Sands for ICPP 2026">
  <div class="home-hero-overlay">
    <h1>AIRS 2026</h1>
    <p class="hero-subtitle">{{ site.long_title }}</p>
    <p class="hero-meta">{{ site.hero_meta }}</p>
    <p class="action-row hero-actions">
      <a class="text-button" href="{{ '/call-for-papers/' | relative_url }}">Call for Papers</a>
      <a class="text-button secondary" href="{{ '/program/' | relative_url }}">Program</a>
    </p>
  </div>
</section>

<div class="notice">
  <strong>Status:</strong> AIRS 2026 is a proposed half-day workshop for ICPP 2026. AIRS is planned as a non-archival workshop: accepted submissions will be presented for discussion and feedback and will not be published in formal proceedings. Submission instructions, paper deadlines, and invited speakers will be announced after confirmation with the ICPP 2026 workshop chairs.
</div>

<section class="content-section">
  <h2>About the Workshop</h2>
  <p>Agentic AI is moving from model-level reasoning benchmarks and single-turn LLM applications into deployed systems that coordinate tools, models, data, services, and people under real operational constraints. These systems increasingly combine LLM inference, retrieval, code execution, external APIs, databases, tool sandboxes, multi-agent coordination, and human-in-the-loop workflows.</p>

  <p>AIRS treats agentic AI as a first-class distributed systems workload: dynamic, stateful, tool-using, long-running, and deployed under real resource, reliability, and security constraints. The workshop aims to bring together researchers and practitioners from parallel and distributed computing, ML systems, LLM serving, multi-agent systems, security, and trustworthy AI.</p>
</section>

<section class="content-section">
  <h2>Non-Archival Workshop</h2>
  <p>AIRS 2026 is planned as a non-archival workshop. Accepted submissions will be presented at the workshop for discussion and feedback, but will not be published in formal proceedings. This format is intended to encourage early-stage work, work-in-progress results, vision papers, and open discussion.</p>
</section>

<section class="content-section">
  <h2>Call for Papers</h2>
  <p>AIRS 2026 welcomes regular research papers, short papers, work-in-progress papers, and vision papers on systems, infrastructure, algorithms, and deployment for agentic AI in real-world settings.</p>
  <p><a class="text-button" href="{{ '/call-for-papers/' | relative_url }}">Read the full Call for Papers</a></p>
</section>

<section class="content-section">
  <h2>Workshop Focus</h2>
  <p>The workshop is organized around three connected dimensions:</p>
  <ul>
    <li><strong>Infrastructure and systems:</strong> scalable runtime support, orchestration, state management, secure tool execution, and cloud/edge deployment.</li>
    <li><strong>Algorithms for agents:</strong> planning, scheduling, coordination, adaptation, memory management, and reliability-aware runtime decisions.</li>
    <li><strong>Real-world deployment:</strong> evaluation and operational experience under performance, cost, privacy, safety, and reliability constraints.</li>
  </ul>
</section>

<section class="content-section">
  <h2>Important Dates</h2>
  <p>Submission, notification, and final-version deadlines will be posted after confirmation with the ICPP 2026 workshop chairs.</p>
  <table>
    <tbody>
      {% for item in site.data.dates %}
      <tr>
        <th scope="row">{{ item.name }}</th>
        <td>{{ item.date }}</td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</section>

<section class="content-section">
  <h2>Topics of Interest</h2>
  <p>AIRS welcomes work on systems, infrastructure, algorithms, and deployment for agentic AI in real-world settings. Topics include, but are not limited to:</p>
  <ul>
    {% for topic in site.data.topics %}
    <li>{{ topic }}</li>
    {% endfor %}
  </ul>
</section>

<section class="content-section">
  <h2>Workshop Format</h2>
  <p>AIRS is planned as a compact half-day program with invited talks, peer-reviewed paper presentations, short talks or lightning talks when appropriate, and a panel discussion on the systems roadmap for deployable agentic AI.</p>
  <ul>
    <li>Invited talks on agent systems infrastructure, reliability, security, and deployment.</li>
    <li>Peer-reviewed presentations for accepted research, short, work-in-progress, and vision papers.</li>
    <li>A moderated panel discussion on open systems problems and evaluation gaps.</li>
  </ul>
</section>

<section class="content-section">
  <h2>Organizers</h2>
  <ul class="compact-list">
    {% for person in site.data.organizers %}
    <li><strong>{{ person.name }}</strong>, {{ person.affiliation }}</li>
    {% endfor %}
  </ul>
</section>
