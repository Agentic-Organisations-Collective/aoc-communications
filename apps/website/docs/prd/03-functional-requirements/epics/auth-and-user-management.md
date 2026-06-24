# E1 — Auth & User Management

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.

## Scope

Registration, login, and the user-management layer that gates members-only content.

## Requirements

- Non-public content requires a **login**; login requires **registration**;
  registration implies **user management**.
- **Social login is required**: Google, GitHub, Microsoft, LinkedIn.
- Registration is **not open to everyone** — only people who are members (or marked
  as such in user management) get a working login. New people can apply via
  registration (see [E2](./membership-application-and-payment.md)).
- After login, members navigate a content area that is otherwise not publicly
  visible.

## Two registration paths

- **Brand-new person:** registers → application lands in an inbox where the board
  decides whether/when they become a member.
- **Pre-registered member:** already exists in user management (invited / onboarded
  offline / added manually by email) → on registering they **immediately** get a
  login and are already a member. _(Important use case.)_

## User data model (keep lean)

- Fields: email, phone, first/last name, company, possibly multiple addresses.
- Some fields may be **sourced elsewhere** (e.g. via social accounts / APIs) rather
  than stored ourselves.
- A **"do not display online"** flag controls directory visibility (see
  [E6](./member-and-sponsor-directory.md)).
- Member status values include at least: applicant, **on probation** ("auf
  Vorbehalt"), **activated**.

## Roles & permissions (decided)

The system distinguishes these roles:

- **Board / admin** — approve applications, manage members and status, full access.
- **Member** — access members-only content and event documentation.
- **Applicant** — has registered/applied; awaiting board approval.
- **Sponsor** — sponsor record; visibility on the site (see
  [E3](./donations-and-sponsorships.md)).

## MVP access (decided)

Before self-registration exists (Phase 2), members reach the gated area via a
**manual social-login allowlist**: the board adds approved social identities, and
only those can sign in to view event documentation.

## Non-functional dependency

- Members-only content must be **protected from scraping**, not merely hidden — see
  [Non-Functional Requirements](../../04-quality-and-compliance/non-functional-requirements.md).

## Open questions

- Which **auth provider** (European / open-source preferred) — see
  [ADR-0002](../../../decisions/0002-authentication-provider.md).
- Exactly which addresses/fields are mandatory vs. optional.
