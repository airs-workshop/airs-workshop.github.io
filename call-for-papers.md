---
layout: default
title: Call for Papers
description: "Call for papers for AIRS 2026."
---

<section class="page-hero">
  <div class="container page-hero-inner">
    <p class="eyebrow">Call for Papers</p>
    <h1>AIRS 2026</h1>
    <p>{{ site.long_title }}</p>
  </div>
</section>

<section class="content">
  <div class="notice">
    <strong>Status:</strong> This call is tentative. Final submission instructions, dates, and publication details will be announced after confirmation with the ICPP 2026 workshop chairs.
  </div>

  <h2>Motivation</h2>
  <p>Agentic AI systems increasingly execute long-running workflows, invoke external tools, coordinate across services, and operate under latency, cost, reliability, privacy, and safety constraints. These workloads create new research questions for parallel and distributed computing: how should agents be scheduled, isolated, monitored, scaled, evaluated, and deployed when their behavior depends on model inference, retrieval, memory, tool execution, dynamic control flow, and external side effects?</p>

  <p>Agent workflows often resemble dynamic distributed task graphs with unpredictable control flow, heterogeneous resource demands, and long-lived state. AIRS 2026 invites work that studies agentic AI as a real-world systems problem and connects infrastructure, algorithms, and deployment experience to the ICPP community.</p>

  <h2>Scope</h2>
  <p>The workshop welcomes research on systems, infrastructure, algorithms, and deployment practices for agentic AI. Algorithmic work is in scope when it supports scalable, reliable, efficient, secure, observable, or trustworthy deployed systems.</p>

  <h2>Topics of Interest</h2>
  <ul>
    {% for topic in site.data.topics %}
    <li>{{ topic }}</li>
    {% endfor %}
  </ul>

  <h2>Submission Types</h2>
  <ul>
    <li>Regular research papers</li>
    <li>Short papers</li>
    <li>Work-in-progress papers</li>
    <li>Vision papers</li>
  </ul>

  <h2>Important Dates</h2>
  <div class="table-like">
    {% for item in site.data.dates %}
    <div class="table-row">
      <strong>{{ item.name }}</strong>
      <span>{{ item.date }}</span>
    </div>
    {% endfor %}
  </div>

  <h2>Review Process</h2>
  <p>Each submission will be peer reviewed by experts in parallel and distributed computing, ML systems, cloud systems, LLM serving, agentic AI infrastructure, and trustworthy AI. Evaluation criteria will include relevance to ICPP, technical quality, novelty, clarity, soundness, quality of evaluation where applicable, and potential to stimulate discussion at the workshop. Reviewer assignments will account for conflicts of interest and topic fit, with attention to balancing systems expertise and agentic AI expertise.</p>

  <h2>Publication Note</h2>
  <p>Accepted papers will be presented at the workshop. Publication will follow the official ICPP 2026 workshop proceedings policy and final camera-ready instructions.</p>
</section>
