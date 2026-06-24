# Tech Stack & Third-Party Integrations

> 🟡 **DRAFT** — Stack and integrations. **Tool choices are tracked as proposals in
> [ADRs](../decisions/README.md)** and decided later by the technical team; this page
> summarises them and records settled product decisions.

## Language

- **Content language: English only** (decided).

## Core stack

- **Frontend:** **Astro** and **Svelte** (proposed — see
  [ADR-0008](../decisions/0008-frontend-framework.md)).
- **Content format:** **Markdown with front matter**, using different data models
  per content type (see
  [Content Model & Event Hierarchy](../prd/03-functional-requirements/epics/content-model-and-event-hierarchy.md)).

## Authentication

- **Social login is required:** Google, GitHub, Microsoft, LinkedIn.
- **Auth provider:** European / open-source preferred — options in
  [ADR-0002](../decisions/0002-authentication-provider.md).

## Payments

- Online **membership fee payment** via a payment link, plus **donation** and
  **sponsor contribution** flows (see
  [E2](../prd/03-functional-requirements/epics/membership-application-and-payment.md) and
  [E3](../prd/03-functional-requirements/epics/donations-and-sponsorships.md)).
- Provider options in [ADR-0003](../decisions/0003-payment-provider.md); billing model in
  [ADR-0004](../decisions/0004-membership-billing-model.md).

## Member data & profile imagery

- **Member records (decided):** Markdown + front matter in Git at
  `aoc-board/packages/members`.
- **Avatars (decided):** loaded from **LinkedIn** (see
  [E6](../prd/03-functional-requirements/epics/member-and-sponsor-directory.md)).
- **Event media (decided):** stored in Git in `aoc-curation/packages/events`.

## Content automation (GitHub-based)

- A **"Marketing Automate OS"** built on **GitHub**: content intake via **Issues**,
  agent-assisted generation in **pull requests**, and a **publish pipeline** on merge
  that republishes the Astro/Svelte site and **schedules a LinkedIn post** (see
  [E5](../prd/03-functional-requirements/epics/content-automation-and-publishing.md)).
  - GitHub organisation: <https://github.com/Agentic-Organisations-Collective>
    (org profile: `.github/profile/README.md`).

## Hosting & domain

- Intended domain: **agentic-organisations-collective.eu** — _not yet configured on
  GitHub Pages._ Note: GitHub Pages is static-only — hosting options for gated
  content are in [ADR-0001](../decisions/0001-hosting-model.md).
- **Canonical domain (decided): `www`** (apex redirects to `www`).
- **GitHub Pages** is the **technically preferred** host for the **public** tier;
  **EU** hosting preferred for personal-data workloads (decided in
  [ADR-0001](../decisions/0001-hosting-model.md)).

## Distribution & tracking

- **LinkedIn** as the primary distribution channel (association page).
- Optional **tracking pixels** for LinkedIn, Twitch, Google ads (see
  [E7](../prd/03-functional-requirements/epics/tracking-and-analytics.md)).
- Analytics tooling options in [ADR-0005](../decisions/0005-web-analytics.md).

## Tool decisions (tracked as ADRs)

| Topic | ADR |
| :---- | :---- |
| Hosting model | [ADR-0001](../decisions/0001-hosting-model.md) |
| Authentication provider | [ADR-0002](../decisions/0002-authentication-provider.md) |
| Payment provider | [ADR-0003](../decisions/0003-payment-provider.md) |
| Membership billing model | [ADR-0004](../decisions/0004-membership-billing-model.md) |
| Web analytics | [ADR-0005](../decisions/0005-web-analytics.md) |
| Email & newsletter | [ADR-0006](../decisions/0006-email-and-newsletter.md) |
| Forum platform | [ADR-0007](../decisions/0007-forum-platform.md) |
| Frontend framework | [ADR-0008](../decisions/0008-frontend-framework.md) |
