# AOC Website — Executive Summary

> 🔵 **UNDER REVIEW** — One-page manager's overview. For detail, see the
> [PRD](./README.md) and the [Roadmap & Milestones](./roadmap-and-phasing.md).

## What it is

The **digital home of the Agentic Organisations Collective (AOC)** — a non-profit
association (Verein, in formation) for professional exchange about **Software
Factories and Agent-OS systems**.

It is both a **public shop window** (who we are, our topics, our events) and a
**members-only area** (deeper content and event documentation behind a login). It is
English-only, content is **sourced from our existing Git packages** (not retyped into
the site), and member exchange happens on **LinkedIn / WhatsApp** — there is
deliberately **no forum and no newsletter**.

## What it's for (the 5 jobs)

1. **Self-presentation** — a credible public face for the association.
2. **Public content** — tease topics and events to attract participation.
3. **Member content** — gated articles, slides, and event documentation for members.
4. **Member acquisition** — an online apply-to-join flow.
5. **Online payment** — pay membership fees (and optional sponsor contributions) online.

The strategic aim: **grow reach (mainly via LinkedIn) and fund events through
memberships and sponsorships.**

## The three phases at a glance

| Phase | Theme | What a member/visitor can do | Why now |
| :---- | :---- | :---- | :---- |
| **1 — MVP** | Be present & lawful | Browse the public site and event announcements; **approved members log in** to view gated event documentation | Establish presence and credibility first; founding members are onboarded by hand |
| **2 — Membership lifecycle** | Open the funnel | **Anyone can apply, get approved, and pay online**; a **live member & sponsor directory** appears | Once gated content makes joining worthwhile, turn on acquisition + funding |
| **3 — Content engine & giving** | Scale & fund | Semi-automated article publishing + LinkedIn scheduling; **donations & sponsor sign-up**; AI "ask anything" over content | Scale content output and broaden the funding surface |

### Phase 1 — MVP (presence-first)

- **Outcome:** AOC is publicly visible and **lawful to operate**; manually approved
  members can view gated event documentation.
- **In it:** public pages (home, about, topics, **event announcements**); the event
  content model; a **read-only member area** (access via a manual allowlist — no
  self-sign-up yet); a **static founding members & sponsors directory**; basic
  (cookie-free) analytics; **legal pages** (Impressum, privacy, English statutes).
- **Must be true to launch:** legal pages live, member content protected from
  scraping, founding directory shown.
- **Not yet:** no public join flow, no online payment.

### Phase 2 — Membership lifecycle

- **Outcome:** new people can **apply → be approved → pay online**, end to end; the
  directory becomes **live and self-maintaining**.
- **In it:** self-registration & social login; the application form with the correct
  fee per membership category; board approval; "on probation → activated" once paid;
  the live opt-out directory; a press page.
- **Unlocks:** the acquisition and payment KPIs start accruing here.

### Phase 3 — Content engine & giving

- **Outcome:** content production is **semi-automated** and the **giving/sponsorship**
  surface is live.
- **In it:** GitHub-based article intake → agent-assisted drafting → publish pipeline
  → LinkedIn scheduling; donation form & sponsor sign-up; an AI chat that answers
  questions across the site's content (replaces a classic search box).

## The one strategic trade-off to know

We chose **presence-first**: the **funding engine (join + pay) goes live in Phase 2,
not at launch.** The bet is that there's little to *join* before there's gated content
worth paying for, and founding members are handled manually meanwhile. If "how do I
join/pay?" demand shows up during Phase 1, we pull the application form forward early.

## Deliberately out of scope

No members' forum, no email/newsletter, no on-site event ticketing — these live on
**LinkedIn / WhatsApp / external tools** by decision.
