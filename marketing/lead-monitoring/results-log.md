# Lead monitoring — results log

Newest-first (most recent run's section at top, for quick scanning). Each entry: date found, platform, keyword, URL, one-line note, and a drafted response ready for your review. This task only observes, drafts, and logs — nothing here has been posted to Quora.

**Status column**: `Pending Review` = new lead, draft ready, awaiting your decision (default for every newly found entry), `Done` = you've reviewed and posted/handled it, `Ignored` = reviewed and deliberately skipped (e.g. thread too old/stale, no honest fit) — no need to keep checking either way. Tell Claude "mark [thread] as done" or "mark [thread] as ignored" and it'll flip the status in place — handled items stay in the log (so they're not re-surfaced as "new" if they ever reappear in a search) but you can skip them when scanning. Older entries above may still show `Open` from before this column was renamed — treat `Open` and `Pending Review` as the same state.

---

## 2026-08-19 — scheduled run (24 queries: 6 general + 18 competitor-name, per current task keyword list)

23 of 24 result URLs across all queries were already in `seen-posts.json`. 1 genuinely new, relevant lead found. 1 additional new URL surfaced but was filtered as noise (not a parental-control lead) and added to `seen_urls` only, not logged below: "Is there a family networking site?" (unrelated family-social-network question, picked up under the FamilyTime-alternative query).

**Process note — required reference file does not exist:** this task's Step 4 calls for reading `marketing/blog-drafts/social-posts/paxio-post-comments.md` for the established Quora-reply tone/voice/facts before drafting each response, and states this step is not optional. That file is not present in this repo and has never existed in its git history (checked via `git log --all --diff-filter=A -- "*paxio-post-comments*"`, zero hits) — the same is true for `paxio-fresh-posts.md`. The only file actually present in that directory is `published-posts-social-copy.md` (social-share copy for published blog posts — genuine-answer-first, clear maker disclosure, non-salesy — but written for promoting blog links, not for answering Quora questions directly). The draft below was written using that file's voice as the closest available reference, plus `pricing.html` verified directly for feature accuracy, since a lead without a draft isn't allowed to be logged as incomplete. Flagging this so the gap is visible rather than silently recurring every run — worth either creating the missing file or correcting the task's file reference.

| Status | URL | Note |
|---|---|---|
| Pending Review | https://www.quora.com/Is-Apple-Screen-Time-enough-for-managing-a-childs-device-usage-or-should-I-consider-other-apps-like-Bark-or-Qustodio | Parent weighing Apple Screen Time vs. third-party apps (names Bark, Qustodio) — real evaluation-stage lead, but the question is framed around an iPhone, so Paxio (Android-only) is at best a partial fit; drafted response answers the real question and discloses Paxio only as an aside for the Android side of a mixed household |

**Drafted response — for https://www.quora.com/Is-Apple-Screen-Time-enough-for-managing-a-childs-device-usage-or-should-I-consider-other-apps-like-Bark-or-Qustodio:**

> Apple's built-in Screen Time is genuinely solid for the basics — app limits, downtime, content restrictions — and it's free, which matters before you go shopping for a subscription. Where it tends to fall short for parents isn't the feature list, it's enforcement: kids find and share Screen Time passcode workarounds pretty fast, and the reporting is thin if you actually want to see patterns over time.
>
> Third-party apps like Bark and Qustodio add things Screen Time doesn't try to do: Bark leans into content/activity alerts (flags for concerning messages, not just time limits), Qustodio is stronger if your household is mixed iOS/Android and you want one dashboard for both, and both give you more detailed usage reporting than Apple's native view. The tradeoff is a monthly cost, and for some of these, permissions that go deeper than Apple's sandboxed approach — worth reading exactly what each one monitors before you commit, since "monitoring" means very different things between them (some read message content, some don't).
>
> Practical way to decide: if Screen Time's limits keep getting bypassed, a dedicated app closes real, specific gaps. If what you actually want is visibility into content/conversations rather than just time limits, that's a different feature set than either Screen Time or a plain app-blocker gives you — check that specifically rather than assuming any parental control app covers it.
>
> Disclosure since I build one of these: I make Paxio, but it's Android-only, so it isn't a fit for what you're describing here (sounds like an iPhone). Only mentioning it in case there's also an Android device in the house — worth knowing the options aren't just Bark/Qustodio on that side either.

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
