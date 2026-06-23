# AIRS 2026 Workshop Website

This directory contains the Jekyll/GitHub Pages website for AIRS 2026:

**Agentic AI in Real-World Systems: Infrastructure, Algorithms, and Deployment**

The site is intended as a previewable website for a proposed ICPP 2026 half-day workshop. The wording is deliberately conservative: it does not say the workshop has been accepted, does not claim confirmed invited speakers, does not list a Program Committee, and does not invent submission-system details.

## Local Preview

The working conda environment is `homework`.

```bash
cd "/home/gujing/code/sys26workshop/icpp-workshop/ICPP workshop/website"
conda activate homework
bundle exec jekyll serve --host 0.0.0.0 --port 4000
```

Open one of:

```text
http://127.0.0.1:4000/
http://<WSL-IP>:4000/
```

If Windows cannot open `127.0.0.1`, get the WSL IP with:

```bash
hostname -I | awk '{print $1}'
```

The static build command is:

```bash
bundle exec jekyll build
```

The generated site is written to `_site/`, which is ignored by `.gitignore`.

## Reference Sites

The website structure and wording were based on these references:

- ICPP 2026 official homepage: conference name, location, and main conference dates.
  https://icpp2026.github.io/
- ICPP 2026 Call for Workshops: expected workshop proposal components, half-day/full-day format, invited talks, peer-reviewed papers, panel discussion, review process, and workshop website expectation.
  https://icpp2026.github.io/call-for-workshops/
- ICPP 2026 Workshops page: current accepted-workshop status and style of linking to workshop websites.
  https://icpp2026.github.io/workshops/
- DC4AI 2026 workshop website: an accepted ICPP 2026 workshop page used for comparison of common sections such as topics, submission, dates, organizers, invited speaker, and tentative agenda.
  https://hpc-and-ai.github.io/DC4AI-2026/
- SUSTAIN-HPC 2026 workshop website: accepted ICPP 2026 workshop page with a compact single-column academic layout, simple dates table, and concise organizer/contact information.
  https://icpp2026.github.io/sustain-hpc-2026/
- BID 2026 workshop website: accepted ICPP 2026 workshop page with a direct text-first structure for scope, submission, schedule, and committees.
  https://parallel.computer/
- ICPP 2025 workshops page: examples of ICPP workshop summaries and topic positioning.
  https://icpp2025.sdsc.edu/program/workshops
- AI4Dev ICPP 2025 workshop website: example of a compact academic workshop site with aims/scope, CFP, important dates, agenda, and committee sections.
  https://ornl.github.io/events/AI4Dev-ICPP-2025/

The visual design is not a direct clone of any one site. It now follows a restrained academic workshop pattern: top navigation, compact title area, status note, single-column sections, ordinary lists, simple tables, submission guidance, tentative program, and organizers.

## Page-by-Page Review Guide

### `index.md` - Home

Purpose: first landing page for the workshop.

Main content:

- Full-width hero section with `AIRS 2026`, full workshop title, half-day ICPP 2026 positioning, and small navigation buttons.
- Location shown as Singapore.
- Workshop date shown as September 28, 2026.
- Formal status notice saying AIRS 2026 is a proposed workshop.
- Overview of why agentic AI deployment creates systems challenges.
- Core claim that AIRS treats agentic AI as a first-class distributed systems workload.
- Workshop focus section covering infrastructure and systems, algorithms for agents, and real-world deployment.
- Important dates preview from `_data/dates.yml`.
- Workshop format preview: invited talks, peer-reviewed paper presentations, lightning talks/posters/demos, and panel discussion.
- Topics preview from `_data/topics.yml`.
- Organizer list from `_data/organizers.yml`.

Review points:

- Check whether the status notice is appropriately cautious.
- Check whether the systems emphasis is strong enough.
- Keep paper-deadline placeholders until the submission schedule is confirmed.

### `call-for-papers.md` - Call for Papers

Purpose: tentative CFP page.

Main content:

- CFP status notice.
- Motivation for agentic AI as a systems/infrastructure/deployment topic, including dynamic distributed task-graph workloads.
- Scope statement emphasizing ICPP relevance.
- Full topics list from `_data/topics.yml`.
- Tentative submission categories:
  - Regular research papers
  - Short, work-in-progress, and vision papers
- Submission instructions, including ACM Primary Article Template guidance and tentative LaTeX `acmart` proceedings format.
- Important dates from `_data/dates.yml`.
- Review process description.
- Conflict-of-interest and topic-fit wording for reviewer assignment.
- Publication policy:
  `Accepted papers are expected to appear as workshop papers in the ACM ICPP 2026 Workshops Proceedings, subject to the final requirements of ICPP 2026 and ACM.`

Review points:

- Confirm whether the paper types are acceptable.
- Replace submission-link placeholders only when a submission system is confirmed.
- Confirm final page limits and anonymity settings against official ICPP workshop instructions.
- Do not add a Program Committee list until explicitly confirmed.
- Keep the ACM proceedings wording aligned with the official ICPP 2026 workshop publication policy.

### `program.md` - Program

Purpose: tentative half-day schedule page.

Main content:

- Status notice saying the schedule is tentative, speaker participation / accepted papers are not finalized, and the final schedule is subject to ICPP 2026 workshop scheduling and room arrangements.
- Half-day structure:
  - Opening Remarks - 10 min
  - Tentative Invited Talk 1 - 30 min
  - Tentative Invited Talk 2 - 30 min
  - Peer-reviewed Paper Presentations and Lightning Talks - 90 min
  - Coffee Break - 15 min
  - Panel Discussion - 45 min
  - Closing Remarks - 10 min
- Invited speaker placeholder sentence from `_data/speakers.yml`.
- Accepted papers placeholder.

Review points:

- Check whether the half-day duration feels realistic.
- Add actual speakers only after confirmation.
- Add accepted papers only after review decisions.

### `organizers.md` - Organizers

Purpose: organizer profile page.

Main content:

- Organizer intro paragraph.
- One text profile entry per organizer from `_data/organizers.yml`.
- No organizer avatars or card layout are used in the current restrained design.
- Contact email for workshop inquiries.

Organizer list:

- Qinbin Li - Huazhong University of Science and Technology
- Jialin Li - National University of Singapore
- Wei Dong - Nanyang Technological University
- Chaoyi Ruan - National University of Singapore
- Jing Gu - Huazhong University of Science and Technology

Review points:

- Check affiliations and emails.
- Bios are intentionally short and should not copy long proposal bios verbatim.
- Add phone/postal address only if desired for public website use.
- Add photos only from confirmed official profile sources, and leave `photo` empty otherwise.

## Data Files

### `_data/dates.yml`

Controls dates shown on the Home and CFP pages.

Current values include confirmed/tentative workshop timing and placeholders for paper deadlines:

- Paper submission deadline
- Author notification
- Camera-ready deadline
- Workshop date: September 28, 2026

Do not add the already-passed workshop proposal deadline.

### `_data/topics.yml`

Controls the systems-oriented topics list.

The topics mirror the 7-topic CFP list in the current workshop proposal:

- infrastructure, orchestration, and distributed runtime systems
- LLM serving, inference backends, memory/state management, and accelerator-aware execution
- scheduling, placement, resource management, and workflow execution
- communication, coordination, tool invocation, and secure execution environments
- systems-oriented planning, scheduling, adaptation, and reliability-aware runtime decisions
- benchmarking, workload characterization, and performance-cost-quality evaluation
- trustworthy, private, and secure deployment case studies

### `_data/organizers.yml`

Controls organizer lists on Home and Organizers pages.

Fields used:

- `name`
- `initials`
- `affiliation`
- `role`
- `email`
- `homepage`
- `photo`
- `location`
- `bio`

Photo fields are currently unused. Keep them empty unless the design intentionally adds official organizer photos later.

### `_data/speakers.yml`

Controls the invited-speaker placeholder on Program.

Current content is a conservative placeholder:

```yaml
message: "Invited speakers will be announced after confirmation."
```

Only add named speakers after deciding whether they should be listed as potential or confirmed, and update the Program page rendering accordingly if needed.

## Layout and Styling Files

- `_layouts/default.html`: base HTML shell.
- `_includes/header.html`: site header and brand.
- `_includes/nav.html`: top navigation.
- `_includes/footer.html`: footer with title, venue, and status note.
- `assets/css/custom.css`: all custom styling.
- `assets/img/airs-systems-stack.png`: retained local systems-focus visual asset, not currently used by the restrained academic layout.

## Wording Constraints

Keep these constraints unless the workshop status changes:

- Do not say AIRS has been accepted.
- Do not say speakers are confirmed unless confirmed.
- Do not list a Program Committee.
- Do not include the expired proposal deadline as an active date.
- Keep the ACM proceedings wording subject to the final ICPP 2026 and ACM publication policy.
- Do not invent submission system details.
- Do not invent public website URLs.
- Do not add organizer photos unless their source is confirmed and official.
- Keep the emphasis on systems, infrastructure, and deployment rather than generic AI-agent applications.

## GitHub Pages Deployment

To deploy with GitHub Pages, push the repository to GitHub and enable Pages in repository settings. If the website directory is not the repository root, either move the website contents to the root, use a `docs/` directory, or configure a GitHub Actions workflow to build from `website/` and deploy the generated `_site/` directory.

Do not assume a final repository name or public URL until the hosting location is confirmed.
