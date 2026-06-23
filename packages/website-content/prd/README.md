# AOC Website — Requirements Hub (00_START_HERE)

> 🟡 **DRAFT** — This hub restructures the early website idea drafts into a
> requirements outline. Nothing here is approved or specified to a level suitable
> for implementation yet. Treat it as the working baseline for the requirements
> process.

The website for the Agentic Organisations Collective (AOC) — a non-profit
association (Verein) for professional exchange about Software Factories and
Agent-OS systems. This hub holds the product requirements, organised into a
fixed 6-part hierarchy.

## Project dashboard

| Field | Value |
| :---- | :---- |
| Project | AOC public + members website |
| Status | 🟡 Drafting requirements |
| Source | Brainstorming drafts (see `99-archive/`) |
| Stack (proposed) | Astro + Svelte |
| Owner | Communications / Board |

## Structure

| Folder | Contents |
| :---- | :---- |
| `README.md` (this file) | Project dashboard & reading guide |
| `sources-and-references.md` | Single sources of truth & external resources (GitHub, LinkedIn, domain) |
| `01-strategy-and-research/` | Business case, KPIs, personas, benchmarks |
| `02-ux-and-information-architecture/` | Sitemap, navigation, user journey flows |
| `03-functional-requirements/` | Epic overview, feature list, and per-epic specs |
| `04-technical-specs-and-quality/` | Tech stack, integrations, non-functional requirements |
| `05-content-and-media-assets/` | Website copy deck, brand assets |
| `99-archive/` | Outdated versions and ideas on hold (raw source drafts) |

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
content and flows live, `03-…` for *what* gets built, and `04-…` for *how* and the
quality bar. `05-…` holds the actual copy and media. Original raw idea drafts are
preserved verbatim in `99-archive/`.

Canonical sources the website consumes (statutes, bylaws, brand kit, events, plus
GitHub/LinkedIn/domain) are listed in
[Sources & References](./sources-and-references.md).
