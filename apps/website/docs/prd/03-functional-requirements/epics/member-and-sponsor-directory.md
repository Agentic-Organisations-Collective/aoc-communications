# E6 — Member & Sponsor Directory

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts.

## Scope

A public directory of members (and sponsors), built automatically from the canonical
member records.

## Requirements

- Display **members** somewhere on the website; members can **opt out** via a
  **"do not display online"** flag.
- The member list is **built automatically** from the canonical source, not
  maintained separately.
- **Source of truth (decided):** member records are **Markdown + front matter in Git**
  at `aoc-board/packages/members` (see
  [Sources & References](../../sources-and-references.md)).
- **Avatar / profile imagery (decided):** loaded from **LinkedIn**.
- **Public fields (decided):** display name, country, company, avatar (from
  LinkedIn), and links (LinkedIn / website).
- **Display default (decided): opt-out** — members are **shown unless** they set the
  "do not display online" flag. Members must be informed and able to hide easily
  (see [Legal & Compliance](../../04-quality-and-compliance/legal-and-compliance.md)).
- **Sponsors** are also shown, possibly on the **same page** as the member list.

## Dependencies

- User data and opt-out flag: [E1](./auth-and-user-management.md).
- Sponsor records: [E3](./donations-and-sponsorships.md).

## Open questions

- How LinkedIn avatar loading handles members without a LinkedIn profile (fallback).
- Whether members and sponsors share one page or are separated.
