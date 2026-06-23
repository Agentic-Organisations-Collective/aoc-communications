# Sources & References (Single Sources of Truth)

> 🟡 **DRAFT** — Registry of canonical sources the website consumes. These live in
> **other repositories** of the AOC workspace; do **not** duplicate their content
> here. Reference them so changes propagate from the source.

## Single sources of truth (in-workspace)

| Domain | Canonical source | Used by |
| :---- | :---- | :---- |
| **Statutes (Satzung)** | `aoc-governance/packages/statutes` | Membership categories & fees ([E2](./03-functional-requirements/epics/membership-application-and-payment.md)), [personas](./01-strategy-and-research/user-personas-and-competitor-benchmarks.md) |
| **Bylaws (Geschäftsordnung)** | `aoc-governance/packages/bylaws` | Bodies & roles (board approval, curatorium), member benefits |
| **Design assets / brand** | `aoc-foundations/packages/brand-kit` | [Brand assets](./05-content-and-media-assets/brand-assets.md) |
| **Events (past & present)** | `aoc-curation/packages/events` | [Content model & event hierarchy](./03-functional-requirements/epics/content-model-and-event-hierarchy.md), [sitemap](./02-ux-and-information-architecture/sitemap-and-navigation.md) |

## External resources

| Resource | Location |
| :---- | :---- |
| **GitHub organisation** | <https://github.com/Agentic-Organisations-Collective> |
| **GitHub org profile** | `.github/profile/README.md` |
| **LinkedIn page** | <https://www.linkedin.com/company/agentic-organisations-collective/> |
| **Domain** | `agentic-organisations-collective.eu` _(not yet configured on GitHub Pages)_ |

## Notes

- **Statutes & bylaws** are legally binding in German; treat them as authoritative
  for membership categories, fees, bodies, and roles. The website must reflect, not
  redefine, them.
- **Brand assets** follow the "never upload a screenshot" rule — reference the
  `brand-kit` source rather than copying logos/imagery.
- **Events** content on the website is produced from `aoc-curation/packages/events`.
- **LinkedIn** is the primary distribution channel (see
  [E5](./03-functional-requirements/epics/content-automation-and-publishing.md) and
  [E7](./03-functional-requirements/epics/tracking-and-analytics.md)).
- The **domain** `agentic-organisations-collective.eu` is intended but **not yet
  configured on GitHub Pages**.
