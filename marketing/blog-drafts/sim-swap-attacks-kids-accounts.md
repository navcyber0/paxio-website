# SIM swap attacks: how a stolen phone number can take over your kid's accounts

_Meta description: In a SIM swap, nobody touches your kid's phone. Someone convinces the carrier to move the number to a new SIM, and every account that texts a login code now texts the attacker. Here's how it works, and the one setting only a parent can turn on._

_~2-3 min read_

![A close-up of fingers holding a small SIM card](images/sim-card-held-fingers.jpg)
<span class="photo-credit">Photo by <a href="https://unsplash.com/@cardmapr">CardMapr.nl</a> on <a href="https://unsplash.com/photos/H5LmvsN1PRU">Unsplash</a></span>

Most account-security advice for kids is about the phone in their hand: a lock screen, a strong password, don't tap strange links. A SIM swap skips all of that. The phone stays in your kid's pocket, still locked, still working, right up until it suddenly shows "No service." By then the phone number is live on a SIM card somewhere else, and every account that sends a login code by text is sending it to someone else.

## How a SIM swap actually works

A phone number belongs to the carrier account, not the physical phone. Carriers can move a number to a new SIM or eSIM, which is exactly what should happen when someone loses a phone. In a SIM swap, an attacker asks for that same move while pretending to be the account holder. Usually they call support or walk into a store with enough personal details to pass the identity check, and sometimes they have help from a bribed insider.

Once the number moves, the attacker taps "forgot password" on the accounts tied to it. A reset code arrives by text, and the account is theirs.

This is a small crime by volume, but it hasn't gone away. The FBI's 2025 Internet Crime Report, published this year, lists SIM swapping as its own crime category, with about $17.4 million in reported losses in 2025. That figure only counts cases people actually reported to the FBI. ([FBI IC3 2025 Annual Report](https://www.ic3.gov/AnnualReport/Reports/2025_IC3Report.pdf))

## Why a kid's number is worth stealing

Kids rarely have bank accounts worth draining. What they do have is a phone number used as the recovery method for nearly everything: game accounts with paid skins and currency, a social account with a rare short username, a school email, sometimes a family streaming or shopping login. Gaming and social accounts get resold, and a hijacked social account can message every one of your kid's friends and ask for money or photos.

There's also a structural catch. Your kid's line is almost always on your plan. The carrier treats you as the account holder, which means the protections that stop a swap are yours to turn on. Your kid can't do it for their own line.

## What actually helps

- **Turn on your carrier's number lock or port-out PIN.** Most major carriers now offer a free setting that blocks SIM changes and number transfers until the account holder turns it off. Check it for every line on the plan, not just your own.
- **Move important accounts off text-message codes.** Where an app supports it, an authenticator app or passkey is tied to the device, not the number, and a SIM swap can't intercept it.
- **Treat sudden "No service" as a warning sign.** If one phone loses signal while the others on the plan are fine, call the carrier from another phone before assuming it's a coverage problem.
- **Keep the carrier account's own details private.** Account numbers, security answers, and the account PIN are exactly what an attacker needs to pass the identity check.

Note that the SIM PIN in Android's settings is a different protection. It stops someone from using a SIM card that's been physically removed, not a swap done at the carrier.

## Where Paxio fits, and where it doesn't

Nothing installed on a phone, Paxio included, can stop a SIM swap, because it happens entirely on the carrier's side. The number lock above is the real defense, and only the account holder can turn it on. What Paxio's content filtering can do is block known phishing pages at the DNS level. Those fake "verify your account" pages are often where attackers collect the personal details they later read to carrier support.

[Paxio's](https://www.paxio.in/) filtering catches those known phishing pages in the background. The carrier lock is still a five-minute call you make yourself.
