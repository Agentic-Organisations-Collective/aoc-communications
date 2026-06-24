# ADR-0007: Members' forum platform (later phase)

- **Status:** Proposed — decision deferred; feature itself is a **later phase**
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [Roadmap & Phasing](../prd/roadmap-and-phasing.md)

## Context

Members want an **exchange forum** to share content relatively freely with other
experts, without publishing to the open internet. This is **not** in the MVP — it is
planned for a later phase — but we record options now.

## Options considered

### Option A — Integrate Discourse (EU-hosted)

- **Pros:** Mature, feature-rich, SSO with our auth, moderation tools.
- **Cons:** Separate app to host/maintain; another UX to theme.

### Option B — GitHub Discussions

- **Pros:** Already in our GitHub-centric workflow; zero hosting; good for technical
  members.
- **Cons:** Requires GitHub accounts; not member-gated by our auth; weaker as a
  community home.

### Option C — Custom build

- **Pros:** Fully tailored and integrated.
- **Cons:** High effort; reinventing a solved problem.

## Recommendation

If/when prioritised, prefer **Discourse with SSO**. Consider **GitHub Discussions**
as a lightweight interim given the GitHub-centric stack.

## Decision

Deferred. The technical team decides later; feature scheduled for a later phase.
