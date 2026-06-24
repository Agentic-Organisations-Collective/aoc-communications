# ADR-0008: Frontend framework (Astro + Svelte)

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [Tech Stack & Integrations](../architecture/tech-stack-and-integrations.md),
  [ADR-0001 Hosting model](./0001-hosting-model.md)

## Context

The idea drafts name **Astro and Svelte** as the intended stack. Content is authored
as **Markdown with front matter**. We need excellent performance (Lighthouse 100) and
the ability to render both static public pages and (later) gated member content.

## Options considered

### Option A — Astro + Svelte (proposed)

- **Pros:** Content-focused; ships minimal JS (islands); great Lighthouse/SEO;
  first-class Markdown/content collections; Svelte islands for interactivity; SSR
  adapters available for gated content.
- **Cons:** Two mental models (Astro + Svelte); smaller hiring pool than React.

### Option B — Next.js (React)

- **Pros:** Huge ecosystem; mature SSR/auth/payment patterns.
- **Cons:** Heavier JS by default; more work to hit Lighthouse 100 on content pages.

### Option C — SvelteKit

- **Pros:** Single framework (Svelte) for static + SSR; great DX.
- **Cons:** Less content-collection tooling than Astro; smaller ecosystem than React.

## Recommendation

Proceed with the drafted **Astro + Svelte** stack unless the technical team prefers a
single-framework setup (**SvelteKit**) for simplicity.

## Decision

Deferred. The technical team decides later.
