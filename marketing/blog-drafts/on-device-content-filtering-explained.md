# How on-device content filtering works (and why it's different from cloud filtering)

_Meta description: "Content filtering" can mean two very different things depending on where the filtering actually happens. Here's the real difference, and why it matters for what leaves your kid's phone._

_~2 min read_

Most parental control apps say some version of "blocks inappropriate content" — it's easy to assume that's one thing. It isn't. Where the filtering decision happens, on the device or on a server it talks to, changes what data leaves the phone.

![A padlock, representing the security/privacy question at the heart of on-device vs. cloud filtering](images/on-device-filtering-lock.jpg)
<span class="photo-credit">Photo by <a href="https://unsplash.com/@flyd2069">FlyD</a> on <a href="https://unsplash.com/photos/zAhAUSdRLJ8">Unsplash</a></span>

## The mechanism: DNS resolution

Every time an app opens a web address, the device first resolves that address to a server location — DNS resolution. Content filtering almost always works by intercepting that step: check the domain's category, then either let it resolve or block it. True whether filtering is on-device or cloud-based — the difference is *where* that check happens.

## Cloud filtering: the check happens on someone else's server

The device sends DNS requests out to a third-party filtering service, which checks and responds. This works, but every domain your kid's device tries to reach passes through an external company's servers first. Not necessarily sinister — but a running log of your family's browsing now exists on infrastructure you don't own and didn't set the retention policy for.

## On-device filtering: the check happens on the phone

A blocklist lives on the device, gets checked locally, decision made right there — nothing round-trips to an external server for the purpose of filtering. Browsing activity doesn't get routed through a third party as part of how the filter works. Not a promise layered on top — what the mechanism actually does.

## The honest tradeoff

Cloud services update centrally and can apply more sophisticated (ML-based) classification; an on-device blocklist is only as current as its last update. For most parents, "which category does this domain fall into" is a solved-enough problem that the currency tradeoff is small — the privacy tradeoff is the one that actually matters day to day.

## What neither approach covers

Content filtering blocks by domain category — it doesn't evaluate posts or messages *inside* an already-allowed app. That's a fundamentally different, much harder problem than category-level blocking.

## Where Paxio fits

Paxio's content filtering resolves DNS locally — blocklist on the phone, category check on the phone, browsing activity never routed through a third party as part of how it works. One of four core controls, free for one child, alongside screen time, app blocking, and bedtime.

"Does this filter on the device or in the cloud" is a fair, concrete question to ask any parental control app. [Paxio is free to try](https://www.paxio.in/) if on-device is the answer you want.
