# Content Schemas (Front-Matter Data Models)

> 🟡 **DRAFT** — Proposed Markdown front-matter data models. **Decided:** schemas are
> kept **local to `website-content`** (not in the shared `schemas` package). Topic
> values, however, come from the shared
> **`aoc-foundations/packages/taxonomies`** package.

Each content type is authored as Markdown with front matter. Below are the proposed
fields; refine before implementation.

## Event (announcement & documentation)

```yaml
type: event
slug: 2026-07-14-software-factories-berlin
title: string
date: ISO-8601
location: string
status: announcement | documentation
visibility: public            # event records are public
topics: [taxonomy-id]         # from aoc-foundations/packages/taxonomies
sponsors: [sponsor-id]
speakers: [speaker-id]
summary: string               # public abstract
```

> Source of truth for events (incl. media): `aoc-curation/packages/events`.

## Speaker

```yaml
type: speaker
id: string
name: string
company: string
links: { linkedin: url, website: url }
contributions: [talk-id]
```

## Contribution / talk

```yaml
type: talk
id: string
speaker: speaker-id
title: string
abstract: string              # public
image: path
slides: path                  # members-only (PDF, in Git)
video: path                   # members-only (in Git)
photos: [path]                # members-only (in Git)
```

## Article (public and/or members-only)

```yaml
type: article
slug: string
title: string
visibility: public | members
teaser_of: slug               # optional cross-link (teaser policy is per-author)
topics: [taxonomy-id]
body: markdown
```

## Member (directory)

```yaml
# Source of truth: aoc-board/packages/members (Markdown + front matter)
type: member
id: string
display_name: string
country: string
company: string
links: { linkedin: url, website: url }
avatar: linkedin              # avatar loaded from LinkedIn
display: true                 # opt-out: shown unless set false
```

## Notes

- **Public/non-public duplication** is modelled via separate files and an optional
  `teaser_of` cross-link (the public teaser is **optional, author's choice**).
- Topic IDs are validated against the **taxonomies** package.
