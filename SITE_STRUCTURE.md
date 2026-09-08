# paxio-website — site structure & conventions

This documents how the site is actually organized as of 2026-09-08, so new pages follow the
existing pattern instead of drifting. This is a static site (plain HTML/CSS, no build step),
deployed via GitHub Pages from the `main` branch.

## Top-level layout

```
/                           Homepage (index.html)
/pricing.html               Pricing page
/why-paxio.html             Positioning/differentiation page
/features.html, /setup.html, /product-tour.html, /benefits.html   Older marketing pages
/faq.html, /contact.html    Utility pages
/privacy-policy.html, /terms-of-service.html, /delete-account.html, /delete-data.html
/paxio-vs-qustodio.html, /paxio-vs-family-link.html   Head-to-head comparison landing pages

/product/                   Individual feature/control pages (see below)
/blog/                      Blog index + posts (see below)
/help/                      Help Center articles + their screenshot images
/store-assets/              Logo, feature graphics, Play Store assets
/marketing/                 Internal working docs — drafts, SEO plans, outreach copy.
                             NOT part of the live site; never linked from any page.
```

## `/product/` — feature pages

**Purpose**: one dedicated landing page per control/feature, each targeting a real search
phrase (e.g. "disable internet on kid's phone") rather than living only as a section on the
homepage. This directory was introduced 2026-09-08 — these pages previously lived flat at the
site root (`/screen-time-limit.html` etc.), which is why redirect stubs still exist there (see
"Redirects" below).

**Files**:
- `index.html` — the hub/overview page ("How Paxio Works"), reachable at `paxio.in/product/`.
  Shows a condensed preview of every control with a "More on X →" link to its own dedicated page.
- `kids-screen-time-limit.html`, `kids-bedtime-schedule.html`, `kids-internet-pause.html`,
  `kids-streak-bonus.html`, `kids-app-blocking.html`, `kids-content-filtering.html`,
  `kids-parent-dashboard.html`, `kids-child-dashboard.html`, `kids-reports-screen.html` — one page
  per feature.

**Naming convention**: every detail-page filename is prefixed `kids-`, not `kid-` (added
2026-09-08, corrected same day after checking the actual keyword research in
`marketing/seo-improvement-plan.md` — every target phrase there uses plural "kids," e.g. "bedtime
schedule android phone kids," never singular "kid"). `index.html` (the hub) does NOT get the
prefix — it's not a keyword-targeting page itself.

**Per-page structure** (every detail page follows this exact section order):
1. Hero (`<section style="padding-bottom:0">`) — H1 + one paragraph, leading with the natural
   search phrase, not internal product language ("Block apps on your kid's phone with a single
   tap...", not "Every installed app, Allowed or Blocked...").
2. Showcase (`<section>` with `.showcase-row`) — same lead sentence restated, real screenshot in
   `.help-shot` figure.
3. "The details" (`<section style="padding-top:0">`, `.specifics-grid`) — 2-3 `.specifics-item`
   blocks, each a sub-heading + short intro + bullet list.
4. "Setup" (`.setup-steps`) — exactly 3 numbered steps.
5. FAQ (`.faq-list`, native `<details>`) — same Q&A also duplicated in the page's `FAQPage`
   JSON-LD schema in `<head>`, word-for-word.
6. Single CTA (`Try Paxio free` + `See all controls`) — **at the very bottom**, after the FAQ,
   never at the top. (Moved from top to bottom 2026-09-08 for consistency.)

**Explicitly removed** (2026-09-08): an "Explore more / Other Paxio controls" section used to sit
between Setup and FAQ on every detail page, linking to all the sibling pages. Removed as
redundant — the Product nav dropdown already covers this, and the hub page's own job is to be
the single "see everything" cross-link surface. Don't re-add it.

**Real screenshots, not stale ones**: every `.help-shot` image must reflect the actual current
app behavior. This project has twice caught a screenshot showing an outdated mechanic (a stale
streak-bonus card showing the old "5 days → +20 min, needs approval" flow; a stale bedtime screen
mentioning a dim-warning that was later removed from the app). Before reusing any existing image
in `help/images/`, verify what it actually shows against current product truth — don't assume an
existing asset is still accurate just because it exists.

## Redirects (old flat URLs → `/product/`)

GitHub Pages serves static files only — there's no server-side redirect config available. The
10 old flat-URL files at the site root (`screen-time-limit.html`, `bedtime-schedule.html`,
`internet-pause.html`, `streak-bonus.html`, `app-blocking.html`, `content-filtering.html`,
`parent-dashboard.html`, `child-dashboard.html`, `reports-screen.html`, `controls.html`) are now
**redirect stubs**, not real pages — each is a minimal HTML file with:
- `<meta http-equiv="refresh" content="0; url=...">` pointing to the new `/product/...` URL
- `<link rel="canonical" href="...">` pointing to the same new URL (the actual SEO-relevant signal)
- `<meta name="robots" content="noindex">`
- A plain fallback link, in case the refresh doesn't fire

**Keep these stubs** — don't delete them, even though nothing links to them anymore internally.
They exist for anyone with an old bookmark, an old external backlink, or a stale search-index
entry from before the `/product/` move. If the URL structure changes again later, update the
stubs' target rather than removing them.

## `/blog/`

- `index.html` — post grid.
- One file per post, e.g. `blog/cyberbullying-what-it-looks-like.html`.
- Every post: real (license-verified, non-stale) Unsplash photo, a genuinely recent (<12mo)
  primary-source stat where one fits (skip rather than force one), `BlogPosting` JSON-LD.
- Any post comparing/naming a competing product by name must carry the standing disclaimer
  paragraph (see `best-parental-control-apps-features-compared.html` for the exact wording) —
  established 2026-08-14, applies to every future post that names a competitor.
- Drafts live in `marketing/blog-drafts/` until approved — converting one to a live
  `blog/*.html` page is always a separate, manual, explicitly-approved step.

## Shared nav (appears identically on every page)

The `<nav class="nav">` block — brand logo, the "Product" mega-menu dropdown (mirrors the
`/product/` file list above exactly, grouped into 3 columns: Limits & Time / Safety Controls /
Visibility & Reports), then Why Paxio / Pricing / Blog / Contact / Get Paxio — is duplicated
verbatim into every single HTML file (no templating/includes on a static site). **When adding,
renaming, or removing a `/product/` page, the nav-mega block must be updated in every file that
has it** — currently that's every page site-wide. Use a script-based find/replace across `*.html`,
`blog/*.html`, and `product/*.html`, not manual per-file edits — this project's history has
several examples of exactly this kind of sitewide mechanical update.

Right after `</nav>` on every page there's a small inline script closing the Product dropdown on
an outside click:
```html
<script>
document.addEventListener('click', function (e) {
  document.querySelectorAll('.nav-dropdown details[open]').forEach(function (d) {
    if (!d.contains(e.target)) d.removeAttribute('open');
  });
});
</script>
```
The selector must be `.nav-dropdown details[open]`, not `.nav-dropdown[open]` — the `open`
attribute lives on the child `<details>` element, not the wrapper div. (This was shipped broken
once with the wrong selector — verify via actual DOM testing, not just "the script exists," if
touching this again.)

## Path conventions

- Root-level pages reference assets/other pages with bare relative paths: `style.css`,
  `store-assets/...`, `help/images/...`, `pricing.html`.
- `/blog/*.html` and `/product/*.html` are one level deep — they reference root-level things with
  a `../` prefix: `../style.css`, `../store-assets/...`, `../pricing.html`.
- `/help/*.html` follows the same one-level-deep `../` pattern.
- Files within the same directory (e.g. one `/product/` page linking to another) use bare
  filenames, no prefix.

## Pricing (single source of truth: `pricing.html`)

Free: 1 child profile, daily screen time limit, block up to 5 apps, unblock up to 3 content
categories, parent PIN, weekly reports (3 stats, 30-day history).
Pro: ₹499/mo or ₹4,999/yr (44%/54% off a real ₹899/₹10,788 base — these discount percentages are
computed from an actual higher price, not decorative), up to 3 child profiles, unlimited app
blocking + per-app time limits, all content categories, bedtime/schedule locks, remote internet
pause, streak bonus, weekly reports (7 stats, 1-year history), priority support.

**Currency is INR, not USD** — this site briefly ran USD pricing in early September 2026; it was
reverted. If a stale `$` figure ever resurfaces anywhere, it's a regression, not a live change.

## Structured data conventions

- Every `/product/*.html` and most `/blog/*.html` pages carry a `FAQPage` JSON-LD block in
  `<head>` whose Q&A text matches the visible `.faq-list` content verbatim — don't let these two
  drift apart when editing one.
- The homepage carries `MobileApplication` + `ItemList` (site nav) JSON-LD. The
  `MobileApplication` schema's `offers.priceCurrency` must stay `"INR"`.
- Comparison pages (`paxio-vs-*.html`) carry `FAQPage` JSON-LD only, no `BlogPosting`/`Article`
  type — they're landing pages, not blog content.

## Verification workflow

For any HTML/content change: serve locally (`python3 -m http.server` from the repo root) and
check via the Claude Browser tools (`get_page_text`, `read_network_requests`, direct DOM checks
via `javascript_tool`) rather than assuming a find/replace worked — this project has caught real
bugs (broken nav-dropdown selector, stale screenshots, broken internal links after moving files)
that a naive "the script ran successfully" check would have missed. After a structural change
(moving/renaming files), always do a full site-wide grep for the old filename before considering
it done — a single missed reference anywhere breaks silently on a static site (no build step to
catch a bad link).
