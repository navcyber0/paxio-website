# SEO improvement plan — started 2026-09-08

Triggered by: only 200+ impressions in Search Console, ranking ~page 13 for target terms. This
plan replaces guesswork with an actual audit (see "Audit findings" below) and a prioritized fix
list. Cross-reference `paxio_project_marketing_seo_plan` (memory) for what was already done as of
2026-08-31 — this file picks up from there, doesn't repeat it.

## Official social profiles (reference list)

Canonical list of Paxio's live social accounts — use these exact URLs anywhere a profile link is
needed (directory submissions, Schema.org `sameAs`, footer links, outreach emails), rather than
guessing or reconstructing a handle.

- **Facebook**: https://www.facebook.com/paxio.in
- **Instagram**: https://www.instagram.com/paxio.in/
- **YouTube**: https://www.youtube.com/@Paxio-in
- **X/Twitter**: https://x.com/paxioin
- **Reddit**: account created and actively posting (2026-08-26) — no fixed public profile URL to
  list here since Reddit presence is per-post, not a branded profile page in the same sense.

Worth adding these as `sameAs` entries in the homepage's `MobileApplication` JSON-LD block — this
is a real, low-effort SEO win (helps Google associate the social profiles with the brand entity)
that isn't yet in the on-page action list above; add it as a task if not already done by the time
this is picked up.

## Audit findings (2026-09-08, via live WebSearch + direct site inspection)

1. **Branded search works fine.** `"paxio" parental control app` returns paxio.in on page 1,
   alongside Qustodio/TechRadar/Canopy/SafeWise/Hoverwatch. Confirms indexing itself isn't broken —
   the problem is ranking for anything non-branded.
2. **Zero blog posts rank for their own target long-tail keywords.** Tested the bedtime-schedule
   post's target phrase directly — paxio.in doesn't appear anywhere in results; the space is
   dominated by Boomerang, Kiddoware, Constant Kid, NexSpy, and Google's own support docs, all of
   which have years of domain history Paxio doesn't have yet.
3. **Off-page/backlink work has never actually started**, despite being identified as "higher
   leverage than on-page tweaks for a brand-new domain" back on 2026-08-02 (see
   `paxio_project_marketing_seo_plan` section 3). No AlternativeTo/Product Hunt/BetaList/SaaSHub
   listings exist. This is almost certainly the single biggest reason impressions are still this
   low — a domain with zero backlinks has very little to signal relevance/authority to Google
   regardless of how good the on-page content is.
4. **Possible stale index snapshot**: a live web search's own summary of paxio.in described it as
   still "coming soon to Google Play" with placeholder copy — that messaging hasn't been true on
   the live site for weeks (the real Play Store link has been live since 2026-08-31 per the
   resolved blocking-dependency note). Worth confirming directly in Search Console whether the
   homepage's last-crawled snapshot is current, and using "Request Indexing" on the homepage and
   any recently-changed page if it's stale.
5. **GitHub Pages mirror (`navcyber0.github.io`) is not a duplicate-content risk** — checked
   directly, it 404s (no site deployed there), so it isn't competing with `www.paxio.in` in the
   index. Ruled out, not a fix needed.
6. **Technical basics are already solid** (per the 2026-08-02 audit, re-confirmed): canonical
   tags, OG/Twitter meta, JSON-LD, robots.txt, HTTPS, one `<h1>` per page, complete sitemap with
   per-post blog entries. Nothing broken here — the gap is authority + content depth, not technical
   hygiene.

**Bottom line**: this isn't a "fix the website" problem, it's a "the website has no authority yet"
problem. A brand-new domain competing against sites with years of backlinks and domain history
needs off-page signal, not more on-page polish, to move past page 10+. On-page work below still
matters (it's what off-page traffic converts into rankings for), but it's not the bottleneck.

## Priority keywords

Chosen for realistic ranking odds on a new domain — long-tail, specific intent, low-to-medium
competition — not head terms like "parental control app" (unwinnable short-term, dominated by
Qustodio/Bark/Family Link/aggregator roundups with years of authority).

### Tier 1 — long-tail, directly matches existing/plannable blog content (best near-term odds)
- `bedtime schedule android phone kids` / `bedtime lock app for kids android`
- `block apps on child's phone without rooting`
- `on-device content filter android kids` (Paxio's real differentiator — cloud-filtering
  competitors can't legitimately claim this)
- `screen time limit vs app blocking difference`
- `parental control app that doesn't track location`
- `ai chatbot risks for kids` / `is chatgpt safe for my child` (rides the AI-safety post's topical
  momentum — genuinely trending search interest, low existing competition specific to the
  kids-safety angle)
- `cyberbullying warning signs parent` (matches the published cyberbullying post)

### Tier 2 — India-specific + pricing-intent (underserved by the mostly-US/UK-focused competitor
content found in this audit — real gap)
- `parental control app india price`
- `parental control app under 500 rupees` / `screen time app india free`
- `qustodio alternative india` / `qustodio price india`
- `family link vs paxio` (comparison searches convert well — someone searching this is already
  evaluating, not just browsing)
- `best parental control app for xiaomi/realme/oppo android` — a real, specific pain point
  surfaced in this audit's own research (aggressive battery optimization on Indian-market phone
  brands kills background enforcement apps) that's genuinely underserved content-wise; worth its
  own post if Paxio's battery-optimization handling is solid enough to write about honestly

### Tier 3 — comparison/commercial-intent (the format competitors currently own via listicles)
- `best parental control app 2026 comparison` — already targeted by
  `best-parental-control-apps-features-compared.html`; needs the off-page push below to have a
  chance, on-page alone won't out-rank TechRadar/SafeWise's domain authority
- `qustodio vs paxio`, `google family link vs paxio` — dedicated one-on-one comparison pages
  (narrower, easier to rank than a 6-way comparison, and matches how people actually search when
  they already use a specific competitor and are evaluating switching)

### Explicitly not targeting yet
- `parental control app`, `best parental control app`, `screen time app` (bare head terms) — years
  away from realistic on a new domain with no backlinks; revisit once Tier 1/2 show real traction.

## Action plan

### A. Off-page / authority (highest priority — this is the actual bottleneck)
1. **Directory submissions** (free, ~1-2 hours total, real backlinks): AlternativeTo, SaaSHub,
   Product Hunt (full launch, not just a listing). These are quick, free, and the single fastest
   way to get real external links pointing at paxio.in. (BetaList dropped 2026-09-08 — its real
   submission path turned out to be a paid product-showcase placement, not a free listing. Slant.co
   also dropped 2026-09-08 — confirmed not an active/reachable domain.)
2. **Reach out to existing "best parental control apps" roundup authors** (Hoverwatch, Canopy,
   SafeWise, ParentalEdge, Boomerang — all surfaced in this audit's own competitor research) asking
   to be considered for inclusion, with a specific honest angle (on-device filtering, no location
   tracking, INR pricing for India) rather than a generic "please add my app" ask. Lower
   response-rate but each hit is a high-authority backlink.
3. **Two dedicated one-on-one comparison pages** (`paxio-vs-qustodio.html`,
   `paxio-vs-family-link.html`) — narrower target than the existing 6-way comparison post, matches
   real switching-intent search phrasing, and gives something specific to link to when doing
   outreach in item 2.
4. Continue the Quora-answer engagement already running via `paxio-lead-monitor` — doesn't create
   backlinks (Quora links are nofollow) but does build indexed brand-mention volume, which
   Google's algorithm does weight as a secondary trust signal over time.

### B. On-page (keep doing, but understand it's not the bottleneck alone)
1. Verify Search Console's cached homepage snapshot is current; use "Request Indexing" on the
   homepage and pricing page specifically, given finding #4 above.
2. Write the two comparison pages from A.3 with the exact Tier-2/3 keyword phrasing in the title,
   H1, and first paragraph (not buried) — this is the fix for finding #2 (posts not ranking for
   their own target phrase) combined with the authority push, not a replacement for it.
3. Internal linking pass: every blog post should link to at least 2 other relevant posts and to
   the pricing/comparison pages — current posts are mostly linking only back to the homepage,
   which under-uses the topical-depth signal Google rewards multi-page sites for.
4. Add `FAQPage` schema to the pricing page (common questions like "is there a free plan," "does
   it work offline," "is my data private") — cheap to add, directly matches how competitor content
   (many of which use FAQ schema) shows up as rich results.
5. One new post targeting the Xiaomi/Realme/Oppo battery-optimization angle (Tier 2) — genuinely
   underserved, specific, and plays to a real Android-fragmentation pain point most competitor
   content glosses over.

### C. Verification / ongoing tracking
1. Re-check Search Console impressions/position weekly, not just when something feels off — the
   off-page work in section A takes weeks to show effect (new backlinks need to be crawled and
   trust needs to accumulate), so don't judge this plan's success on a 1-week window.
2. Track per-post rankings for their specific Tier 1 target phrase, not just overall site
   impressions — overall impressions can stay flat while individual posts start moving on their
   specific long-tail phrase, which is the leading indicator this plan is working before overall
   numbers move.

## What NOT to do
- Don't keyword-stuff existing posts to chase Tier 1 phrases harder — the audit found the content
  itself is fine; the gap is external authority, and over-optimized on-page text without backlinks
  to back it up doesn't move rankings and risks reading worse to actual readers.
- Don't chase head terms (`parental control app`) yet — see "explicitly not targeting" above.
- Don't buy backlinks or use link-farms/directory-spam services — Google penalizes this, and it's
  a real risk to a domain that's otherwise clean.
