# ADR-0001: Hosting model

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [Tech Stack & Integrations](../architecture/tech-stack-and-integrations.md),
  [Sources & References](../prd/sources-and-references.md)

## Context

A pure **GitHub Pages** site is static-only and cannot serve auth-gated member
content, run login, or process payments. The intended domain
`agentic-organisations-collective.eu` is not yet configured. The site has a public
tier and a members-only tier, plus later registration and payments. EU data
residency is preferred.

## Options considered

### Option A — Split: static public site + separate app for members/auth/payments

- **Pros:** Public site stays fast and cheap (CDN/Pages); clean separation; public
  marketing can ship first (MVP) independent of the app; easy to reach Lighthouse
  100 on the public tier.
- **Cons:** Two deployments to operate; shared design system must be kept in sync;
  cross-domain session/SSO handling.

### Option B — Full SSR app on an EU host

- **Pros:** One codebase and deployment; gating, auth and payments are
  straightforward; consistent UX.
- **Cons:** Higher hosting/ops cost; public pages no longer "just static"; more
  surface to harden for Lighthouse/perf.

### Option C — Static frontend + serverless/edge functions

- **Pros:** Mostly static (fast/cheap) with functions only for auth callbacks,
  payment webhooks, gated fetches; EU edge regions available.
- **Cons:** Function/runtime lock-in risk; gated content rendering is more complex;
  cold-starts.

## Recommendation

Lean toward **Option A** for the MVP (public site + event announcements + a small
gated member area), keeping the option to converge on **Option C/B** as
registration and payments are added. Host in the **EU** regardless.

> **Preferences (from product):** **GitHub Pages is technically preferred** for the
> **public** tier; **EU** hosting is preferred for anything handling personal data;
> the final call is **deferred** to this ADR. The canonical domain is
> **`www` (redirect apex)** — see [Tech Stack & Integrations](../architecture/tech-stack-and-integrations.md).

## Members app location

Where the gated members app lives is **decided together with this ADR**. Options:
`members.<domain>` subdomain, `app.<domain>` subdomain, or a same-domain `/members`
path. A subdomain pairs naturally with the **Split** model (Option A).

## Decision

Deferred. The technical team decides later.
