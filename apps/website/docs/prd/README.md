# AOC Website — Product Requirements (PRD)

> 🟡 **DRAFT** — This hub restructures the early website idea drafts into a
> requirements outline. Nothing here is approved or specified to a level suitable
> for implementation yet. Treat it as the working baseline for the requirements
> process.

The website for the Agentic Organisations Collective (AOC) — a non-profit
association (Verein) for professional exchange about Software Factories and
Agent-OS systems. This is the **Product Requirements (PRD)**: it captures *what*
the website must do and *why* — **requirements only**. Solution specs live in
[`../architecture/`](../architecture/README.md) and decisions in
[`../decisions/`](../decisions/README.md).

## Project dashboard

| Field | Value |
| :---- | :---- |
| Project | AOC public + members website |
| Status | 🟡 Drafting requirements |
| Source | Brainstorming drafts (see `99-archive/`) |
| Language | English only |
| Entity | Verein in formation (i.G.) |
| Owner | Communications / Board |

## Structure

| Folder | Contents |
| :---- | :---- |
| `README.md` (this file) | PRD index & reading guide |
| `roadmap-and-phasing.md` | Release phases (MVP first) |
| `sources-and-references.md` | Single sources of truth & external resources (GitHub, LinkedIn, domain) |
| `01-strategy-and-research/` | Business case, KPIs, personas, benchmarks |
| `02-ux-and-information-architecture/` | Sitemap, navigation, user journey flows |
| `03-functional-requirements/` | Epic overview, feature list, and per-epic specs |
| `04-quality-and-compliance/` | Non-functional requirements and legal & compliance |
| `99-archive/` | Outdated versions and ideas on hold (raw source drafts) |

> **Outside this PRD (siblings under `docs/`):** solution specs in
> [`../architecture/`](../architecture/README.md) and tool/architecture decisions
> in [`../decisions/`](../decisions/README.md). Website **content** (copy, voice &
> tone, media) is **not** here — it is sourced from packages such as
> `website-content`, `brand-kit`, and `events`.

## Governance rules

1. **Never upload a screenshot.** If a requirement is visual, embed the live file
   link (Figma, FigJam, Miro). If it changes there, it changes everywhere.
2. **Document lifecycle status.** Every document carries one tag at the very top:
   - 🟡 **DRAFT** — work in progress; do not build yet.
   - 🔵 **UNDER REVIEW** — ready for stakeholder feedback.
   - 🟢 **APPROVED** — frozen baseline; developers can build this.
   - 🔴 **DEPRECATED** — no longer valid (move to `99-archive/`).
3. **Two-way link.** If a requirement is tracked in a task tool (issues, project
   board), the ticket links back to the requirement page here, and vice versa.

## Reading guide

Start with `01-strategy-and-research/` for the *why*, then `02-…` for *where*
content and flows live, `03-…` for *what* gets built, and
`04-quality-and-compliance/` for the quality bar and legal constraints. Original
raw idea drafts are preserved verbatim in `99-archive/`.

Strict separation: this PRD holds **requirements only**. The *how* (architecture,
tech stack) lives in [Architecture](../architecture/README.md), and tool choices
are tracked as proposals in [Decisions / ADRs](../decisions/README.md), to be
decided by the technical team.

Canonical sources the website consumes (statutes, bylaws, brand kit, events, plus
GitHub/LinkedIn/domain) are listed in
[Sources & References](./sources-and-references.md).

Release sequencing (MVP first) is in [Roadmap & Phasing](./roadmap-and-phasing.md).
