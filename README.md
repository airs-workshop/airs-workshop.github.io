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
- ICPP 2025 workshops page: examples of ICPP workshop summaries and topic positioning.
  https://icpp2025.sdsc.edu/program/workshops
- AI4Dev ICPP 2025 workshop website: example of a compact academic workshop site with aims/scope, CFP, important dates, agenda, and committee sections.
  https://ornl.github.io/events/AI4Dev-ICPP-2025/

The visual design is not a direct clone of any one site. It uses the common academic workshop pattern of top navigation, hero section, overview, dates, topics, submission guidance, tentative program, and organizers.

## Page-by-Page Review Guide

### `index.md` - Home

Purpose: first landing page for the workshop.

Main content:

- Hero section with `AIRS 2026`, full workshop title, and half-day ICPP 2026 positioning.
- Location shown as Singapore.
- Workshop date shown as a full "to be announced after confirmation" placeholder.
- Formal status notice saying AIRS 2026 is a proposed workshop.
- Overview of why agentic AI deployment creates systems challenges.
- Core claim that AIRS treats agentic AI as a first-class distributed systems workload.
- Dynamic distributed task-graph framing for agent workflows.
- Important dates preview from `_data/dates.yml`.
- Workshop format preview: invited talks, peer-reviewed paper presentations, lightning talks/posters/demos, and panel discussion.
- Topics preview from `_data/topics.yml`.
- Organizer preview from `_data/organizers.yml`.
- Right-side focus cards for the proposal's three pillars: Infrastructure and Systems, Algorithms, and Deployment.

Review points:

- Check whether the status notice is appropriately cautious.
- Check whether the systems emphasis is strong enough.
- Replace date placeholders only after the actual workshop date is confirmed.

### `call-for-papers.md` - Call for Papers

Purpose: tentative CFP page.

Main content:

- CFP status notice.
- Motivation for agentic AI as a systems/infrastructure/deployment topic, including dynamic distributed task-graph workloads.
- Scope statement emphasizing ICPP relevance.
- Full topics list from `_data/topics.yml`.
- Tentative submission types:
  - Regular research papers
  - Short papers
  - Work-in-progress papers
  - Vision papers
- Important dates from `_data/dates.yml`.
- Review process description.
- Conflict-of-interest and topic-fit wording for reviewer assignment.
- Conservative publication note:
  `Accepted papers will be presented at the workshop. Publication will follow the official ICPP 2026 workshop proceedings policy and final camera-ready instructions.`

Review points:

- Confirm whether the paper types are acceptable.
- Confirm whether page limits should be added here or left only on the Submission page.
- Do not add a Program Committee list until explicitly confirmed.
- Do not claim ACM Digital Library publication unless this is officially confirmed for AIRS.

### `submission.md` - Submission

Purpose: placeholder submission-instructions page.

Main content:

- Submission site placeholder: announced after confirmation with the ICPP 2026 workshop chairs.
- Formatting: ACM format / final ICPP 2026 workshop submission instructions.
- Tentative page limits:
  - Regular research papers: up to 8 pages, excluding references.
  - Short papers: up to 4 pages, excluding references.
  - Work-in-progress papers: up to 4 pages, excluding references.
  - Vision papers: up to 4 pages, excluding references.
- Review policy.
- Anonymity policy: follows the final ICPP 2026 workshop submission instructions.
- Publication note aligned with the proposal.
- Note that detailed instructions and link will be announced after confirmation with ICPP 2026 workshop chairs.

Review points:

- Replace submission-link placeholders only when a submission system is confirmed.
- Do not invent EasyChair, CMT, HotCRP, OpenReview, or Linklings unless confirmed.
- Confirm final page limits against official ICPP workshop instructions.

### `program.md` - Program

Purpose: tentative half-day schedule page.

Main content:

- Status notice saying the schedule is tentative and speaker participation / accepted papers are not finalized.
- Half-day structure:
  - Opening Remarks - 10 min
  - Invited Talk 1 - 35 min
  - Invited Talk 2 - 35 min
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
- One organizer profile card per entry from `_data/organizers.yml`.
- Initials avatar fallback for each organizer. Photos are optional and currently not populated.
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

Current values are full placeholder sentences:

- Paper submission deadline
- Author notification
- Camera-ready deadline
- Workshop date

Do not add the already-passed workshop proposal deadline.

### `_data/topics.yml`

Controls the systems-oriented topics list.

The topics emphasize:

- distributed runtime systems and orchestration
- LLM serving and accelerator-aware execution
- scheduling and resource management
- memory, state, and KV-cache management
- communication protocols and coordination mechanisms
- planning, decision-making, adaptation, and reliability-aware runtime decisions
- tool sandboxing
- cloud/edge and heterogeneous deployment
- workload characterization and dynamic task-graph abstractions
- performance-cost-quality evaluation
- reliability, observability, security, privacy, and trustworthy deployment
- real-world deployment case studies

### `_data/organizers.yml`

Controls organizer cards on Home and Organizers pages.

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

Photo policy:

- Leave `photo` empty unless the image comes from a confirmed official source such as an organizer homepage, institution profile, Google Scholar profile, or OpenReview profile.
- Do not use random image-search results or social-media photos.
- Do not download photos into the repository unless source and usage permission are clear.
- If `photo` is empty, the site displays an initials avatar such as `QL`, `JH`, `BH`, `BL`, or `DS`.

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
- `assets/img/airs-systems-stack.png`: retained local systems-focus visual asset, not currently used as the primary hero content.

## Wording Constraints

Keep these constraints unless the workshop status changes:

- Do not say AIRS has been accepted.
- Do not say speakers are confirmed unless confirmed.
- Do not list a Program Committee.
- Do not include the expired proposal deadline as an active date.
- Do not claim ACM Digital Library publication unless confirmed for AIRS.
- Do not invent submission system details.
- Do not invent public website URLs.
- Do not add organizer photos unless their source is confirmed and official.
- Keep the emphasis on systems, infrastructure, and deployment rather than generic AI-agent applications.

## GitHub Pages Deployment

To deploy with GitHub Pages, push the repository to GitHub and enable Pages in repository settings. If the website directory is not the repository root, either move the website contents to the root, use a `docs/` directory, or configure a GitHub Actions workflow to build from `website/` and deploy the generated `_site/` directory.

Do not assume a final repository name or public URL until the hosting location is confirmed.
