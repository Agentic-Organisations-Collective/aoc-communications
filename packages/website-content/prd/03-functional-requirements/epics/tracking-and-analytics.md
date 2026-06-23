# E7 — Tracking & Analytics

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.

## Scope

Visitor and campaign tracking that supports reach generation, ideally without a
cookie banner.

## Requirements

- **Goal:** generate reach, likely with heavy use of **LinkedIn**.
  - LinkedIn page: <https://www.linkedin.com/company/agentic-organisations-collective/>
    (see [Sources & References](../../sources-and-references.md)).
- Track users on the website and **where they come from** (traffic source).
- Support **campaign tracking** well.
- Consider **tracking pixels** for ads (LinkedIn, Twitch, Google) to target better.
- Ideally, **avoid a cookie banner**.

## Dependencies

- Feeds the KPIs in
  [Business Case & KPIs](../../01-strategy-and-research/business-case-and-kpis.md).
- Privacy/consent constraints relate to
  [Non-Functional Requirements](../../04-technical-specs-and-quality/non-functional-requirements.md).
- LinkedIn publishing: [E5](./content-automation-and-publishing.md).

## Open questions

- Whether **paid ads** are needed at all (open), though we do want to promote events.
- Which analytics approach allows meaningful tracking **without** a cookie banner.
