# ADR-0005: Web analytics (cookieless)

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [E7 — Tracking & analytics](../prd/03-functional-requirements/epics/tracking-and-analytics.md),
  [Legal & Compliance](../prd/04-quality-and-compliance/legal-and-compliance.md)

## Context

We want **campaign/source tracking** and reach measurement, ideally **without a
cookie banner**. EU data residency and GDPR-friendliness preferred. Ad pixels
(LinkedIn/Twitch/Google) are an open question and would change the consent picture.

## Options considered

### Option A — Plausible (EU, cookieless)

- **Pros:** EU-hosted; cookieless by design (often no banner needed); lightweight;
  UTM/campaign support.
- **Cons:** Less granular than GA; paid SaaS (self-host possible).

### Option B — Umami (self-host, open-source)

- **Pros:** Free, open-source, self-hostable in EU; cookieless.
- **Cons:** You operate it; fewer features.

### Option C — Fathom

- **Pros:** Cookieless, privacy-first, simple.
- **Cons:** Paid; verify EU data location.

### Option D — Google Analytics 4

- **Pros:** Powerful, free, deep campaign analytics.
- **Cons:** Requires consent banner; GDPR concerns; contradicts the no-banner goal.

## Recommendation

Prefer a **cookieless EU tool** (Plausible or self-hosted Umami). If **ad pixels**
are later required, they will likely **trigger consent** — keep them separable so the
baseline analytics stay banner-free.

## Decision

Deferred. The technical team decides later.
