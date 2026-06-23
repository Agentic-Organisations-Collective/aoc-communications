# E5 — Content Automation & Publishing

> 🟡 **DRAFT** — Functional requirements derived from the idea drafts. Envisioned as
> a "Marketing Automate OS" built on GitHub.

## Scope

The agent-assisted content intake, generation, review, and publishing pipeline.

## Intake

- A **content intake process via GitHub Issues**: choose type "new content", flag
  **public/non-public**, and drop in audio, text, files, PDF, PowerPoint, etc.

## Generation (agent-assisted)

- A process turns the intake into:
  - a cleanly structured **professional article** for the members' area, and
  - a cleanly formatted **public post**,
  - **cross-linked**, delivered in a **pull request**.

## Publishing pipeline

- Merging the PR triggers a **pipeline** that:
  - republishes the **Astro/Svelte** site (member + public), and
  - immediately generates and **schedules a LinkedIn post** for the association page
    (at least for the publication date).

> Canonical locations: GitHub org
> <https://github.com/Agentic-Organisations-Collective>, LinkedIn page
> <https://www.linkedin.com/company/agentic-organisations-collective/> (see
> [Sources & References](../../sources-and-references.md)).

## Contribution & documentation inputs

- Contributors can contribute not only talks but also **professional articles**.
- Capture **photo, video, and audio** recordings of contributions (even if hard for
  the website) so talks can be documented with video.
- Transcribe talks and, with slide PDFs and the transcript, have an **agent write a
  professional article** for the members' area.

## Channel strategy

- Public contributions are published on a **LinkedIn page** as link + post with post
  info; the website may carry only the professional articles, with short forms
  public or teased.

## Dependencies

- Output respects the public/non-public model in [E4](./content-model-and-event-hierarchy.md).
- LinkedIn scheduling + tracking relate to [E7](./tracking-and-analytics.md).

## Open questions

- Whether a **newsletter** is included.
- Review/consistency-check steps and who owns approval.
