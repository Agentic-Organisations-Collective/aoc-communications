# Architecture Decision Records (ADRs)

> 🟡 **PROPOSED** — These ADRs capture **tool and architecture options as proposals
> with pros and cons**. They are **not decided here**; the **technical team** makes
> the final call later. Until then, treat every option as open.

Each ADR follows the same shape: context → options (with pros/cons) →
recommendation → decision (deferred).

## Index

| ADR | Topic | Status |
| :---- | :---- | :---- |
| [ADR-0001](./0001-hosting-model.md) | Hosting model (static vs. SSR vs. serverless) | Proposed |
| [ADR-0002](./0002-authentication-provider.md) | Authentication provider | Proposed |
| [ADR-0003](./0003-payment-provider.md) | Payment provider | Proposed |
| [ADR-0004](./0004-membership-billing-model.md) | Membership billing model | Proposed |
| [ADR-0005](./0005-web-analytics.md) | Web analytics (cookieless) | Proposed |
| [ADR-0006](./0006-email-and-newsletter.md) | Email (transactional) & newsletter | Proposed |
| [ADR-0007](./0007-forum-platform.md) | Members' forum platform (later phase) | Proposed |
| [ADR-0008](./0008-frontend-framework.md) | Frontend framework (Astro + Svelte) | Proposed |

## How to use

- Add a new ADR when a tool/architecture choice arises.
- Keep status `Proposed` until the technical team decides, then switch to
  `Accepted` (or `Superseded` / `Rejected`) and record the rationale.
