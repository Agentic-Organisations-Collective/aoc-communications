# E2 — Membership Application & Payment

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts. See the
> end-to-end flow in
> [User Journey Flows](../../02-ux-and-information-architecture/user-journey-flows.md).

## Scope

The online join flow: application form, board approval, probation, and online fee
payment.

## Application form

- An **online form** captures personal data (name, contact, etc.). The applicant can
  register with a **social login** to return later; social login can **pre-fill**
  name/email.
- The form includes fields per the **membership statutes**: researcher, public
  authority, company (which size), or individual.
  - Single source of truth: `aoc-governance/packages/statutes` (see
    [Sources & References](../../sources-and-references.md)). The form must reflect,
    not redefine, the statutes.
- Based on the category, the **correct annual fee** is shown immediately, along with
  the relevant **benefits**.
- Optional free-text questions: what the applicant expects from the association and
  what they can contribute (worth including even if it lengthens the form).

## Approval & status flow

1. Submitting the form creates a **membership application**.
2. A **board member** approves the application and manages its status (possibly
   several people involved) via user management.
3. On approval the user becomes a **member on probation** ("auf Vorbehalt"): can log
   in and view content, and receives an email prompting payment.
4. The user gets a **payment link**, pays the fee online, and may optionally add a
   small **sponsor contribution**.
5. Once payment is received, the user moves from **"on probation"** to
   **"activated"**.

## Dependencies

- Auth and status model: [E1](./auth-and-user-management.md).
- Optional sponsor contribution relates to [E3](./donations-and-sponsorships.md).
- Online payment provider: see
  [Tech Stack & Integrations](../../04-technical-specs-and-quality/tech-stack-and-integrations.md).

## Open questions

- Exact fee table per category and company size (sourced from the statutes).
- Whether approval requires a single board member or multiple.
