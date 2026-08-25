# Tester recruitment — Reddit + Quora copy

**OBSOLETE (2026-08-26): Paxio has moved out of Google Play open testing into a full production release.** These posts recruit testers for a beta — that ask no longer applies. Don't post as-is; left in place as reference only.

Goal: recruit early testers/parents to try Paxio, using the mobile-permissions post as supporting content. Draft only — you post these yourself (no Reddit/Quora connector exists to post automatically).

Testing link used throughout: `https://play.google.com/store/apps/details?id=com.paxio` — confirm it's still open to new testers before posting.

---

## Reddit — r/Parenting (soft ask, parent-to-parent)

**Title:** Built a parental control app after getting frustrated with the location-tracking-heavy ones — looking for a few parents to try it and tell me what's broken

**Body:**
Full disclosure: I'm the person building this (Paxio), not a random recommendation.

Got frustrated looking for something that just does screen time limits, app blocking, and content filtering well, without also wanting to track my kid's location or read their messages — most of what I found bundled that in as a "feature" I never asked for.

Been building Paxio for a while now, on-device content filtering (nothing routed through a third-party server), screen time + app blocking + bedtime scheduling, free for one child. Wrote up some of the actual thinking behind it if you want the longer version: [link to a blog post — e.g. the bedtime one]

Looking for a handful of parents willing to actually install it and tell me what's confusing, broken, or missing — not looking for praise, looking for the stuff that doesn't work. 2-minute setup. https://play.google.com/store/apps/details?id=com.paxio

Happy to answer anything in the comments — or feel free to email feedback/bugs directly to support@paxio.in.

---

## Reddit — r/AndroidApps (tester-focused, more technical)

**Title:** [Beta] Paxio — parental control app (screen time/app blocking/content filtering), looking for testers before wider release

**Body:**
Maker here (disclosure). Built a parental control app for Android — screen time limits, app blocking, on-device DNS content filtering (not routed through a cloud filtering service), bedtime scheduling. Free tier covers all of that for one child, no separate paid tier gate on the core controls.

In closed/early testing now, looking for people willing to actually install it on a real device (or a spare one) and break things — permission flows, device-role setup (same phone vs. separate device for the kid), whatever. Genuinely want the bug reports, not just "looks nice."

https://play.google.com/store/apps/details?id=com.paxio

Happy to answer technical questions about how the enforcement actually works (VPN-based DNS filtering, Accessibility Service for app blocking, etc.) if anyone's curious about the implementation, not just the product. Bug reports also welcome at support@paxio.in.

---

## Quora answers (real, currently-live questions found via search)

### Q: "Is there a parental control app that will remotely shut down my child's phone at bedtime?"
Source: https://www.quora.com/Is-there-a-parental-control-app-that-will-remotely-shut-down-my-childs-phone-at-bedtime

**Answer draft:**
Yes — most parental control apps handle this as a recurring bedtime lock rather than a literal shutdown (the phone stays on, but locks/becomes unusable during the window you set). Worth checking a few things when picking one: does it let you pick specific days (school nights vs. weekends), does it have a separate one-off timer for things like homework so you're not stuck extending the actual bedtime, and does the schedule reliably survive a device restart (a common silent failure point).

I'm building one of these (Paxio, disclosure) and wrote up the actual mechanics of how a bedtime lock should work, since "set a bedtime" sounds simpler than it turns out to be in practice: [link to bedtime post]. Currently in testing if you want to try it — free for one child, handles bedtime plus screen time limits, app blocking, and content filtering. Feedback welcome at support@paxio.in. https://play.google.com/store/apps/details?id=com.paxio

### Q: "What is the most effective app for parents to limit screen time and block access to certain apps on Android devices?"
Source: https://www.quora.com/What-is-the-most-effective-app-for-parents-to-limit-screen-time-and-block-access-to-certain-apps-on-Android-devices

**Answer draft:**
Depends a bit on what you actually need beyond the basics, but the core things worth checking in any app: does it enforce a real daily time limit (not just track usage), does app blocking work in real time (not something a kid can wait out or uninstall around), and does content filtering happen on the device itself or route through a third-party server (worth knowing either way, but different privacy tradeoffs).

Disclosure: I build one of these (Paxio) — handles all three plus bedtime scheduling, free for one child, on-device content filtering. Currently looking for early testers if you want to try it and tell me what's missing (or email support@paxio.in): https://play.google.com/store/apps/details?id=com.paxio

### Q: "Which is the best parental control app for android to use on multiple devices (to view and restrict kids activities from parents device)?"
Source: https://www.quora.com/Which-is-the-best-parental-control-app-for-android-to-use-on-multiple-devices-to-view-and-restrict-kids-activities-from-parents-device

**Answer draft:**
Worth checking whether the app actually supports your specific setup — some assume the kid has a dedicated device, others assume a shared family phone, and not all of them handle both cleanly. If you're managing from a separate device than your kid's, make sure whatever you pick actually syncs settings/limits in both directions reliably (a surprising number don't handle this well).

I'm building Paxio (disclosure) — specifically built to work whether your kid has their own device or shares one with you, switchable from the app itself. Screen time, app blocking, content filtering, bedtime. In testing now (feedback to support@paxio.in): https://play.google.com/store/apps/details?id=com.paxio

---

## Notes

- **No promotional offer in these (updated 2026-08-26).** The r/Parenting post previously offered "3 months of the full paid feature set free" — removed per the user's decision that standing posts shouldn't carry a specific offer; time-boxed promos will be run separately during a defined period instead.
- All Reddit/Quora copy discloses maker status upfront — this matters for both platforms' actual community norms (undisclosed self-promotion tends to get removed/downvoted hard) and for the "authentic, not sales-y" tone rule already established.
- Each answer is written to genuinely answer the question first, mention Paxio second — not a bait-and-switch.
- You'll want to actually read each Quora question's other existing answers before posting, in case someone's already said something you'd want to respond to or avoid duplicating.
- If the Play Store link/testing track ever changes, let me know and I'll swap it in everywhere at once.
