# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Primary users: parents of kids roughly 6-14 who have their own Android device, already actively concerned about screen time. Global audience — the product is deliberately positioned as international, not region-specific, despite some early locale signals (Indian carrier/locale) seen in early test-device logs.

## Product Purpose

In today's world, the smartphone has become irreplaceable — for adults and kids alike, day-to-day life doesn't really run without one anymore. Paxio's purpose isn't to take that away from a kid. It's to make sure the phone stays what it should be: a tool used productively, or for entertainment within a healthy, bounded amount of time — not an always-on virtual companion that quietly becomes an addiction or a stand-in for real relationships.

Left unmonitored, a kid's phone use can go wrong in real ways: becoming a vector for cyberbullying (as target, or without realizing it, as participant), reinforcing addictive usage habits, or feeding unhealthy relationships and dependencies.

## Positioning

Paxio's current controls — screen time limits, app blocking, content filtering, and bedtime scheduling — are today's answer to that. The scope is expected to grow as more of these risks get addressed over time; this is not a fixed, final feature list. Screen-time monitoring and control is the headline message; privacy (no location tracking, on-device content filtering, nothing read from messages) is a real, supporting differentiator, not the lead.

## Operating Context

Marketing/legal website for the Paxio Android app (paxio.in / www.paxio.in, hosted on GitHub Pages). Companion to the Android app itself (separate repo) — the site's job is acquisition (explain the product, get an install) and required legal/support pages (privacy policy, terms, account/data deletion instructions), not the product experience itself.

## Capabilities and Constraints

- Core controls: screen time limits (daily limit + live usage tracking), app blocking (per-app allow/block, enforced in real time), content filtering (on-device DNS-based category blocking — browsing activity never leaves the device), bedtime scheduling (recurring lock + a separate one-off timer for homework/dinner).
- No location tracking of the child, ever — a deliberate, permanent product decision, not a missing feature.
- Content filtering resolves DNS locally on the device — no third-party cloud filtering service in the data path.
- Android-only currently; no iOS version exists.

### Pricing tiers (confirmed real and implemented, 2026-08-08)

A paid tier now exists in the app. This corrects the earlier "no paid tier yet" note — Paxio Pro is real, gated, and priced.

**Paxio Free (forever):**
- 1 child profile
- Daily screen time limit
- App blocking — up to 5 apps
- Content filter — unblock up to 3 categories (rest stay filtered by default)
- Parent PIN protection
- Weekly reports — 3 stats (screen time, over-limit days, blocked app attempts), 30-day history

**Paxio Pro — ₹499/mo (44% off ₹899) or ₹4,999/yr (54% off ₹10,788):**
- Up to 3 child profiles
- Unlimited app blocking + per-app time limits
- Content filter — unblock any categories
- Bedtime & schedule locks
- Remote internet control (pause internet instantly, or for a set duration)
- Weekly reports — 7 stats, 1-year history
- Priority support

**No self-serve upgrade yet.** There's no Play Billing integration — Pro entitlement is granted by hand during early access. The app's "Upgrade to Pro" buttons route to the site's Contact page rather than a live checkout; any on-site Pro CTA should do the same until self-serve billing ships.

**Family tier is a documented future plan only** (7 profiles, multi-device, rewards) — not built, not priced for real. Do not advertise it as available.

## Brand Commitments

- Name: Paxio (rebranded from an earlier "KidSafe" name — no live trace of the old name should remain in shipped copy).
- Voice: authentic, safety-first, leads with a real parent problem — explicitly not sales-y, not feature-list-y, no urgency/scarcity language, not typical SaaS marketing tone. This is a repeated, explicit instruction, not a style guess.
- Positioning priority: monitoring/control capability is the headline message; privacy is real but secondary, not the lead (reversed from an earlier privacy-first framing, corrected 2026-08-03).

## Evidence on Hand

No real customer testimonials, case studies, press mentions, or third-party benchmarks exist yet — the product is still in closed/early testing. Do not fabricate any of these in future copy; state absence rather than inventing placeholder social proof.

## Product Principles

1. The phone itself isn't the enemy — irreplaceable in modern life, for kids too. The product's job is bounded, healthy, productive use, not phone removal or blanket restriction.
2. Lead with monitoring/control capability, not privacy — privacy is a real, supporting differentiator, never the headline.
3. Say what's true today, not what's aspirational — Free is capped at 1 child/5 apps/3 unblocked categories, Pro is real but manually granted (no self-serve checkout yet), Family is future-only, and the current controls are today's answer to a broader, still-growing set of real risks (cyberbullying, addictive habits, unhealthy relationships), not a finished list.
4. Never claim a feature that isn't real or currently active (e.g. AI-generated insights are paused/backlog, not live).
5. Copy should read like a parent who understands the problem wrote it, not a SaaS marketing team.

## Accessibility & Inclusion

No specific accessibility standard (e.g. WCAG level) has been formally committed to yet — general good practice only, nothing to hold current or future work to as a hard requirement.
