# E6 — Member & Sponsor Directory

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.

## Scope

A public directory of members (and sponsors), built automatically from user
management.

## Requirements

- Display **members** somewhere on the website; members can **opt out** via a
  **"do not display online"** flag in user management.
- The member list is **built automatically from user management**, not maintained
  separately.
- Per member, source displayed data via **APIs** (e.g. Gravatar, LinkedIn profile).
  Use one or more social accounts as the basis for displayed data rather than
  storing everything ourselves.
- Show each member's **country** and, if provided, their **company**.
- **Sponsors** are also shown, possibly on the **same page** as the member list, and
  ideally also live in user management (effectively a customer CRM).

## Dependencies

- User data and opt-out flag: [E1](./auth-and-user-management.md).
- Sponsor records: [E3](./donations-and-sponsorships.md).

## Open questions

- Which social/profile API is the primary source per member.
- Whether members and sponsors share one page or are separated.
