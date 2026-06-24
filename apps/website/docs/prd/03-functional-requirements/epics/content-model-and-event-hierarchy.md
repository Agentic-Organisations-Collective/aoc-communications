# E4 — Content Model & Event Hierarchy

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.

## Scope

The public/non-public content model and the structured content hierarchy around
events.

## Public vs. non-public content model

- **Duplicate content deliberately**: public content lives in one file, protected
  content in another file.
- When they belong together (e.g. the public version is a short form of, or a
  reference to, a long members-only article), the two are **linked to each other**.
- **Public teaser policy (decided): optional** — the **author decides** per article
  whether a members-only article also gets a public teaser.
- Consistent duplication is acceptable — it makes explicit what is public and what
  is not.
- A content creation and publishing process (agents, review steps, consistency
  checks) sits on top of this model (see [E5](./content-automation-and-publishing.md)).

## Content types

- **Professional articles** (in-depth; more detailed in the closed area than in
  public). Long articles can also be public. The **blog is merged** into a single
  **Articles** section (decided).
- **Event recaps / documentation** (public and non-public).
- **Short posts/news** are published **on-site and on LinkedIn** (decided).

## Event content hierarchy

- Around an event: **participants, sponsors, and speakers** attach to the event;
  **contributions/talks** attach to speakers.
  - **Public:** contributions show **image, title, abstract** only.
  - **Members:** contributions also include **slide PDFs** and optionally
    **video/photo** documentation.
- Distinguish **event announcements** from **event documentation**:
  - **Announcements** can already include speakers, talks, and sponsors.
  - **Documentation** has much more content but a similar structure.
- **Event registration (decided):** the website only **announces** events and
  **links out** (e.g. LinkedIn event / external tool); **no on-site RSVP or
  ticketing** in the MVP.
- **Topics (decided):** topic values come from the shared
  **`aoc-foundations/packages/taxonomies`** package (see
  [Sources & References](../../sources-and-references.md)).
- **Schemas (decided):** front-matter data models are kept **local to
  website-content** — see
  [Content Schemas](../../../architecture/content-schemas.md).

## Implementation note

- Everything is done with **Markdown front matter** using different data models per
  content type.

- Single source of truth for past and present events:
  `aoc-curation/packages/events` (see
  [Sources & References](../../sources-and-references.md)).
- **Media (talk videos, photo documentation, slide PDFs) lives entirely in Git** in
  `aoc-curation/packages/events` (decided) — not on an external video host.
- **Speaker consent (decided):** obtain the speaker's consent **before publishing**
  their photos, video, or slides.

## Dependencies

- Anti-scraping protection for members-only content:
  [Non-Functional Requirements](../../04-quality-and-compliance/non-functional-requirements.md).
- Directory display of speakers/sponsors relates to
  [E6](./member-and-sponsor-directory.md).

## Open questions

- Whether the website carries only professional articles, with short forms teased
  and the rest on LinkedIn.
- Whether a **blog** and/or **newsletter** are part of the model
  ([ADR-0006](../../../decisions/0006-email-and-newsletter.md)).
