# ADR-0004: Membership billing model

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team / Board
- **Related:** [E2 — Membership application & payment](../prd/03-functional-requirements/epics/membership-application-and-payment.md),
  [ADR-0003 Payment provider](./0003-payment-provider.md)

## Context

Annual membership fees differ by category (researcher, public authority, company by
size, individual) per the statutes. We need to decide how dues recur. This is partly
a **board/finance** decision, not only technical.

## Options considered

### Option A — Annual recurring, auto-renew

- **Pros:** Predictable revenue; less manual chasing; smooth member experience.
- **Cons:** Requires stored mandate/subscription; cancellation and dunning flows;
  SCA handling.

### Option B — Manual yearly invoice

- **Pros:** Simple; aligns with how many German Vereine operate; no stored mandates.
- **Cons:** Manual effort; late/failed renewals; reconciliation work.

### Option C — One-time payment with renewal reminder

- **Pros:** Simplest to launch; no recurring infrastructure.
- **Cons:** Higher churn; depends on members acting on reminders.

## Recommendation

Start with **Option C / B** for the MVP (payments are a later phase anyway), and
move to **Option A (auto-renew)** once the membership base justifies it. Confirm with
the board's finance/statute rules.

## Decision

Deferred. The technical team and board decide later.
