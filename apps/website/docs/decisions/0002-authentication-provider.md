# ADR-0002: Authentication provider

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [E1 — Auth & user management](../prd/03-functional-requirements/epics/auth-and-user-management.md)

## Context

Members-only content requires login. Social login is required (Google, GitHub,
Microsoft, LinkedIn). A **European** (or open-source, ideally European) provider is
preferred over a US SaaS. Registration is gated: only members (or people marked as
such) get a working login.

## Options considered

### Option A — Zitadel (EU SaaS or self-host, open-source)

- **Pros:** EU-hosted option; open-source; social logins; modern; self-host
  possible for full data control.
- **Cons:** Smaller ecosystem than incumbents; self-host adds ops.

### Option B — Authentik (self-host, open-source)

- **Pros:** Full control, EU data residency by hosting yourself; flexible.
- **Cons:** You operate and secure it; more setup.

### Option C — Keycloak (self-host, open-source)

- **Pros:** Mature, battle-tested, feature-rich.
- **Cons:** Heavier to run and theme; steeper learning curve.

### Option D — Logto (open-source)

- **Pros:** Developer-friendly, modern UX, self-host or cloud.
- **Cons:** Younger project; verify EU hosting.

### Option E — Clerk (US SaaS) — fallback

- **Pros:** Fastest to integrate; great DX; handles everything.
- **Cons:** US-based (data residency concern); contradicts the EU preference.

## Recommendation

Prefer an **EU/open-source** option (Zitadel or self-hosted Authentik). Use Clerk
only as a time-boxed fallback if EU options block the MVP.

## Decision

Deferred. The technical team decides later.
