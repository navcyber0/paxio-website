# Changelog — paxio-website

Internal tracking only — for audit/reference purposes. Not linked from or shown anywhere on the
live site (www.paxio.in). Whoever makes a notable change to this repo bumps `VERSION` and adds an
entry here in the same commit (or same small batch of commits), following [[paxio-feedback-changelog-per-release]]'s
pattern from the main Paxio app repo, adapted to this site.

**Versioning**: `MAJOR.MINOR.PATCH`. Bump MINOR for a new page/feature/section, PATCH for a fix or
small content change, MAJOR reserved for a full redesign or restructuring. Newest entry at the top.

## [1.3.0] — 2026-10-05
### Added
- Blog post `blog/mod-apk-cracked-games-malware.html` ("Are Mod APKs Safe? What Parents Should Know
  About Game Mods"), with hero + 1200x630 OG image, a card on `blog/index.html` and a `sitemap.xml` entry.

## [1.2.3] — 2026-10-02
### Added
- **UTM tags on every "Get it on Google Play" CTA site-wide** (`utm_source=website&utm_medium=referral&utm_campaign=site_cta`), so the app's GA4 property (`kids-safe-nav`) can finally distinguish "installed after clicking a website CTA" from Play Store organic search/browse and the still-unattributed `(direct)` bucket. Google Play's Install Referrer API passes these through to Firebase/GA4 automatically at install time — no deep-linking or app-side change needed. Tagged 121 links across 72 public pages (every root/blog/help/product page that has a download CTA; the 10 legacy standalone screen pages like `app-blocking.html` have no CTA at all, superseded by their `/product/kids-*` equivalents, so nothing to tag there). Same `utm_source=website` scheme is distinct from the separate per-platform `utm_source=reddit|facebook|instagram|x|youtube` tags going on social bio links.

## [1.2.2] — 2026-10-02
### Fixed
- **GA4 (Google Analytics) was never actually wired up to the live site — zero sessions recorded, ever, despite the `www.paxio.in` GA4 property existing in console.** Discovered while investigating app-install lead-source attribution: Search Console showed real organic traffic (clicks/impressions on `paxio.in` throughout September) that GA4 had no record of at all. Mixpanel was correctly present on every public page (enforced by `.github/workflows/check-mixpanel.yml`), but the GA4 `gtag.js` snippet was never added anywhere in the repo. Added the snippet (measurement ID `G-0T28PK25EL`) to all 82 public pages (root, `blog/`, `help/`, `product/`), same insertion point as Mixpanel (right before `</head>`). Also extended the CI workflow (renamed to `check-analytics.yml`'s job set — same file, now checks both snippets) so a new page missing either analytics tag fails the build.

## [1.2.1] — 2026-10-01
### Removed
- Homepage footer's "As featured on" launch-platform badges (LaunchIgniter, LiftOff, Launchstag).

## [1.2.0] — 2026-10-01
### Added
- Blog post `blog/kids-screen-time-on-weekends.html` ("Kids' Screen Time on Weekends: How Much Is
  Too Much?"), with hero + 1200x630 OG image, a card on `blog/index.html` and a `sitemap.xml` entry.

## [1.1.0] — 2026-09-30
### Added
- Custom branded 404 page (`404.html`) replacing GitHub Pages' default error page — all internal
  links use root-absolute paths so they resolve correctly regardless of the missing URL's depth.
- Digital Asset Links file (`.well-known/assetlinks.json`) enabling Android App Links verification
  and Google Sign-In credential sharing for `com.paxio`.
- `.nojekyll` — required for GitHub Pages to actually serve the `.well-known/` path (Jekyll's
  default build silently excludes any dotfile/dotfolder otherwise).
### Fixed
- Broken internal link on `what-is-a-parental-control-app.html` (bare relative path to a post
  that actually lives under `/blog/`).
### Changed
- The Roblox blog post's "check your kid's app" sidebar callout now links directly to App
  Checker's `com.roblox.client` page instead of the tool's generic homepage.

## [1.0.0] — baseline
Existing live site as of the start of this tracked history — full page set (product pages, blog,
help center, comparison pages), Mixpanel analytics, GA4/Firebase, ASO screenshot assets, short/long
Play Store descriptions.
