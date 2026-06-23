# Non-Functional Requirements (SEO, Performance, Accessibility)

> 🟡 **DRAFT** — Quality bar derived from the idea drafts. Treat as a checklist; each
> item must be verified before a page goes live.

## Performance

- [ ] **Lighthouse 100 / 100 / 100 / 100** (all green) on the **public** site.
- [ ] **Lighthouse 100 / 100 / 100 / 100** (all green) on the **logged-in** site.

## Accessibility

- [ ] **At least WCAG AA**, with as much **AAA** as possible.
- [ ] Honor and evaluate **browser signals**: high contrast, dark/light theme,
      language, etc.

## Security & content protection

- [ ] Members-only content must be **protected from scraping**, not merely hidden.
- [ ] Access control enforced server-side, consistent with
      [Auth & user management](../03-functional-requirements/epics/auth-and-user-management.md).

## Privacy & SEO

- [ ] Tracking supports **campaign tracking** and traffic-source attribution (see
      [Tracking & Analytics](../03-functional-requirements/epics/tracking-and-analytics.md)).
- [ ] Ideally **no cookie banner** — choose an analytics approach that avoids it.
- [ ] Public content is **findable** (SEO), supporting reach goals.

## Open questions

- Concrete accessibility audit method and target AAA criteria.
- The specific analytics/consent approach that satisfies "no cookie banner".
