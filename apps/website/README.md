# website

The Agentic Organisations Collective (AOC) public + members website — a non-profit
association (Verein i.G.) for professional exchange about Software Factories and
Agent-OS systems.

This is an **app** (not a content package). Application code will live here; the
**documentation** lives under [`docs/`](./docs/README.md).

## Documentation

| Area | Path | Purpose |
| :---- | :---- | :---- |
| **Requirements (PRD)** | [`docs/prd/`](./docs/prd/README.md) | *What* the site must do and *why* — requirements only |
| **Decisions (ADRs)** | [`docs/decisions/`](./docs/decisions/README.md) | Tool/architecture options as proposals; decided by the technical team |
| **Architecture** | [`docs/architecture/`](./docs/architecture/README.md) | *How* it is built — tech stack, integrations, schemas |

> **Strict separation:** requirements (the *what/why*) are kept apart from solution
> specs (the *how*). Website **content** (copy, voice & tone, media) is **not** in
> this app — it is sourced from packages such as `website-content`, `brand-kit`,
> and `events`.
