# Website Features and Content Process (Draft)

> **Draft notes — not requirements.** Translated from a spoken brainstorming
> transcript and lightly structured. Items are ideas and open questions, not
> decisions.

## Public vs. non-public content model

- In the age of AI, the idea is to **duplicate content deliberately**: public
  content lives in one file, protected content in another file.
- When they belong together (e.g. the public version is a short form of, or a
  reference to, a long members-only article), the two are linked to each other.
- Consistent duplication is acceptable — it makes it explicit what is public and
  what is not.
- A content creation and publishing process (agents, review steps, consistency
  checks) is set up on top of this model.

## User management and login

- Non-public content requires a **login**; a login requires **registration**; and
  registration implies **user management**.
- Not everyone may register freely — only **members** of the association (or those
  marked as such in user management) can register. New prospective members can also
  apply via registration.
- **Application flow:** A brand-new person who wants to become a member registers;
  this lands in an inbox where the board decides whether/when they become a member.
- **Pre-registered members:** If someone is already known to be a member and exists
  in user management (e.g. invited or onboarded offline, added manually by email),
  then when they register on the website they immediately get a login and are
  already a member. **Important use case.**

### Authentication and user data

- **Social login is required**: Google, GitHub, Microsoft, LinkedIn.
- Maintain a few user fields: email, phone, first/last name, company, possibly
  multiple addresses. Some of this might be sourced elsewhere. Keep it lean.
- After login, members can navigate a content area that is otherwise not publicly
  visible. Protection is critical — content must not be easily scraped.

## Website performance and accessibility

- Target a **Lighthouse score of 100/100/100/100** (all green) on both the public
  site and the logged-in site.
- **Accessibility: at least AA**, with as much AAA as possible.
- Honor and evaluate **browser signals**: high contrast, dark/light theme,
  language, etc.
- **Tech stack:** Astro and Svelte.
- **Auth provider:** Clerk could do everything, but a **European** (or open-source,
  ideally European) login provider is preferred. To be researched.

## Membership application and payment flow

1. A person applies for membership via an **online form** (personal data, name,
   contact, etc.) and can register with a social login so they can return later.
   Social login can pre-fill name/email.
2. The form includes fields per the **membership statutes**: researcher, public
   authority, company (which size), or individual. The **annual fee differs**
   accordingly and the correct fee is shown immediately, along with the benefits.
3. Optional free-text fields/questions: what they expect from the association and
   what they can contribute. Worth including even if it makes the form longer.
4. Submitting the form creates a **membership application**.
5. A **board member** approves the application and manages its status (possibly
   involving several people) via user management.
6. On approval, the user is activated as a **member on probation** ("auf Vorbehalt"):
   they can log in and view content, and receive an email prompting them to pay the
   membership fee.
7. They receive a **payment link** for the fee and pay online. Optionally they can
   add a small sponsor contribution.
8. Once payment is received, the user moves from **"on probation"** to **"activated"**.

## Donations and sponsorships

- **Donation form:** enter an amount, add a comment, provide company or name, and
  donate.
- **Sponsor form:** "I would like to become a sponsor."

## Tracking and analytics

- Goal is to generate reach, likely with heavy use of **LinkedIn**.
- Track users on the website and **where they come from**.
- Consider **tracking pixels** for ads (LinkedIn, Twitch, Google) to target better —
  open question whether ads are needed, but we do want to promote events.
- Tracking should support **campaign tracking** well.
- Ideally, **avoid a cookie banner**.

## Event recaps and content hierarchy

- Need a content type for **event recaps**, again public and non-public.
- A **content hierarchy** around an event: participants, sponsors, and speakers
  attach to the event; contributions/talks attach to speakers.
  - **Public:** contributions show image, title, abstract only.
  - **Members:** contributions also include slide PDFs and optionally video/photo
    documentation.
- Distinguish **event announcements** from **event documentation**:
  - Announcements can already include speakers, talks, and sponsors.
  - Documentation has much more content but a similar structure.
- Everything is done with **Markdown front matter** using different data models.

## Membership and sponsorship benefits

### Member benefits ("Become a member" / "Join in" page)

- Be visible as a member on the website and use the membership for own marketing.
- Preferred opportunity to contribute talks at events as an expert.
- Participate in the roles and bodies of the association, including the **curatorium**
  (which owns the subject-matter direction and curation of events) — i.e. have a say.
- Access to member-only event content.
- An **exchange forum** to share content relatively freely with other experts and
  learn from each other, without publishing everything to the open internet.

### Sponsor benefits

- We seek sponsoring to run event formats and high-level business exchange; sponsor
  income funds event technology, documentation, etc. — mainly for event formats.
- Sponsors get: **logo on the website**, **named as sponsor at events**, and the
  right to **attend member events** with knowledgeable people.

## Member and sponsor display

- Display **members** somewhere on the website; members can **opt out** of being
  shown (a "do not display online" flag in user management).
- The member list is **built automatically from user management**, not maintained
  separately.
- Per member, source data via APIs (e.g. Gravatar, LinkedIn profile). Use one or
  more social accounts as the basis for displayed data rather than storing
  everything ourselves.
- Show each member's **country** and, if provided, their **company**.
- **Sponsors** are also shown, possibly on the same page as the member list, and are
  ideally also in user management (effectively a customer CRM).

## Content automation and publishing

- Possibly a newsletter (open). Alongside public content, maybe a **blog** — or
  rather **in-depth professional articles** (more detailed in the closed area than
  in public). Long articles can also be public; short posts/news may or may not
  belong on the website.
- Possibly the website only carries professional articles; short versions are public
  or teased; everything else happens on **LinkedIn** (a LinkedIn page where all
  public contributions are published as link + post with post info).
- **Content automation** (similar to a "Marketing Automate OS"), built on **GitHub**:
  - A **content intake process via Issues**: choose type "new content", flag
    public/non-public, drop in audio, text, files, PDF, PowerPoint, etc.
  - A process then turns the intake into a cleanly structured **professional article**
    for the members' area and a cleanly formatted **public post**, cross-linked, in a
    **pull request**.
  - Merging the PR triggers a **pipeline** that republishes the Astro/Svelte site
    (member + public) and immediately generates and **schedules a LinkedIn post** for
    the association page (at least for the publication date).

## Content contribution and documentation

- Contributors can contribute not only talks but also **professional articles**.
- Try to capture **photo, video, and audio recordings** of contributions (even if
  hard for the website), so talks can be documented with video.
- Transcribe talks and, together with slide PDFs and the transcript, have an **agent
  write a professional article** for the members' area.
