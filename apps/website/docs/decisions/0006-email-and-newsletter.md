# ADR-0006: Email & newsletter

- **Status:** Rejected — out of scope (no email/newsletter system)
- **Date:** 2026-06-23
- **Deciders:** Board
- **Related:** [E2 — Membership application & payment](../prd/03-functional-requirements/epics/membership-application-and-payment.md),
  [E5 — Content automation & publishing](../prd/03-functional-requirements/epics/content-automation-and-publishing.md)

## Context

We considered transactional email and a newsletter. The board decided the website
will **not** build an email or newsletter system: outreach and notifications go
through **LinkedIn and/or WhatsApp**, and member-facing prompts (e.g. payment) are
shown **in the member area** or handled **manually**.

## Decision

**Out of scope.** No newsletter and no bulk mailing. No transactional email system
is built for now; any approval/payment follow-up is manual or in-app. Email may
still be stored as an optional contact field, but the site does not send mail.

Revisit with a **new ADR** only if a concrete need for transactional email arises.
