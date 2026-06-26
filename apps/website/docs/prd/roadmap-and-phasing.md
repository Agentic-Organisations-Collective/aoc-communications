# Roadmap, Phasing & Milestones

> 🔵 **UNDER REVIEW** — Release sequencing and milestones for the website, with the
> prioritisation model made explicit. Reflects the agreed **presence-first MVP** and
> the decisions from the priority review. Tooling for each capability is tracked as
> proposals in [ADRs](../decisions/README.md).

## Prioritisation model (two orthogonal axes)

Priority on this project is expressed on **two independent axes**. They are *not*
the same thing, and an epic's position on one does not determine the other.

| Axis | Question it answers | Values | Where it lives |
| :---- | :---- | :---- | :---- |
| **Value (MoSCoW)** | How important is this capability **in itself**? | Must / Should / Could | `Priority` column in the [Epic Overview](./03-functional-requirements/epic-overview-and-feature-list.md) |
| **Timing (Phase)** | **When** do we build it? | Phase 1 / 2 / 3 | `Phase` column + this roadmap |

Consequences of treating them as orthogonal:

- A **Should-have can ship before a Must-have** when sequencing demands it
  (e.g. analytics **E7** is a *Should* but lands in Phase 1; membership payment
  **E2** is a *Must* but waits for Phase 2). This is intentional, not a contradiction.
- **Value never silently re-orders phases.** Phase order is driven by dependencies
  and the MVP bet (below), then sanity-checked against value — a high-value item is
  not allowed to sit late *without a recorded reason*.
- **Launch gates are a third, narrower notion** (see each milestone): a gate is a
  hard blocker for *that release*, independent of MoSCoW. A *Should*-have can be a
  launch gate (legal pages are not a "Must-have feature" in product terms, but the
  site **cannot go live without them**).

## The MVP bet (decided: presence-first)

Phase 1 deliberately ships **2 of the 5 business-case purposes** in full
(self-presentation, public content) plus a slice of a third (member content,
read-only). **Member acquisition and online payment are held to Phase 2.**

- **Why this bet:** there is little to *join* before there is content worth gating,
  and the **founding members are onboarded manually**, so a public join+pay funnel
  adds scope without yet serving demand. We establish presence and credibility first,
  then open the funnel once the gated content gives membership a reason to exist.
- **Accepted risk:** the **funding engine** (memberships, sponsorships) is not live
  at launch, so the year-1 acquisition/payment KPIs only start accruing in Phase 2.
  Mitigated by manual founding-member onboarding and a **static founding directory**
  (below) that signals traction before the funnel exists.
- **Trip-wire to revisit:** if inbound "how do I join / pay?" demand appears during
  Phase 1, pull the **E2 application form** forward (payment can still trail).

---

## Phase 1 — MVP: public presence + event content + read-only member area

**Outcome:** AOC is **publicly present and lawful to operate**, visitors can see what
the association is and does, and **manually provisioned members** can view gated event
documentation.

### Scope (Phase 1)

| Item | Epic | Notes |
| :---- | :---- | :---- |
| Public site (home/self-presentation, about, topics, **event announcements**) | E4 | Public contributions show **image, title, abstract** only |
| Event content model in `aoc-curation/packages/events` | E4 | Markdown + front matter; announcements vs. documentation |
| **Member area (read-only)** — view event documentation (slide PDFs, video/photo) | E1 (minimal) | Access via **manual social-login allowlist**; no self-registration yet |
| **Static founding directory** (members + sponsors) | E6 (static subset) | Built from existing register data (`aoc-board/packages/register`); **no member-data/auth dependency** — a credibility win for self-presentation |
| Basic analytics, cookieless | E7 | *Should-have, not a launch gate* — see gate note below |
| **Legal pages** (Impressum, privacy, English statutes/bylaws) | — | See [Legal & Compliance](./04-quality-and-compliance/legal-and-compliance.md) |

### Launch gates (hard blockers for go-live)

1. **Legal pages** — Impressum, privacy policy, and English translations of
   statutes/bylaws. The site **cannot be published lawfully** (Verein i.G.) without
   them.
2. **Anti-scraping protection** for members-only content — gated documentation must
   be **protected, not merely hidden**, before any member content goes live
   ([NFR](./04-quality-and-compliance/non-functional-requirements.md)).
3. **Static founding directory** — ships in the MVP as agreed (signals traction).

> **Explicitly *not* a launch gate: analytics (E7).** We accept launching
> potentially **blind on reach KPIs** if E7 slips. Trade-off recorded: the
> business-case reach metrics (traffic by source, LinkedIn referral share, monthly
> visitors) are **unmeasurable until E7 ships**, so either E7 lands with the MVP or
> those KPIs start late. E7 stays a *Should* and is **strongly recommended** for the
> launch window, but it does not block go-live.

### Definition of Done (Phase 1)

- Public pages render content sourced from the canonical packages (no copy stored in
  the app).
- An allowlisted social identity can sign in and view gated event documentation;
  a non-allowlisted identity cannot, and gated content resists scraping.
- All three launch gates are satisfied.
- The quality bar in [NFR](./04-quality-and-compliance/non-functional-requirements.md)
  is met for every shipped page.

---

## Phase 2 — Membership lifecycle (opening the funnel)

**Outcome:** new people can **apply, be approved, and pay online**; the member
directory becomes **live and self-maintaining**.

### Scope (Phase 2)

| Item | Epic | Notes |
| :---- | :---- | :---- |
| Self-registration & social login (full) | E1 (full) | Adds the registration/application path on top of Phase-1 auth |
| Membership application & online payment | E2 | Application form → board approval → probation → activated; in-app/manual payment prompts (no email) |
| Member & sponsor directory (live, opt-out) | E6 (full) | Auto-built from `aoc-board/packages/members`; LinkedIn avatars; supersedes the Phase-1 static list |
| Press page | — | From `aoc-communications/press` |

### Dependency note

- E2 depends on the **full E1** registration path and on payment-provider /
  billing-model decisions ([ADR-0003](../decisions/0003-payment-provider.md),
  [ADR-0004](../decisions/0004-membership-billing-model.md)).
- **Scope-saving observation:** because Phase-1 minimal auth already carries social
  login (4 providers), gated routes, and anti-scraping, the incremental cost of E1
  here is mainly the **application form** — this is *why* E2 sits immediately after,
  and why pulling the form forward (the MVP trip-wire) is cheap if demand appears.

### Definition of Done (Phase 2)

- A brand-new person can apply, be approved by the board, log in on probation, pay
  online, and move to *activated* — end to end, per
  [User Journey Flows](./02-ux-and-information-architecture/user-journey-flows.md).
- The live directory reflects member records and honours the opt-out flag.

---

## Phase 3 — Content engine & giving

**Outcome:** content production is **semi-automated** and the **giving/sponsorship**
surface is live.

### Scope (Phase 3)

| Item | Epic | Notes |
| :---- | :---- | :---- |
| Content automation & publishing | E5 | GitHub intake → agent-assisted articles → publish pipeline → LinkedIn scheduling |
| Donations & sponsorships | E3 | Donation form + sponsor sign-up |
| AI chat ("ask anything") across content | — | Replaces a classic on-site search; not in MVP |

### Watch-item (recorded tension)

- **Sponsorship is strategic but deferred.** "5 sponsors onboarded" is a **year-1
  KPI** and sponsorships fund events, yet E3 sponsor sign-up sits in Phase 3. Until
  then, **sponsor onboarding is manual** and sponsors appear via the static (Phase 1)
  / live (Phase 2) directory. **Revisit if** sponsor demand outruns the manual
  process — the **sponsor sign-up slice of E3 may be pulled into Phase 2**.

---

## Out of scope (decided)

No members' forum and no newsletter/email system. Member-to-member exchange and
outreach use **LinkedIn / WhatsApp**
([ADR-0007](../decisions/0007-forum-platform.md),
[ADR-0006](../decisions/0006-email-and-newsletter.md)).

## Dependency order (what gates what)

```text
E4 (content model) ─┬─► Phase 1 public site
E1-minimal (auth) ──┼─► Phase 1 member area ──► (anti-scraping gate)
E6-static ──────────┘
                     │
E1-full ──► E2 (application + payment) ──► E6-live ──► Phase 2
                     │
E5 ─┬─► Phase 3
E3 ─┘
```

## Notes

- Phases are about **sequencing**, not hard cut-offs; an earlier phase may stub a
  later capability (e.g. the Phase-1 allowlist before full auth; the static directory
  before the live one).
- **Milestones vs. phases:** each phase above now carries an **Outcome**, explicit
  **scope**, **launch gates** (where relevant), and a **Definition of Done** — these
  are the milestone criteria. Dates and effort sizing are **deliberately not fixed
  here** yet; add them when the technical team picks tooling via the ADRs.
- Every phase still respects the quality bar in
  [Non-Functional Requirements](./04-quality-and-compliance/non-functional-requirements.md).
