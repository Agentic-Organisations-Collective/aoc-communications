# Website Ideas (Drafts)

> **Status: archived input.** The early brainstorming drafts that lived here have
> been moved into the structured requirements hub and are preserved verbatim in the
> archive.

## Where the content went

The raw drafts (`website-purpose.md` and
`website-features-and-content-process.md`) were restructured into the website's
**Product Requirements (PRD)** in the `website` app at
[`apps/website/docs/`](../../../apps/website/docs/README.md):

- Strategy, KPIs, personas → `docs/prd/01-strategy-and-research/`
- Sitemap & user journeys → `docs/prd/02-ux-and-information-architecture/`
- Feature epics (auth, payments, content, tracking, …) → `docs/prd/03-functional-requirements/`
- Non-functional requirements & legal → `docs/prd/04-quality-and-compliance/`

Tool/architecture **decisions** live in `docs/decisions/` (ADRs) and **solution
specs** in `docs/architecture/`. The website **copy deck** and **voice & tone**
now live in this `website-content` package — content is sourced from packages,
not kept in the PRD.

The original verbatim drafts are kept in
[`apps/website/docs/prd/99-archive/`](../../../apps/website/docs/prd/99-archive/)
for reference.
