# Website placeholder (coming soon)

Temporary static **coming-soon** page for the public website: the brand mark
(Papyrus Cream) and the name in the brand display font (**Kalam**), centered on an
Electric Cobalt Blue (`#1D4ED8`) background. It exists so the public tier can go live
on **GitHub Pages** immediately, ahead of the real site (Astro + Svelte, see
[`../docs/decisions/0008-frontend-framework.md`](../docs/decisions/0008-frontend-framework.md)).

## Files

- `index.html` — the page (inline SVG logo + name, no external/runtime dependencies).
- `fonts/kalam-latin-400.woff2`, `fonts/kalam-latin-700.woff2` — the brand display
  font **Kalam** (Google Fonts, OFL), **self-hosted** (latin subset) so no request
  goes to a third-party CDN — keeps the page GDPR-clean and offline-robust.
- `favicon.svg` — brand mark (blue) for the browser tab.
- `CNAME` — custom domain published to Pages: `www.agentic-organisations-collective.eu`.
- `.nojekyll` — disables Jekyll processing on Pages.

## How it deploys

The workflow [`.github/workflows/deploy-pages.yml`](../../../.github/workflows/deploy-pages.yml)
uploads this folder as the Pages artifact and deploys it on every push to `main`
that touches `apps/website/placeholder/**` (or via **Run workflow** / `workflow_dispatch`).

## One-time manual setup (cannot be done from the repo)

1. **Enable Pages with the GitHub Actions source:** repo → *Settings* → *Pages* →
   *Build and deployment* → *Source: GitHub Actions*.
2. **DNS for the custom domain** (`agentic-organisations-collective.eu`) — at the
   domain provider:
   - `www` → `CNAME` → `agentic-organisations-collective.github.io`
   - apex `@` → four `A` records to GitHub Pages:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
     (and the matching `AAAA` records if IPv6 is used).
   - The canonical host is `www` (apex redirects to `www`), per
     [ADR-0001](../docs/decisions/0001-hosting-model.md).
3. After DNS resolves, enable **Enforce HTTPS** in *Settings* → *Pages*.

> Until the custom domain's DNS is live, the site is reachable at the project URL
> `https://agentic-organisations-collective.github.io/aoc-communications/`. Because a
> `CNAME` is set, that project URL will redirect to the custom domain once DNS is in
> place.

## Replacing the placeholder with the real site

When the Astro + Svelte site is ready, swap the workflow's *Upload static placeholder*
step for a build (e.g. `pnpm install` + `astro build`) and point
`upload-pages-artifact` at the build output (e.g. `apps/website/dist`). Keep `CNAME`
in the published output (Astro: place it in `public/`).
