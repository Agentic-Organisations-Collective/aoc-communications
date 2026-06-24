# Roadmap & Phasing

> 🟡 **DRAFT** — Release phasing for the website. Reflects the agreed MVP scope.
> Tooling for each capability is tracked as proposals in
> [ADRs](../decisions/README.md).

## Phase 1 — MVP (public site + event content + read-only member area)

**Goal:** be publicly present and let (manually provisioned) members view event
documentation.

- **Public site:** home/self-presentation, about, topics, **event announcements**.
- **Event content model** ([E4](./03-functional-requirements/epics/content-model-and-event-hierarchy.md))
  in `aoc-curation/packages/events` — public view (image, title, abstract).
- **Member area (read-only):** members can **view event documentation**
  (slide PDFs, video/photo). Access via a **manual social-login allowlist** (the
  board adds approved social identities); full self-registration is **not** required
  yet.
- **Basic analytics** ([E7](./03-functional-requirements/epics/tracking-and-analytics.md)),
  cookieless if possible.
- **Legal pages** (Impressum, privacy, English translations of statutes/bylaws) —
  see [Legal & Compliance](./04-quality-and-compliance/legal-and-compliance.md).

## Phase 2 — Membership lifecycle

- **Self-registration & social login** ([E1](./03-functional-requirements/epics/auth-and-user-management.md)).
- **Membership application & online payment** ([E2](./03-functional-requirements/epics/membership-application-and-payment.md)).
- **Member & sponsor directory** ([E6](./03-functional-requirements/epics/member-and-sponsor-directory.md)).
- **Press page** (from `aoc-communications/press`).

## Phase 3 — Content engine, community & giving

- **Content automation & publishing** ([E5](./03-functional-requirements/epics/content-automation-and-publishing.md)):
  GitHub intake → agent-assisted articles → publish pipeline → LinkedIn scheduling.
- **Donations & sponsorships** ([E3](./03-functional-requirements/epics/donations-and-sponsorships.md)) — deferred to here.
- **Members' exchange forum** ([ADR-0007](../decisions/0007-forum-platform.md)).
- **AI chat ("ask anything")** across the content — replaces a classic on-site
  search; not in the MVP.
- **Newsletter** (optional, if prioritised).

## Notes

- Phases are about **sequencing**, not hard cut-offs; earlier phases may stub later
  capabilities (e.g. a simple gated area before full auth).
- Each phase still respects the quality bar in
  [Non-Functional Requirements](./04-quality-and-compliance/non-functional-requirements.md).
