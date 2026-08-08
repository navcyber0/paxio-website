# Blog draft status

Drafted posts below are pending human review until marked Published. A live `blog/` section now exists on the site (added 2026-08-06, see note at bottom) — converting an approved draft into a live page is still a separate, manual, per-post step, never done automatically by the drafting task. Standard format as of 2026-08-04: ~2-3 min read (450-600 words), a genuinely recent (<12 month) official/primary-source stat where one credibly fits (skipped, not forced, where nothing recent enough exists), and a real photo (user-selected from Unsplash, free-use license) as the lead image in place of the earlier SVG illustrations.

## Original 5 topics

| # | Title | File | Status |
|---|---|---|---|
| 1 | Parental control apps that don't track your kid's location — what to look for | `parental-control-apps-no-location-tracking.md` (lead photo `location-tracking-navigation-app.jpg`, Alicia Christin Gerald/Unsplash, replacing the hero SVG; 2nd SVG `on-device-vs-cloud.svg` still in place) | drafted 2026-08-03, pending review — not yet shortened/re-stat'd to the new length/stats standard |
| 2 | Screen time limits vs. app blocking vs. content filtering — what's actually different | `screen-time-vs-app-blocking-vs-content-filtering.md` (lead photo `three-controls-family-couch.jpg`, Vitaly Gariev/Unsplash — Claude-picked; note the first candidate found for this slot was a paid Unsplash+ photo, correctly skipped in favor of a free-license one) | drafted 2026-08-03, pending review — not yet shortened/re-stat'd |
| 3 | What actually happens when you set a bedtime schedule on your kid's phone | `bedtime-schedule-what-actually-happens.md` (lead photo `bedtime-boy-tablet-in-bed.jpg`, Helena Lopes/Unsplash) | 511 words (~2 min). Stat: CDC, *Preventing Chronic Disease*, July 2025 — high-screen-time teens report depression/anxiety symptoms at 2-3x the rate. **Published 2026-08-06** as [`blog/bedtime-schedule-what-actually-happens.html`](../../blog/bedtime-schedule-what-actually-happens.html), commit `9bc7685`. |
| 4 | How on-device content filtering works (and why it's different from cloud filtering) | `on-device-content-filtering-explained.md` (lead photo `on-device-filtering-lock.jpg`, FlyD/Unsplash) | 467 words (~2 min). No stat — the only relevant recent study (UCL/St. Pölten, March 2025) covers a different risk (sideloaded-app permissions), didn't fit. Pending review. |
| 5 | The screen-time argument, and why most apps make it worse | — | pending (narrative/opinion piece, not yet drafted) |

## Broadened child-digital-safety scope (added 2026-08-04)

| Title | File | Status |
|---|---|---|
| Cyberbullying: what it actually looks like, and how to notice it | `cyberbullying-what-it-looks-like.md` (lead photo `cyberbullying-hands-face.jpg`, Luiz Rogério Nunes/Unsplash — deliberately picked a neutral/contemplative photo, avoiding a "depression/suffering"-tagged alternative that came up in search, per the sensitive-topic tone rule) | 588 words (~2.5-3 min). Stat: Pew Research Center, "Teens' Experiences on TikTok, Instagram and Snapchat," 2026-04-15 — ~30% of Snapchat users / ~20% on TikTok & Instagram report harassment. Pending review. |
| What kids are actually sharing on social apps (oversharing) | `what-kids-actually-overshare.md` (lead photo `oversharing-selfie-street.jpg`, Vitaly Gariev/Unsplash) | 505 words (~2 min). No stat — only relevant number found is a 2012-2013 Pew study, too old. Pending review. |
| In-game chat and spending: the two gaming-safety risks that aren't about screen time | `gaming-safety-chat-and-spending.md` (lead photo `gaming-desk-electronics.jpg`, Giang Duong/Unsplash) | 524 words (~2 min). No stat — most recent official source (Video Games Europe/Ipsos) is Sept 2024, ~23 months old. Pending review. |
| Helping your kid tell real from fake online — a digital literacy starting point | `digital-literacy-starting-point.md` (lead photo `digital-literacy-laptop-group.jpg`, John/Unsplash) | 495 words (~2 min). Stat: Pew Research Center, "How Teens Use and View AI," 2026-02-24 — ~20% of teens use AI chatbots to get news. Pending review. |

## Mobile-security track (added 2026-08-06)

| Title | File | Status |
|---|---|---|
| The app permissions kids grant without thinking | `mobile-app-permissions-kids-grant.md` (lead photo `mobile-permissions-app-icons.jpg`, Georgiy Lyamin/Unsplash) | Stat: FTC amended COPPA Rule, in force April 22, 2026 (Federal Register). **Published 2026-08-06** as [`blog/mobile-app-permissions-kids-grant.html`](../../blog/mobile-app-permissions-kids-grant.html) — first live post, commit `9559204` (photo swapped same day, commit `35dde19`). |
| QR code scams work because of how phones handle them — not because kids are careless | `qr-code-scams-mobile-devices.md` (lead photo `qr-code-scam-package.jpg`, Markus Winkler/Unsplash — deliberately picked a package-with-QR-code photo to match the FBI unsolicited-package scheme cited in the post) | ~590 words (~2 min). No numeric stat — the FBI IC3 advisory (primary source, July 2025) explicitly states this scheme "isn't yet as widespread as other fraud" and gives no figure, so the post cites the advisory itself rather than forcing a number. Drafted 2026-08-08, pending review. |

## Screen-time track (added 2026-08-07)

| Title | File | Status |
|---|---|---|
| Age-appropriate screen time, now that the "two-hour rule" is gone | `age-appropriate-screen-time-milestones.md` (lead photo `age-milestones-family-tablet.jpg`, Alexander Dummer/Unsplash) | ~570 words (~2 min). Stat: AAP policy statement + technical report "Digital Ecosystems, Children, and Adolescents," *Pediatrics* Vol. 157 Issue 2, published 2026-01-20 — retires the 2016 fixed two-hour/day guidance. Converted to live template and added to `blog/index.html` locally on 2026-08-07, **not yet pushed** — pending user review/approval per the new daily-post workflow (build+review locally each day, push only after explicit go-ahead). |

## Photo sourcing note (added 2026-08-04)

All lead photos are user-selected from Unsplash (free-use license, no attribution legally required, but a small `<span class="photo-credit">` line was added under each as good practice — safe to remove if the live post design doesn't want it). Original SVG illustration files are left in place in `images/` (not deleted) in case any post wants to revert or use them as a secondary/supporting graphic later — only the markdown embed line was changed to point at the new photo.

Only the not-yet-drafted #5 still needs a lead photo, once it exists. All other posts now have real photos.

## Next topics to draw from (not yet drafted)

- Healthy digital habits / screen-time psychology, grounded in real research
- AI chatbots and kids: what's actually risky, what isn't
- (Sensitive, lower priority per positioning) online predators/stranger-contact awareness, sexting/inappropriate-content exposure — handle with the same care as the cyberbullying post if/when picked up

## Publishing note

A blog listing page and post template now exist on the live site (`blog/index.html` + per-post pages, added 2026-08-06). Two drafts have been converted and published so far: mobile-app-permissions-kids-grant (first post) and bedtime-schedule-what-actually-happens (second post) — see their rows above for commit hashes.

**Workflow update (2026-08-07):** per the user, converting a draft into the live-template page, updating `blog/index.html`, and downloading Unsplash images are all fine to do locally without asking each time, as long as everything stays inside this repo's `blog/`/`marketing/blog-drafts/` folders and images come from Unsplash (free-license only) unless another source is cleared first. The one remaining gate is `git push` to GitHub — that still needs the user's explicit go-ahead every time, reviewed via the local page first. Intended cadence: one post built+ready per day, pushed after approval.
