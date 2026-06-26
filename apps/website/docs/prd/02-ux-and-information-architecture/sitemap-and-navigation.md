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
├── Topics                         (public overviews; from taxonomies package)
├── Events
│   ├── Event announcements        (speakers, talks, sponsors; links out for RSVP)
│   └── Event documentation/recaps (public view: image, title, abstract)
├── Articles                       (single section; blog merged in)
├── Press                          (later phase; from aoc-communications/press)
├── Become a member / Join in      (benefits + public fees + application form)
├── Donate                         (later phase)
├── Become a sponsor               (later phase)
├── Members & sponsors directory   (built from aoc-board/packages/members)
└── Login / Register

Members area (behind login)
├── Members dashboard
├── Member-only content & professional articles
├── Event documentation (full)     (slide PDFs, video/photo documentation)
└── Account / profile & display settings
```

## Navigation notes

- Primary navigation exposes the public tier; the members area appears after login.
- The **member & sponsor directory** is built automatically from the canonical member
  records in `aoc-board/packages/members`
  (see [member directory epic](../03-functional-requirements/epics/member-and-sponsor-directory.md)).
- Membership categories and fees surface on the **Become a member** page (see
  [membership application epic](../03-functional-requirements/epics/membership-application-and-payment.md)).

## Decisions & open questions

- **Decided:** content is **English only**; short-form posts/news live **on-site and
  on LinkedIn**. **No on-site forum** — member-to-member exchange happens off-site
  (e.g. WhatsApp communities / LinkedIn).
- **Decided:** **no on-site search** in the MVP; a future **AI chat ("ask anything")**
  across the content is preferred over a classic search (later phase).
- **Decided:** events are **announcement-only with link-out** (no on-site RSVP).
- **Decided:** **blog is merged** into a single **Articles** section; a **Press**
  page is added in a later phase; **no contact page**; **ads** decision is **later**.
- **Open:** exact placement of Press and directory in the global navigation.
