# Sources & References (Single Sources of Truth)

> 🟡 **DRAFT** — Registry of canonical sources the website consumes. These live in
> **other repositories** of the AOC workspace; do **not** duplicate their content
> here. Reference them so changes propagate from the source.

## Single sources of truth (canonical, in-workspace)

> Each package below is **versioned** and **owns** its content. The website
> **consumes** these packages as its source and must **never duplicate** content
> that originates in another package — reference and pull it so changes propagate
> from the source.

| Domain | Canonical source (package) | Used by |
| :---- | :---- | :---- |
| **Statutes (Satzung)** | `aoc-governance/packages/statutes` | Membership categories & fees ([E2](./03-functional-requirements/epics/membership-application-and-payment.md)), [personas](./01-strategy-and-research/user-personas-and-competitor-benchmarks.md); German binding, English translation kept in sync |
| **Bylaws (Geschäftsordnung)** | `aoc-governance/packages/bylaws` | **Fee amounts** ([E2](./03-functional-requirements/epics/membership-application-and-payment.md)), bodies & roles (board approval, **curatorium** content approval), member benefits |
| **Public minutes** | `aoc-governance/packages/public-minutes` | Transparency / minutes area — board-approved, publishable records only ([sitemap](./02-ux-and-information-architecture/sitemap-and-navigation.md)) |
| **Design assets / brand** | `aoc-foundations/packages/brand-kit` | Site theme, logo, colours, brand voice |
| **Taxonomies (controlled vocabularies)** | `aoc-foundations/packages/taxonomies` | Subject classification & tags ([content model](./03-functional-requirements/epics/content-model-and-event-hierarchy.md), [content schemas](../architecture/content-schemas.md)) |
| **Events (per-event canonical)** | `aoc-curation/packages/events` | Public event pages **and** member-space documentation ([content model](./03-functional-requirements/epics/content-model-and-event-hierarchy.md), [sitemap](./02-ux-and-information-architecture/sitemap-and-navigation.md)); event **media** stored there in Git |
| **Press material** | `aoc-communications/packages/press` | Press page — releases, fact sheets, media contact ([sitemap](./02-ux-and-information-architecture/sitemap-and-navigation.md)) |
| **Member records** | `aoc-board/packages/members` | [Member & sponsor directory](./03-functional-requirements/epics/member-and-sponsor-directory.md) |

## Related packages (not canonical website sources)

> Either **derived** from a canonical source for publishing, or **internal** working
> material. The website does not treat these as the origin of truth, and the same
> content is **never authored twice**.

| Package | Relation | Role |
| :---- | :---- | :---- |
| `aoc-communications/packages/event-teasers` | Derived from `aoc-curation/packages/events` (+ curation) | Ready-to-publish teaser / announcement copy; **never** the canonical event source |
| `aoc-curation/packages/topics` | Internal planning backlog; feeds `events` planning | Proposed event themes under consideration — **not** the website's subject classification (that is `taxonomies`) |

## External resources

| Resource | Location |
| :---- | :---- |
| **GitHub organisation** | <https://github.com/Agentic-Organisations-Collective> |
| **GitHub org profile** | `.github/profile/README.md` |
| **LinkedIn page** | <https://www.linkedin.com/company/agentic-organisations-collective/> |
| **Domain** | `agentic-organisations-collective.eu` _(not yet configured on GitHub Pages)_ |

## Notes

- **Versioning.** Every canonical package is versioned and released independently;
  the website consumes **released** content and never copies it in. Statutes and
  bylaws are German-binding with English translations kept in sync (see each
  package's `VERSIONING.md`); `brand-kit` is versioned for stable distribution.
- **Statutes & bylaws** are legally binding in German; treat them as authoritative
  for membership categories, fees, bodies, and roles. The website must reflect, not
  redefine, them.
- **Public minutes** are published only when board-approved and non-sensitive — the
  website shows exactly what `public-minutes` releases, nothing more.
- **Brand assets** follow the "never upload a screenshot" rule — reference the
  `brand-kit` source rather than copying logos/imagery.
- **Taxonomies vs. topics (no duplication).** `aoc-foundations/packages/taxonomies`
  is the **controlled vocabulary** used to classify and tag website content;
  `aoc-curation/packages/topics` is a **planning backlog** of proposed event themes
  that feeds event planning. They do not overlap — one is the fixed classification
  scheme, the other a pipeline of candidate event ideas. The public **Topics** page
  and all content tags use **taxonomies**.
- **Events vs. event-teasers (no duplication).** `aoc-curation/packages/events` is
  the **canonical** per-event source (program, speakers, media, content notes), used
  for event pages and **member-space documentation**. `event-teasers` holds
  **derived** public teaser copy and is **explicitly never the canonical source**.
  The website pulls announcements from `event-teasers` and full documentation from
  `events`; the facts are authored once, in `events`.
- **Press** content (releases, fact sheets, media contact) comes from
  `aoc-communications/packages/press`, kept consistent with approved public
  messaging.
- **Member records** are Markdown + front matter in `aoc-board/packages/members`;
  **avatars** are loaded from LinkedIn.
- **Schemas.** Front-matter **schemas** for website content are defined in the
  website architecture docs ([Content Schemas](../architecture/content-schemas.md)).
- **LinkedIn** is the primary distribution channel (see
  [E5](./03-functional-requirements/epics/content-automation-and-publishing.md) and
  [E7](./03-functional-requirements/epics/tracking-and-analytics.md)).
- The **domain** `agentic-organisations-collective.eu` is intended but **not yet
  configured on GitHub Pages**.
