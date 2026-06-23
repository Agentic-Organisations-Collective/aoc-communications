# Tech Stack & Third-Party Integrations

> 🟡 **DRAFT** — Proposed stack and integrations from the idea drafts. Several items
> are explicitly to be researched.

## Core stack

- **Frontend:** **Astro** and **Svelte**.
- **Content format:** **Markdown with front matter**, using different data models
  per content type (see
  [Content Model & Event Hierarchy](../03-functional-requirements/epics/content-model-and-event-hierarchy.md)).

## Authentication

- **Social login is required:** Google, GitHub, Microsoft, LinkedIn.
- **Auth provider:** **Clerk** could do everything, but a **European** (or
  open-source, ideally European) login provider is **preferred**. _To be researched._

## Payments

- Online **membership fee payment** via a payment link, plus **donation** and
  **sponsor contribution** flows (see
  [E2](../03-functional-requirements/epics/membership-application-and-payment.md) and
  [E3](../03-functional-requirements/epics/donations-and-sponsorships.md)).
- _Payment provider: to be selected._

## Profile data APIs

- Source member profile data via APIs such as **Gravatar** and **LinkedIn profile**,
  rather than storing everything ourselves (see
  [E6](../03-functional-requirements/epics/member-and-sponsor-directory.md)).

## Content automation (GitHub-based)

- A **"Marketing Automate OS"** built on **GitHub**: content intake via **Issues**,
  agent-assisted generation in **pull requests**, and a **publish pipeline** on merge
  that republishes the Astro/Svelte site and **schedules a LinkedIn post** (see
  [E5](../03-functional-requirements/epics/content-automation-and-publishing.md)).
  - GitHub organisation: <https://github.com/Agentic-Organisations-Collective>
    (org profile: `.github/profile/README.md`).

## Hosting & domain

- Intended domain: **agentic-organisations-collective.eu** — _not yet configured on
  GitHub Pages._
- See [Sources & References](../sources-and-references.md) for all canonical sources.

## Distribution & tracking

- **LinkedIn** as the primary distribution channel (association page).
- Optional **tracking pixels** for LinkedIn, Twitch, Google ads (see
  [E7](../03-functional-requirements/epics/tracking-and-analytics.md)).

## To research / decide

- European/open-source auth provider vs. Clerk.
- Payment provider.
- Analytics tooling that works **without a cookie banner**.
- Which profile API is the primary source per member.
