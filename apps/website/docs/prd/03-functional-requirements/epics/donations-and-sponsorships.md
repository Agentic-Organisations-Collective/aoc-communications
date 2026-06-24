# E3 — Donations & Sponsorships

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.
> **Phase: later (deferred).** Donations are **shifted to a later phase**; sponsor
> onboarding follows membership. See [Roadmap & Phasing](../../roadmap-and-phasing.md).

## Scope

Standalone forms for one-off donations and for becoming a sponsor.

## Donation form

- Enter an **amount**, add a **comment**, provide **company or name**, and donate.
- **Decided:** allow **anonymous donations** and offer **suggested amount presets**.
- Members may also add a small sponsor contribution during fee payment (see
  [E2](./membership-application-and-payment.md)).

## Sponsor form

- "**I would like to become a sponsor.**" Captures intent and leads to sponsor
  onboarding.

## Sponsorship context & benefits

- We seek sponsoring to run **event formats** and high-level business exchange;
  sponsor income funds **event technology, documentation, etc.** — mainly for event
  formats.
- Sponsors receive:
  - **Logo on the website.**
  - **Named as sponsor at events.**
  - Right to **attend member events** with knowledgeable people.
- Sponsors are ideally tracked in **user management** (effectively a customer CRM)
  and shown in the directory (see [E6](./member-and-sponsor-directory.md)).

## Dependencies

- Payment provider: see
  [Tech Stack & Integrations](../../../architecture/tech-stack-and-integrations.md).

## Open questions

- Whether donations require an account or are fully anonymous/guest.
- **Sponsor tiers: to be decided later** (flat vs. named tiers).
