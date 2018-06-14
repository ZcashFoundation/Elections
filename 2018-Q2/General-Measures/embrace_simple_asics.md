# Ballot Proposal: Embracing Simple PoW and ASICs
## A Long-Term Plan to Decentralize Mining

Proposed ballot entry, and convenient TL;DR:

```
The Foundation should commit to a plan for migrating the Zcash protocol to a new proof of work algorithm with a hard-fork planned between September 30, 2020 and December 31, 2020, with the following tasks below:

- Selecting a thermodynamically efficient (not ASIC-resistant!), currently unused proof-of-work algorithm
- Hosting and building an open hardware specification for the selected PoW algorithm
- Assembling a consortium of hardware companies to build hardware against this open specification, while encouraging upstream contributions
- Building an open source, cross-platform, user-friendly, p2pool-esque piece of mining software for use with this hardware
- Manage the hard fork upgrade process across users, wallets, exchanges

[ ] Agree
[ ] Disagree
```

## Background

With equal degree fascination and anxiety, I watched the Great ASIC Resistance Debate unfold in Zcash and other cryptocurrencies this year. On the Zcash side, the debate reached fever-pitch after Bitmain released the AntMiner Z9 mini, which resulted in our statement on ASIC Resistance and the [ensuing commitment to investigate and prescribe action.](https://z.cash.foundation//blog/statement-on-asics/)

That statement sowed the seeds for this ballot proposal, and in particular this paragraph (bold parts my own):

> The Foundation believes it’s important to maintain the power of GPUs in Zcash mining. However—and this nuance is important—we also recognize that ASIC resistance may be a red herring, for the health and decentralization of the protocol in the long term. **Perhaps there is another path that we could take, with ample time for community buy-in—and we welcome input on getting there.**
> In the short term, we consider it critical to protect the community members who are building the ecosystem with us. If it’s necessary based on our evaluation of the ASICs on the network, we will hire a developer to construct and submit a ZIP to mitigate its effect on the network. If the Zcash core development team and community approves, it will ideally be deployed by late 2018.

This ballot proposal is that alternate path, one that I believe is worth discussing—one that flips the debate by **embracing ASICs and simple PoW, but only so long as we can encourage open commoditization and access to mining hardware.**

**Full disclosure: what follows is my personal opinion, and not representative of official Foundation policy.** That I am a Foundation employee should not weigh on your evaluation of this proposal, instead let the scales be tipped by the merits of the argument contained herein.

To be blunt: I do not think ASIC Resistant is a long-term, sustainable goal. I *do* think, based on the data available at the time, it was reasonable to make that a high priority when Zcash launched, and that it helped to encourage broader, fairer distribution of ZEC, but to me it is abundantly clear that it's not the right design goal today. With a high enough economic incentive, a hardware manufacturer will ultimately find some way to make an application-specific circuit...and if it's in a particular position, it could monopolize the development and distribution of such a circuit. That creates a dangerous environment for centralization. On the other side of the coin, if you somehow managed to make a truly ASIC-resistant PoW design (something many consider impossible, myself included), then if you are not the largest coin using general compute power you open yourself up to [51% attacks, potentially by easily-rented, virtual compute cycles](https://www.crypto51.app/).

I won't spend time re-*hashing* these arguments, but suffice it to say that the following articles have influenced my thinking on ASICs and PoW, and I strongly encourage anyone reading this ballot proposal (and really any cryptocurrency enthusiast) to also consider reading these articles:

- https://download.wpsoftware.net/bitcoin/asic-faq.pdf
- https://blog.sia.tech/the-state-of-cryptocurrency-mining-538004a37f9b

Given this perspective on the inevitability of ASICs, I think it's better to consider what an ideal PoW mining environment would resemble, and what proactive steps we can take to get there.

## Goals and Assumptions

Here are my explicit goals with this proposal:

- A mining environment that favors broad distribution of rewards
- Less centralization in hashpower (either from pools or mining farms)
- Less centralization in hardware manufacturing (to prevent "stealth" ASIC mining and monopolization)
- Better UX for hobbyist miners, without contributing to centralized pools, to encourage a fat tail of hashpower distribution
- Open source components for all the pieces above, with broad upstream contributions from hardware manufacturers and software developers

And my assumptions:

- Simple, purposeful PoW is better for the security of the network, and enables more entrants in the hardware business...
- ...particularly if a hardware spec is open and contributed to by multiple manufacturers, and the hardware has ample time to be developed _prior_ to PoW activation
- Zcash remains a PoW-based cryptocurrency
- The Foundation will be in a position to orchestrate a hard-fork upgrade with a PoW change
- The Foundation can get hardware companies to agree to an open spec to build on this PoW
- It's possible to build mining software that is open, easy to use, and doesn't contribute to traditional pool centralization
- It's possible to do the above within the Foundation's budget, and without compromising the Foundation's work on supporting privacy infrastructure for the public good (a key part of the Foundation's Mission!)


## Detailed Rationale

Given the goals and assumptions, let's consider each part of the proposal.

```
The Foundation should commit to migrating the Zcash protocol to a new proof of work algorithm with a hard-fork planned between September 30, 2020 and December 31, 2020, with the following goals:
```

This is self-explanatory, but why plan a PoW change with a fork so far in the future? Here's my rationale:

- There are many, many stakeholders in the ecosystem, and giving ample warning helps them make investment decisions (e.g., not spending too much of their money on Equihash ASICs or GPUs).
- But more importantly, a long runway until PoW change can prevent stealth mining by having manufacturers compete in earnest far before they can directly profit off a given piece of hardware through a native token reward...and may encourage them to sell the hardware _sooner_ rather than stockpile it to accumulate hashpower, since their hardware would be sitting idle prior to activation, while other manufacturers could be generating cashflow by _selling_ their hardware...which is the outcome we want.

I think a hasty PoW change to something more ASIC resistant is short-term beneficial, but long-term serves to _widen_ the gap between any given hardware manufacturer's monopoly position as an esoteric ASIC manufacturer and their nearest competitor. But a long-known-in-advance PoW change could allow others to compete, particularly if the next bullet point in my proposal is met:

```
- Selecting a thermodynamically efficient (not ASIC-resistant!), currently unused proof-of-work algorithm
```

The simpler the PoW, the less likely clever hardware tricks can be used to generate competitive advantage for a given manufacturer, and the more likely—and more rapidly—the hardware will be commoditized. Combined with a long lead time to PoW change, it may be possible to have a competitive hardware market months before the fork.

The actual selection could be done like the Zcash Mining Challenge, or via an expert the Foundation hires or contracts.

```
- Hosting and building an open hardware specification for the selected PoW algorithm
```

A competitive, well-maintained, open spec would benefit everyone, particularly new entrants in manufacturing. The Foundation would have to either initiate development or—ideally—work with a number of hardware manufacturers to contribute to an open spec (see next point). This could also be run like the Mining Challenge.

```
- Assembling a consortium of hardware companies to build hardware against this open specification, while encouraging upstream contributions
```

This may be the most difficult, yet most important piece. In effect, this would be an attempt for the Foundation to act as a conduit for [co-opetition](https://en.wikipedia.org/wiki/Coopetition) between manufacturers, sharing development cost while maintaining their own manufacturing business lines. Nothing like this has been done in the mining world before, as far as I know...but that's not to say that it can't work, it's just never been attempted.

```
- Building an open source, cross-platform, user-friendly, p2pool-esque piece of mining software for use with this hardware
```

Much of this work would be for naught if it resulted in overly centralized pools; instead, we should endeavor to have this hardware work with a standard, open, decentralized-first piece of software. Again, we could use a renewed Mining Challenge to spur development, or (attempt) to build it ourselves. Even better if we could implement this directly in the Foundation's future independent node implementation. And thankfully this work can be done in parallel to the hardware development/consortium/PoW selection.

```
- Manage the hard fork upgrade process across users, wallets, exchanges
```

This is still very hard, but seemingly easier by comparison. :)

## Critiques 

There are many risks here, commensurate with the proposal's ambition. My assumptions might be dead wrong. Hardware manufacturers may not be interested in a consortium to build simple PoW equipment. Good UX for hobbyist mining might _require_ centralized pieces. Stealth/more efficient mining might still happen, even if three or four hardware manufacturers agree to an open spec for which they frequently upstream contributions. Hard forks can be difficult to coordinate and organize. The challenges to create good, decentralized mining software and encourage hardware manufacturers might prove too difficult.

And ultimately, it very likely won't prevent the rise of massive mining farms on this PoW. There are _huge_ advantages to running farms, when volume purchases on hardware, in-house hardware development, and access to utility-level electricity create economies of scale. But with the right steps, we could limit the effect those farms have on overall hash power. If the improved UX and cheaper/competitive ASIC market result in 10-20% of hashpower living on farms and 80%-90% in the "fat tail" of hobbyists/users not overly controlled by a single pool, I would consider that a success.

And despite the risks I do think it's worth suggesting this proposal, and getting feedback from the panel on whether this should be a priority for the Foundation. I eagerly look forward to your comments and the community vote.
