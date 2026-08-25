# Reddit — r/AlphaAndBetaUsers (recommended starting point)

**OBSOLETE (2026-08-26): Paxio has moved out of Google Play open testing into a full production release.** This entire post is built around "looking for testers before wider release" — that ask no longer applies. Don't post as-is; left in place as reference only.

Why this sub: purpose-built for exactly this ask — apps looking for testers post here as the norm, not an exception. Self-promotion friction that would get a post removed in r/Parenting or r/AndroidApps doesn't apply here.

**Flair to use:** [Android] (check the sub's current flair list before posting — it may have changed)

**Title:** [Android] Paxio — parental control app (screen time, app blocking, on-device content filtering) — looking for testers before wider release

**Body:**

Maker here, full disclosure.

Paxio is a parental control app for Android — daily screen time limits, real-time app blocking, on-device DNS content filtering (not routed through a third-party server), and bedtime scheduling. Free tier covers all four controls for one child, no paywall on the core features.

What I'm looking for: people willing to actually install it on a real device and try to break it — permission flow, device-role setup (same phone shared with a kid vs. a separate dedicated device), the actual enforcement behavior. Bug reports and "this is confusing" feedback are what I actually need, not praise.

A bit on how it works under the hood, if that's useful context for testing: content filtering is VPN-based DNS filtering (so it can flag/block categories without routing traffic through an external server), app blocking uses Accessibility Service to catch a blocked app in real time, and there's a PIN-gated settings layer so a kid can't just flip things back off.

https://play.google.com/store/apps/details?id=com.paxio

Happy to answer anything about the implementation or take feature requests — this is early enough that real input still shapes what gets built next. Bug reports/feedback also welcome directly at support@paxio.in if you'd rather not post it here.

---

## Notes

- Testing link is the live Play Store listing (`https://play.google.com/store/apps/details?id=com.paxio`) — confirm it's still open to new testers before posting.
- **No promotional offer in this post (updated 2026-08-26).** Previously offered "3 months of the full paid feature set free" — removed per the user's decision that standing posts shouldn't carry a specific offer; time-boxed promos will be run separately during a defined period instead.
- Read the sub's posting rules/pinned mod post first — some beta-tester subs require a specific title format or restrict to a weekly megathread rather than standalone posts; worth a 2-minute check before posting so this doesn't get auto-removed.
- Once you have a few real testers and some real feedback, that's the natural trigger for the r/Parenting follow-up post already drafted in `published-posts-social-copy.md` / the earlier tester-recruitment file — "here's what testers said" is a stronger opener than a cold pitch.
