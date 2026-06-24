# ADR-0006: Email (transactional) & newsletter

- **Status:** Proposed — decision deferred to the technical team
- **Date:** 2026-06-23
- **Deciders:** Technical team
- **Related:** [E2 — Membership application & payment](../prd/03-functional-requirements/epics/membership-application-and-payment.md),
  [E5 — Content automation & publishing](../prd/03-functional-requirements/epics/content-automation-and-publishing.md)

## Context

Policy: **minimise email** wherever possible. Some flows may still need
**transactional** email (e.g. application approval, payment link). A **newsletter**
is optional and not prioritised. Primary distribution is **LinkedIn**.

## Options considered

### Transactional email

#### Option A — EU provider (e.g. Brevo / Mailjet)

- **Pros:** EU data residency; deliverability; templating.
- **Cons:** Another account/integration.

#### Option B — Postmark

- **Pros:** Excellent transactional deliverability and DX.
- **Cons:** US-based.

#### Option C — Resend

- **Pros:** Modern DX, simple API.
- **Cons:** Verify EU data location; younger.

### Newsletter

- **Option N1 — No newsletter (LinkedIn only):** simplest; aligns with the
  "minimise email" policy.
- **Option N2 — EU newsletter tool (Brevo/Mailjet) later:** owned audience channel;
  adds consent/list management overhead.

## Recommendation

Keep email to a **minimum**; where transactional mail is unavoidable, prefer an **EU
provider**. Defer the **newsletter** (start LinkedIn-only) and revisit if an owned
channel is needed.

## Decision

Deferred. The technical team decides later.
