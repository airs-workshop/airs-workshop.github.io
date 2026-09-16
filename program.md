---
layout: default
title: Program
description: "AIRS 2026 half-day workshop program."
---

<section class="subpage-hero" aria-label="Program">
  <img src="{{ '/imgs/fenpi.png' | relative_url }}" alt="Singapore skyline for AIRS 2026">
  <div class="subpage-hero-inner">
    <p class="kicker">AIRS 2026 Program</p>
    <h1>Workshop Program</h1>
    <p class="subtitle">Agentic AI in Real-World Systems: Infrastructure, Algorithms, and Deployment</p>
    <p class="meta-line">September 28, 2026 &middot; Singapore</p>
  </div>
</section>

<section class="content-section">
  <h2>Schedule</h2>
  <table>
    <thead>
      <tr>
        <th>Time</th>
        <th>Program</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">13:30&ndash;15:00</th>
        <td><strong>Keynote Session</strong></td>
      </tr>
      {% for speaker in site.data.speakers %}
      <tr>
        <th scope="row">{{ speaker.time }}</th>
        <td><strong>Keynote {{ speaker.number }}:</strong> {{ speaker.name }}, {{ speaker.title }}, {{ speaker.affiliation }} ({{ speaker.abbreviation }})</td>
      </tr>
      {% endfor %}
      <tr>
        <th scope="row">15:00&ndash;15:30</th>
        <td><strong>Coffee Break</strong></td>
      </tr>
      <tr>
        <th scope="row">15:30&ndash;16:45</th>
        <td><strong>Accepted Paper Presentations</strong></td>
      </tr>
      <tr>
        <th scope="row">15:30&ndash;15:55</th>
        <td>How Far Are We From True Auto-Research?</td>
      </tr>
      <tr>
        <th scope="row">15:55&ndash;16:20</th>
        <td>Trace: Optimizing Long-Context Agents via Task-Adaptive Information Extraction</td>
      </tr>
      <tr>
        <th scope="row">16:20&ndash;16:45</th>
        <td>From Rigid to Dynamic: Entropy-Guided Adaptive Inference for Long-Context LLMs</td>
      </tr>
      <tr>
        <th scope="row">16:45&ndash;16:50</th>
        <td><strong>Closing Remarks</strong></td>
      </tr>
    </tbody>
  </table>
</section>
