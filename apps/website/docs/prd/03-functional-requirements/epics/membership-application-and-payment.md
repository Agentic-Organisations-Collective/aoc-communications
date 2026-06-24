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
  - **Categories** source of truth: `aoc-governance/packages/statutes`.
  - **Fee amounts (decided)** are defined in the **bylaws**:
    `aoc-governance/packages/bylaws` (see
    [Sources & References](../../sources-and-references.md)). The form must reflect,
    not redefine, these.
- Based on the category, the **correct annual fee** is shown immediately, along with
  the relevant **benefits**. **Concrete fee amounts are shown publicly** on the join
  page (decided).
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

> **Unpaid probation (decided):** there is **no automation**. If an approved member
> does not pay, the board handles it as a **manual process**.
>
> **Phase note:** registration and payment are **Phase 2** (see
> [Roadmap & Phasing](../../roadmap-and-phasing.md)); email is minimised
> ([ADR-0006](../../../decisions/0006-email-and-newsletter.md)).

## Dependencies

- Auth and status model: [E1](./auth-and-user-management.md).
- Optional sponsor contribution relates to [E3](./donations-and-sponsorships.md).
- Online payment provider: see
  [Tech Stack & Integrations](../../../architecture/tech-stack-and-integrations.md).

## Open questions

- Exact fee table per category and company size (defined in the **bylaws**).
- Whether approval requires a single board member or multiple.
- Payment provider and billing model — see
  [ADR-0003](../../../decisions/0003-payment-provider.md) and
  [ADR-0004](../../../decisions/0004-membership-billing-model.md).
