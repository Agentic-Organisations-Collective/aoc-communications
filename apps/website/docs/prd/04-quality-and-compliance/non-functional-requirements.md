# Non-Functional Requirements (SEO, Performance, Accessibility)

> 🟡 **DRAFT** — Quality bar derived from the idea drafts. Treat as a checklist; each
> item must be verified before a page goes live.

## Performance

- [ ] **Lighthouse 100 / 100 / 100 / 100** (all green) on the **public** site.
- [ ] **Lighthouse 100 / 100 / 100 / 100** (all green) on the **logged-in** site.
- [ ] **Enforce image optimization and a performance budget in CI** (decided).

## Accessibility

- [ ] **At least WCAG AA**, with as much **AAA** as possible.
- [ ] Honor and evaluate **browser signals**: high contrast, dark/light theme, etc.
- [ ] **Audit method (decided):** **automated** checks (axe / Lighthouse) in **CI**
      plus **periodic manual** testing.

## Language

- [ ] **Content language: English only** (decided). Honor the theme/contrast browser
      signals; the language signal is not used to switch content.

## Legal & compliance

- [ ] Meet the requirements in [Legal & Compliance](./legal-and-compliance.md)
      (Impressum with `i.G.` status, GDPR privacy policy, no donation-receipt
      promises until `Gemeinnützigkeit`).

## Security & content protection

- [ ] Members-only content must be **protected from scraping**, not merely hidden.
- [ ] Access control enforced server-side, consistent with
      [Auth & user management](../03-functional-requirements/epics/auth-and-user-management.md).

## Privacy & SEO

- [ ] Tracking supports **campaign tracking** and traffic-source attribution (see
      [Tracking & Analytics](../03-functional-requirements/epics/tracking-and-analytics.md)).
- [ ] **Launch banner-free (decided):** no ad pixels at launch, so **no cookie
      banner**; ads are an ads-later decision.
- [ ] Public content is **findable** (SEO), supporting reach goals.

## Open questions

- Concrete target AAA criteria to pursue beyond the AA baseline.
- The specific analytics/consent approach that satisfies "no cookie banner".
