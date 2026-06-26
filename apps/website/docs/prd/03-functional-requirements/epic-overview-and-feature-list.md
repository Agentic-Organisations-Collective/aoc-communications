# Epic Overview & Feature List

> 🟡 **DRAFT** — The product backlog at epic level, derived from the idea drafts.
> Status is provisional.
>
> **Priority is two orthogonal axes** (see
> [Prioritisation model](../roadmap-and-phasing.md#prioritisation-model-two-orthogonal-axes)):
> **Value (MoSCoW)** = how important in itself; **Phase** = when we build it. A
> *Should*-have can ship before a *Must*-have when sequencing demands it — that is
> intentional, not a contradiction.
>
> **Two-way link rule:** when an epic is tracked on a task board, link the ticket to
> the epic file below and back.

## Epics

| # | Epic | Summary | Value (MoSCoW) | Phase (timing) | Status |
| :---- | :---- | :---- | :---- | :---- | :---- |
| E1 | [Auth & user management](./epics/auth-and-user-management.md) | Registration, social login, member-gated access, user data | Must-have | 1 (minimal allowlist) → 2 (full self-reg) | 🟡 Draft |
| E2 | [Membership application & payment](./epics/membership-application-and-payment.md) | Application form, board approval, probation→activated, online fee payment | Must-have | 2 | 🟡 Draft |
| E3 | [Donations & sponsorships](./epics/donations-and-sponsorships.md) | Donation form, sponsor sign-up form | Should-have | 3 (sponsor slice may move to 2 — see roadmap watch-item) | 🟡 Draft |
| E4 | [Content model & event hierarchy](./epics/content-model-and-event-hierarchy.md) | Public/non-public content, event announcements vs. documentation, content hierarchy | Must-have | 1 | 🟡 Draft |
| E5 | [Content automation & publishing](./epics/content-automation-and-publishing.md) | GitHub-based intake, agent-assisted articles, publish pipeline, LinkedIn scheduling | Should-have | 3 | 🟡 Draft |
| E6 | [Member & sponsor directory](./epics/member-and-sponsor-directory.md) | Directory built from `aoc-board/packages/members`, opt-out, LinkedIn avatars | Should-have | 1 (static founding subset) → 2 (full live) | 🟡 Draft |
| E7 | [Tracking & analytics](./epics/tracking-and-analytics.md) | Source tracking, campaign tracking, optional ad pixels, no cookie banner | Should-have | 1 (recommended; **not** a launch gate) | 🟡 Draft |

> **Out of scope (decided):** no members' forum and no email/newsletter system —
> member-to-member exchange and outreach happen via LinkedIn / WhatsApp
> ([ADR-0007](../../decisions/0007-forum-platform.md),
> [ADR-0006](../../decisions/0006-email-and-newsletter.md)). See the
> [Roadmap & Phasing](../roadmap-and-phasing.md) for the full sequence.

## Cross-cutting feature themes

- **Public vs. members-only** runs through E1, E4, E5, E6.
- **Quality bar** (Lighthouse, accessibility, anti-scraping) is captured separately
  in [Non-Functional Requirements](../04-quality-and-compliance/non-functional-requirements.md).
- **Tool & architecture choices** are tracked as proposals in
  [ADRs](../../decisions/README.md) (decided later by the
  technical team).
- **Release sequencing** is in [Roadmap & Phasing](../roadmap-and-phasing.md).
