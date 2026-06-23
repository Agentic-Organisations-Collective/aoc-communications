# User Journey Flows

> 🟡 **DRAFT** — Flows derived from the idea drafts.
>
> **Governance rule — never upload a screenshot.** When these flows are drawn up
> visually, embed the live FigJam/Figma/Miro link below rather than pasting static
> images.
>
> - Live flow board: _embed link here_

## 1. Registration & login

- Non-public content requires a **login**; login requires **registration**;
  registration implies **user management**.
- **Social login is required**: Google, GitHub, Microsoft, LinkedIn.
- Registration is **not open to everyone** — only people who are members (or marked
  as such in user management) get a working login. New people can apply via
  registration.

### Two registration paths

- **Brand-new person:** registers → lands in an inbox where the board decides
  whether/when they become a member.
- **Pre-registered member:** already exists in user management (invited or onboarded
  offline, added manually by email) → on registering they **immediately** get a
  login and are already a member. _(Important use case.)_

## 2. Membership application & payment

1. Person applies via an **online form** (personal data, name, contact) and can
   register with a social login to return later. Social login can **pre-fill**
   name/email.
2. Form includes fields per the **membership statutes** (researcher, public
   authority, company + size, or individual). The **correct annual fee** and the
   **benefits** are shown immediately.
3. Optional free-text questions: what they expect from the association and what they
   can contribute (worth including even if it lengthens the form).
4. Submitting creates a **membership application**.
5. A **board member** approves the application and manages its status (possibly
   involving several people) via user management.
6. On approval, the user becomes a **member on probation** ("auf Vorbehalt"): they
   can log in and view content, and receive an email prompting payment.
7. They get a **payment link**, pay online, and may optionally add a small **sponsor
   contribution**.
8. Once payment is received, the user moves from **"on probation"** to
   **"activated"**.

```text
Apply (form) → Application created → Board approves → On probation (login + email)
   → Pay via link → Activated
```

## 3. Donation flow

- **Donation form:** enter an amount, add a comment, provide company or name, donate.

## 4. Sponsorship flow

- **Sponsor form:** "I would like to become a sponsor." Leads to sponsor onboarding
  (logo, naming at events, member-event access).

## Related specs

- [Auth & user management epic](../03-functional-requirements/epics/auth-and-user-management.md)
- [Membership application & payment epic](../03-functional-requirements/epics/membership-application-and-payment.md)
- [Donations & sponsorships epic](../03-functional-requirements/epics/donations-and-sponsorships.md)
