# Epic Overview & Feature List

> 🟡 **DRAFT** — The product backlog at epic level, derived from the idea drafts.
> Status and priority columns are provisional.
>
> **Two-way link rule:** when an epic is tracked on a task board, link the ticket to
> the epic file below and back.

## Epics

| # | Epic | Summary | Priority | Phase | Status |
| :---- | :---- | :---- | :---- | :---- | :---- |
| E1 | [Auth & user management](./epics/auth-and-user-management.md) | Registration, social login, member-gated access, user data | Must-have | 1 (minimal) → 2 (full) | 🟡 Draft |
| E2 | [Membership application & payment](./epics/membership-application-and-payment.md) | Application form, board approval, probation→activated, online fee payment | Must-have | 2 | 🟡 Draft |
| E3 | [Donations & sponsorships](./epics/donations-and-sponsorships.md) | Donation form, sponsor sign-up form | Should-have | 3 (deferred) | 🟡 Draft |
| E4 | [Content model & event hierarchy](./epics/content-model-and-event-hierarchy.md) | Public/non-public content, event announcements vs. documentation, content hierarchy | Must-have | 1 | 🟡 Draft |
| E5 | [Content automation & publishing](./epics/content-automation-and-publishing.md) | GitHub-based intake, agent-assisted articles, publish pipeline, LinkedIn scheduling | Should-have | 3 | 🟡 Draft |
| E6 | [Member & sponsor directory](./epics/member-and-sponsor-directory.md) | Directory built from `aoc-board/packages/members`, opt-out, LinkedIn avatars | Should-have | 2 | 🟡 Draft |
| E7 | [Tracking & analytics](./epics/tracking-and-analytics.md) | Source tracking, campaign tracking, optional ad pixels, no cookie banner | Should-have | 1 | 🟡 Draft |
| E8 | Members' exchange forum | Gated forum for expert exchange | Could-have | 3 (deferred) | 🟡 Draft |

> E8 is deferred to a later phase; platform options are in
> [ADR-0007](../../decisions/0007-forum-platform.md). See the
> [Roadmap & Phasing](../roadmap-and-phasing.md) for the full sequence.

## Cross-cutting feature themes

- **Public vs. members-only** runs through E1, E4, E5, E6.
- **Quality bar** (Lighthouse, accessibility, anti-scraping) is captured separately
  in [Non-Functional Requirements](../04-quality-and-compliance/non-functional-requirements.md).
- **Tool & architecture choices** are tracked as proposals in
  [ADRs](../../decisions/README.md) (decided later by the
  technical team).
- **Release sequencing** is in [Roadmap & Phasing](../roadmap-and-phasing.md).
