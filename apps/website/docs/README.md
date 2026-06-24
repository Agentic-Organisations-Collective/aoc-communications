# Website Documentation

Documentation for the AOC `website` app, organised to keep **requirements**
strictly separate from **solution specs** and **decisions**.

## Layout

| Folder | Holds | Answers |
| :---- | :---- | :---- |
| [`prd/`](./prd/README.md) | Product Requirements (PRD) | *What* & *why* |
| [`decisions/`](./decisions/README.md) | Architecture Decision Records (ADRs) | *Which option* (proposed, decided later) |
| [`architecture/`](./architecture/README.md) | Architecture & technical specs | *How* |

## Rules

1. **Requirements vs. solution.** Keep the *what/why* (PRD) apart from the *how*
   (architecture). Do not mix tech choices into requirement pages.
2. **Decisions are proposals first.** Tool/architecture choices live in `decisions/`
   as ADRs with pros/cons and stay `Proposed` until the technical team decides.
3. **Content is sourced, not stored.** Copy, voice & tone, brand, events, and member
   data come from other packages (see
   [Sources & References](./prd/sources-and-references.md)); the docs reference them
   rather than duplicating them.

## Start here

New readers should begin with the [PRD](./prd/README.md).
