# Changelog — paxio-website

Internal tracking only — for audit/reference purposes. Not linked from or shown anywhere on the
live site (www.paxio.in). Whoever makes a notable change to this repo bumps `VERSION` and adds an
entry here in the same commit (or same small batch of commits), following [[paxio-feedback-changelog-per-release]]'s
pattern from the main Paxio app repo, adapted to this site.

**Versioning**: `MAJOR.MINOR.PATCH`. Bump MINOR for a new page/feature/section, PATCH for a fix or
small content change, MAJOR reserved for a full redesign or restructuring. Newest entry at the top.

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
