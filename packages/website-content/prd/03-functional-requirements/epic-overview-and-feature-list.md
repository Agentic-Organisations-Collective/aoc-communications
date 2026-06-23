# Epic Overview & Feature List

> 🟡 **DRAFT** — The product backlog at epic level, derived from the idea drafts.
> Status and priority columns are provisional.
>
> **Two-way link rule:** when an epic is tracked on a task board, link the ticket to
> the epic file below and back.

## Epics

| # | Epic | Summary | Priority | Status |
| :---- | :---- | :---- | :---- | :---- |
| E1 | [Auth & user management](./epics/auth-and-user-management.md) | Registration, social login, member-gated access, user data | Must-have | 🟡 Draft |
| E2 | [Membership application & payment](./epics/membership-application-and-payment.md) | Application form, board approval, probation→activated, online fee payment | Must-have | 🟡 Draft |
| E3 | [Donations & sponsorships](./epics/donations-and-sponsorships.md) | Donation form, sponsor sign-up form | Should-have | 🟡 Draft |
| E4 | [Content model & event hierarchy](./epics/content-model-and-event-hierarchy.md) | Public/non-public duplication, event announcements vs. documentation, content hierarchy | Must-have | 🟡 Draft |
| E5 | [Content automation & publishing](./epics/content-automation-and-publishing.md) | GitHub-based intake, agent-assisted articles, publish pipeline, LinkedIn scheduling | Should-have | 🟡 Draft |
| E6 | [Member & sponsor directory](./epics/member-and-sponsor-directory.md) | Auto-built directory from user management, opt-out, API-sourced profiles | Should-have | 🟡 Draft |
| E7 | [Tracking & analytics](./epics/tracking-and-analytics.md) | Source tracking, campaign tracking, optional ad pixels, no cookie banner | Should-have | 🟡 Draft |

## Cross-cutting feature themes

- **Public vs. members-only** runs through E1, E4, E5, E6.
- **Quality bar** (Lighthouse, accessibility, anti-scraping) is captured separately
  in [Non-Functional Requirements](../04-technical-specs-and-quality/non-functional-requirements.md).
- **Stack & integrations** (Astro/Svelte, auth provider, APIs, payment) live in
  [Tech Stack & Integrations](../04-technical-specs-and-quality/tech-stack-and-integrations.md).
