---
layout: default
title: Call for Papers
description: "Call for papers for AIRS 2026."
---

<section class="subpage-hero" aria-label="Call for Papers">
  <img src="{{ '/imgs/fenpi.png' | relative_url }}" alt="Singapore skyline for AIRS 2026">
  <div class="subpage-hero-inner">
    <p class="kicker">AIRS 2026</p>
    <h1>Call for Papers</h1>
  </div>
</section>

<section class="content-section">
  <div class="notice">
    <strong>Status:</strong> This call is tentative. Final submission instructions and paper deadlines will be announced after confirmation with the ICPP 2026 workshop chairs.
  </div>

  <h2>AIRS 2026 Call for Papers</h2>
  <p>AIRS 2026, the workshop on <strong>Agentic AI in Real-World Systems: Infrastructure, Algorithms, and Deployment</strong>, invites research papers, short papers, work-in-progress papers, and vision papers on systems, infrastructure, algorithms, and deployment for agentic AI. AIRS 2026 is planned as a non-archival workshop, and accepted submissions will be presented for discussion and feedback rather than published in formal proceedings. The workshop is proposed as a half-day event held in conjunction with <a href="https://icpp2026.github.io/">ICPP 2026</a> in Singapore.</p>

  <p>Agentic AI systems increasingly execute long-running workflows, invoke external tools, coordinate across services, and operate under latency, cost, reliability, privacy, and safety constraints. These workloads create new research questions for parallel and distributed computing: how should agents be scheduled, isolated, monitored, scaled, evaluated, and deployed when their behavior depends on model inference, retrieval, memory, tool execution, dynamic control flow, and external side effects?</p>

  <p>The workshop welcomes algorithmic contributions when they support scalable, reliable, efficient, secure, observable, or trustworthy deployed systems.</p>

  <h2>Topics of Interest</h2>
  <p>Topics of interest include, but are not limited to:</p>
  <ul>
    {% for topic in site.data.topics %}
    <li>{{ topic }}</li>
    {% endfor %}
  </ul>

  <h2>Submission Categories</h2>
  <ul>
    <li><strong>Regular research papers:</strong> tentatively up to 8 pages, excluding references.</li>
    <li><strong>Short, work-in-progress, and vision papers:</strong> tentatively up to 4 pages, excluding references.</li>
  </ul>
  <p>Final page limits and formatting requirements will follow the official ICPP 2026 workshop guidelines.</p>

  <h2>Submission Instructions</h2>
  <p>The submission site will be announced after confirmation with the ICPP 2026 workshop chairs. All submissions should be made electronically in PDF format and should follow the final ICPP 2026 workshop formatting instructions.</p>
  <p>Please use the <a href="https://www.acm.org/publications/proceedings-template">ACM Primary Article Template</a> for submission and review formatting unless the final ICPP 2026 workshop instructions specify otherwise. The use of the ACM template does not imply archival publication. For LaTeX submissions, authors may use <code>\documentclass[sigconf,review]{acmart}</code>; the <code>anonymous</code> option should be used only if required by the final anonymity policy. Authors should not modify template margins, font sizes, or spacing.</p>

  <h2>Review Process</h2>
  <p>Each submission will be peer reviewed by experts in parallel and distributed computing, ML systems, cloud systems, LLM serving, agentic AI infrastructure, and trustworthy AI. Evaluation criteria will include relevance to ICPP, technical quality, novelty, clarity, soundness, quality of evaluation where applicable, and potential to stimulate discussion at the workshop.</p>
  <p>Reviewer assignments will account for conflicts of interest and topic fit, with attention to balancing systems expertise and agentic AI expertise. The anonymity policy will follow the final ICPP 2026 workshop submission instructions.</p>

  <h2>Publication Policy</h2>
  <p>AIRS 2026 is a non-archival workshop. Accepted submissions will not be included in formal proceedings.</p>
  <p>Accepted submissions are intended for presentation, discussion, and community feedback at the workshop. Authors may submit extended or revised versions of their work to archival conferences and journals.</p>
  <p>Final submission and presentation instructions will be confirmed with the ICPP 2026 workshop chairs.</p>

  <h2>Registration and Presentation Policy</h2>
  <p>At least one presenter for each accepted submission must register for ICPP 2026 and present the work at the workshop. All workshop presenters are required to register for the conference; there will be no workshop-only registration rate.</p>

  <h2>Important Dates</h2>
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
