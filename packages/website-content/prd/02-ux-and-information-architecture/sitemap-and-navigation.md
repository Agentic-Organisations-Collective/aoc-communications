# Sitemap & Navigation Structure

> 🟡 **DRAFT** — Provisional information architecture derived from the idea drafts.

## Core principle: public vs. members-only

The site has two content tiers, deliberately duplicated:

- **Public content** lives in its own files and is openly visible.
- **Protected (members-only) content** lives in separate files behind login.
- When related, a public item links to its members-only counterpart (e.g. a public
  teaser referencing a long members-only article), and vice versa.
- Members-only content must be **protected from scraping**, not just hidden.

## Provisional sitemap

```text
Public site
├── Home / self-presentation
├── About the association
├── Topics                         (public overviews of subject areas)
├── Events
│   ├── Event announcements        (speakers, talks, sponsors)
│   └── Event documentation/recaps (public view: image, title, abstract)
├── Articles / posts               (public professional articles or teasers)
├── Become a member / Join in      (benefits + application form)
├── Donate                         (donation form)
├── Become a sponsor               (sponsor form)
├── Members & sponsors directory   (auto-built from user management)
└── Login / Register

Members area (behind login)
├── Members dashboard
├── Member-only content & professional articles
├── Event documentation (full)     (slide PDFs, video/photo documentation)
├── Exchange forum
└── Account / profile & display settings
```

## Navigation notes

- Primary navigation exposes the public tier; the members area appears after login.
- The **member & sponsor directory** is built automatically from user management
  (see [member directory epic](../03-functional-requirements/epics/member-and-sponsor-directory.md)).
- Membership categories and fees surface on the **Become a member** page (see
  [membership application epic](../03-functional-requirements/epics/membership-application-and-payment.md)).

## Open questions

- Whether the site carries full short-form posts/news or only professional articles,
  with short forms living on **LinkedIn**.
- Whether a **blog** and/or **newsletter** are part of the IA.
