# Legal & Compliance

> 🟡 **DRAFT** — Legal and compliance requirements. The association is currently a
> **Verein in formation (i.G.)**, which affects the imprint and donation receipts.

## Entity status

- The association is a **Verein in Gründung (i.G.)** — not yet a registered `e.V.`
- The **Impressum** must reflect "i.G." and name the responsible founders until
  registration is complete.
- **Donation receipts** (Spendenbescheinigungen) generally require recognised
  non-profit status; until then, do **not** promise tax-deductible receipts. Revisit
  after registration and `Gemeinnützigkeit` recognition.

## Required legal pages

- [ ] **Impressum** (TMG / DDG) with i.G. status and responsible persons. **Contact
      (decided):** use a **board member's email** (no `info@` mailbox for now; there
      is no contact page).
- [ ] **Privacy policy** (GDPR / DSGVO) covering analytics, auth, payments, and any
      third parties.
- [ ] **Cookie/consent**: aim for **no banner** by using cookieless analytics
      ([ADR-0005](../../decisions/0005-web-analytics.md)); if ad pixels are added later, a
      consent mechanism becomes necessary (**ads decision deferred**).
- [ ] **Membership terms** referencing the binding statutes
      (`aoc-governance/packages/statutes`) and **fee** bylaws
      (`aoc-governance/packages/bylaws`).
- [ ] **English translations on site (decided):** statutes/bylaws are binding in
      **German**; the English site shows **non-binding English translations** that
      **link to the binding German** source (reuse `*.en.md` translations in
      `aoc-governance`).

## Data protection

- [ ] **EU data residency** preferred for hosting, auth, analytics, and email.
- [ ] **Data minimisation**: keep user fields lean (see
      [E1](../03-functional-requirements/epics/auth-and-user-management.md)).
- [ ] **Member directory consent**: the directory uses an **opt-out** model (members
      shown unless they hide themselves). Members must be **clearly informed** and
      able to opt out **easily**; ensure a lawful basis and a documented process
      (see [E6](../03-functional-requirements/epics/member-and-sponsor-directory.md)).
- [ ] **Processor agreements (AVV/DPA)** with each third-party provider.
- [ ] **Minimise email** and only with a lawful basis
      ([ADR-0006](../../decisions/0006-email-and-newsletter.md)).
- [ ] **Event media consent**: obtain **speaker consent before publishing** photos,
      video, or slides (see
      [E4](../03-functional-requirements/epics/content-model-and-event-hierarchy.md)).
- [ ] **Data retention (decided): keep all records.** ⚠️ Revisit against GDPR
      storage-limitation: define a justification/retention rationale, especially for
      **declined** applications.

## Licensing

- **Website code (decided):** **open-source under MIT**.
- **Public content license:** to be decided (e.g. Creative Commons) — see open
  questions.

## Payments

- [ ] Payment provider terms and EU regulatory requirements (SCA) — see
      [ADR-0003](../../decisions/0003-payment-provider.md).
- [ ] **Fee receipts/invoicing (decided: later)** — how membership payments are
      documented is deferred.

## Open questions

- Timeline to registered `e.V.` and `Gemeinnützigkeit`, which unlocks donation
  receipts and changes the imprint.
- Which **content license** to apply to public content (e.g. Creative Commons).
