# Lead monitoring — results log

Newest-first (most recent run's section at top, for quick scanning). Each entry: date found, platform, keyword, URL, one-line note. This task only observes/logs — nothing here has been posted to.

**Status column**: `Open` = not yet responded to, `Done` = you've replied/handled it, `Ignored` = reviewed and deliberately skipped (e.g. thread too old/stale) — no need to keep checking either way. Tell Claude "mark [thread] as done" or "mark [thread] as ignored" and it'll flip the status in place — handled items stay in the log (so they're not re-surfaced as "new" if they ever reappear in a search) but you can skip them when scanning.

---

## 2026-08-17 — manual test run of new competitor-name keywords (20 queries: Google Family Link, Bark, Qustodio, Aura, AirDroid, Norton Family, mSpy, FamilyTime, Kids360, Boomerang — generic + alternative/dissatisfaction variant each)

9 new, genuinely relevant Quora threads found. Heavy noise this run, mostly excluded: child-audience "how do I bypass [competitor]" threads (matches existing exclusion pattern, very common for Bark/Qustodio/Family Link specifically since kids search these by name), Quora "vs" comparison Spaces (`barkvsqustodiovscircle.quora.com` etc. — content-farm-style pages, not real user threads), all "Aura" results (name collision with the spiritual/metaphysical "aura" concept — zero genuine hits for the Aura parental-control product), Spanish/Portuguese mSpy threads (non-English), AirDroid results mostly about wireless file transfer or adults removing spyware from their own phone (not a parent lead), and generic informational "how do parental control apps work" questions with no recommendation-seeking intent.

**Aura dropped from the keyword list same day** (2026-08-17) after this run — zero usable hits, not worth the two queries/run. See `paxio-lead-monitor` task file for the updated keyword list (18 competitor queries now, down from 20).

**New pattern worth noting:** mSpy generic legitimacy/alternative questions ("Is MSPY reliable?", "is there software as good or better than it?") were excluded despite surfacing under dissatisfaction-intent queries — none of the snippets had explicit kid/parent framing, and mSpy's reputation is heavily mixed with covert spouse/partner-monitoring use cases on Quora, so treating unqualified mSpy questions as parent leads risks misattributing audience. Kept only threads with explicit "parental control" / "your family" / "your child" framing.

| Status | URL | Note |
|---|---|---|
| Ignored | https://www.quora.com/How-do-I-enable-parental-control-in-Android | ~5 years old — stale, ignoring |
| Done | https://www.quora.com/Is-the-Google-family-link-good | Evaluating whether Family Link is worth using — competitor evaluation-stage lead |
| Done | https://www.quora.com/What-do-you-think-of-Bark-the-15-month-service-that-monitors-your-kids-texts-photos-contact-lists-and-location-using-the-Bark-Watch-smartwatch | Opinion-seeking on Bark's $15/mo value — competitor evaluation-stage lead |
| Open | https://www.quora.com/Do-you-think-a-Bark-Phone-which-allows-parents-to-monitor-their-childs-activity-is-a-good-idea | Same pattern — evaluating Bark's approach |
| Open | https://www.quora.com/Is-Qustodio-a-good-parental-control-app | Direct Qustodio evaluation question |
| Open | https://www.quora.com/I-have-the-app-qustodio-how-could-I-uninstall-it-if-I-forgot-my-password | Parent (owns the password) locked out of their own Qustodio install — real friction/frustration signal |
| Open | https://www.quora.com/What-is-the-difference-between-Qustodio-free-and-premium | Evaluating Qustodio tiers before committing |
| Open | https://www.quora.com/Xnspy-vs-Qustodio-Which-parental-control-app-has-worked-better-for-your-family-and-why | Direct family-framed comparison-shopping between two competitors |
| Open | https://www.quora.com/Is-there-a-company-or-individual-who-has-developed-a-software-for-parents-to-monitor-their-childrens-online-activities-on-various-devices | Explicit "parents"/"children's" framing, actively asking for a solution — strongest lead this run |

## 2026-08-16 — scheduled run (Quora-only, all 6 keywords)

10 new, genuinely relevant Quora threads found. Excluded as poor-fit noise: self-use screen-time-measurement questions (no kid/parent framing), two GPS-location-only requests (Paxio doesn't do geofencing — one explicitly said "I don't need monitoring, just location"), and two "how do I bypass Screentime" threads (child audience asking how to defeat controls, not a parent lead).

| Status | URL | Note |
|---|---|---|
| Open | https://www.quora.com/Where-can-we-find-the-best-parental-control-app-for-our-childrens-phone | Parent asking where to find the best parental control app for their kid's phone |
| Open | https://www.quora.com/Can-I-block-inappropriate-apps-and-websites-on-my-child-s-phone-without-rooting-it | Asking about blocking inappropriate apps/websites without rooting — direct fit for Content Filter + App Control |
| Open | https://www.quora.com/How-do-I-track-my-kid-s-location-and-monitor-app-usage-on-Android | Wants both location and app-usage monitoring |
| Open | https://www.quora.com/How-do-I-track-our-kid-s-mobile | General "how to track our kid's phone" |
| Open | https://www.quora.com/How-do-you-put-a-tracker-on-your-childs-phone | General "tracker on child's phone" — likely broader parental-control intent, not strictly GPS |
| Open | https://www.quora.com/What-is-the-best-app-to-track-kids-activity-in-my-smartphone | Asking for best app to track kids' activity |
| Open | https://www.quora.com/How-can-I-track-my-childs-phone-for-free-without-touching-his-her-phone | Wants free/remote tracking — expectation may need correcting (install access required) but real lead |
| Open | https://www.quora.com/What-is-the-best-app-to-track-sync-monitor-my-kids-phone-without-them-knowing | Wants covert monitoring app |
| Open | https://www.quora.com/Is-there-something-I-can-download-or-do-to-a-phone-before-I-give-it-to-my-child-that-lets-me-monitor-it-without-them-knowing | Wants to pre-configure monitoring before handing phone to child |
| Open | https://www.quora.com/Is-there-an-adult-filter-for-Android-phones-that-filters-all-adult-content-regardless-of-browser-or-app | Direct fit for Content Filter feature (adult-content blocking across browsers/apps) |

**Recency note:** tried to check post/answer dates to filter out threads >1yr old or inactive >6mo, per user request. Both WebFetch (403) and browser automation (Cloudflare "Just a moment..." bot-check, never clears) are blocked by Quora — no programmatic way to get dates. WebSearch snippets don't carry dates either. Decision: keep listing threads by topic relevance only; user will eyeball the date manually when clicking through to reply (works fine for a human since Quora renders it once a real logged-in browser loads the page).

## 2026-08-15 — manual test run (validating paxio-insights lead-monitor logic before enabling the 6-hourly automation)

**Keywords tested:** "parental control app" (Reddit + Quora), "kid keeps bypassing screen time" (Reddit), "reddit parental control app recommendation android kids" (general), `"r/parenting" OR "r/androidapps" parental control app screen time` (general)

**Reddit — 0 genuine results across 4 separate query variations.** Every Reddit-targeted search (`site:reddit.com "..."`, plain keyword phrasing, `r/subreddit`-name phrasing) returned third-party listicle/aggregator sites (AlternativeTo, Hoverwatch, TomsGuide, GitHub) instead of actual reddit.com threads. Conclusion below.

**Quora — 8 genuine, live quora.com question pages found** for keyword "parental control app" Android:

| Status | URL | Note |
|---|---|---|
| Done | https://www.quora.com/What-are-the-best-Android-parental-control-apps | New — not yet answered |
| Done | https://www.quora.com/What-are-the-best-parental-control-apps-for-Android-and-Windows | New — not yet answered |
| Done | https://www.quora.com/How-can-I-make-a-parental-control-app-for-android | New — dev-audience question, not a parent lead, low priority |
| Done | https://www.quora.com/Which-one-is-the-best-parental-control-app-for-Android-devices | New — not yet answered |
| Done | https://www.quora.com/Can-you-install-a-Parental-Control-App-on-an-old-Android-device-Android-version-Marshmallow-If-so-how-can-you-do-that | New — niche (pre-Marshmallow devices), low priority |
| Open | https://www.quora.com/What-are-some-good-parental-control-apps-for-Android | New — not yet answered |
| Open | https://www.quora.com/What-is-the-most-effective-app-for-parents-to-limit-screen-time-and-block-access-to-certain-apps-on-Android-devices | Already drafted — see `marketing/blog-drafts/social-posts/tester-recruitment-reddit-quora.md` |
| Open | https://www.quora.com/Which-is-the-best-parental-control-app-for-android-to-use-on-multiple-devices-to-view-and-restrict-kids-activities-from-parents-device | Already drafted — see `marketing/blog-drafts/social-posts/tester-recruitment-reddit-quora.md` |

All 8 added to `seen-posts.json` so future runs only surface genuinely new threads.

**Verdict on the monitoring approach:** Quora half works well via WebSearch — real, live, relevant threads surface directly. Reddit half does not — WebSearch's index does not appear to have usable coverage of live reddit.com threads for these keywords, returning only third-party sites that reference Reddit rather than actual Reddit URLs. Recommend narrowing `paxio-lead-monitor`'s scope to Quora-only until a real Reddit data source exists (API access is separately blocked — see prior research), rather than running Reddit queries that reliably return nothing useful every 6 hours.
