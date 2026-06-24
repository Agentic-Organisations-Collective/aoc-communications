# ADR-0003: Payment provider

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [E2 — Membership application & payment](../prd/03-functional-requirements/epics/membership-application-and-payment.md),
  [E3 — Donations & sponsorships](../prd/03-functional-requirements/epics/donations-and-sponsorships.md)

## Context

The site must collect **membership fees** (annual), **donations**, and optional
**sponsor contributions** online via a payment link. SEPA and cards are relevant for
a German/EU non-profit. EU-friendly and recurring support preferred.

## Options considered

### Option A — Mollie (EU)

- **Pros:** EU-based; SEPA + cards + common EU methods; clean API; good for
  non-profits.
- **Cons:** Recurring/subscription tooling less rich than Stripe.

### Option B — Stripe

- **Pros:** Best-in-class subscriptions/invoicing/Billing; great DX.
- **Cons:** US company (EU entities exist); can be heavier than needed.

### Option C — GoCardless (SEPA Direct Debit)

- **Pros:** Excellent for recurring SEPA membership dues; low fees for bank debit.
- **Cons:** Card payments need a complement; debit-centric.

### Option D — PayPal

- **Pros:** Familiar to donors; quick to add.
- **Cons:** Fees; UX/branding constraints; less clean for memberships.

## Recommendation

Prefer **Mollie** (EU) for breadth, optionally **GoCardless** for recurring SEPA
dues. Revisit with the billing model in [ADR-0004](./0004-membership-billing-model.md).

## Decision

Deferred. The technical team decides later.
