# The Zcash Foundation Community Governance Process

It’s time for the Zcash Foundation to conduct its first election. After the election, we’d like to continue in mostly the same way we’ve already been operating. (See our [2018 Vision document](https://github.com/ZcashFoundation/ZcashFoundation/blob/master/2018-VISION.md)).

## Objectives for the Election

We have two main objectives for the election:

- Providing a platform for new Board candidates and to elect new board members
- Measure and understand community sentiment to guide Foundation policy

The Board of Directors is important since they are officially the root authorities in control of the organization. Three of the existing Board members have all expressed a preference of remaining on the board. In the Zcash Foundation's [first public statement](https://z.cash.foundation//blog/hello-world/), they described themselves as a "bootstrap board," and so this election is meant to expand the Board beyond the initial bootstrap—and to broaden the Foundation's accountability.

A small board that is motivated and engaged is better than one with a diffuse sense of responsibility. However, we’d also like to be held publicly accountable in as a broad sense as we can. Thus we'd like to maintain a Board of five members; that leaves two open Board seats.

The second objective is more abstract, but just as important; the Foundation has many challenges ahead and understanding community sentiment is tantamount to serving our ever-expanding stakeholders in the Zcash and broader privacy-focused community.

### Being on the Zcash Foundation Board: Duties and Expectations

For prospective Board Members, the expected time commitment is one video call/meeting every two months, along with sporadic email communication when the Executive Director/Chairperson needs feedback (a few hours a week on average, with some variance) and attendance at our annual conference (Zcon). Also please note that being on the Board is currently an unpaid position. 

And what does it mean to be a "root authority" in control of the organization? In our [Chairman's words](https://twitter.com/socrates1024/status/987374121892839424), they steer the Foundation and are ultimately responsible for it (e.g., hiring/firing the Executive Director, having bold visions about the Foundation's future, and working with said Executive Director to execute on them).

## The Community Governance Panel

...so with our objectives clear, how do we achieve them? What should this election look like? Who are the "stakeholders" in our organization? Some approaches include polling the miners, or polling stakeholders. Each of these is appealing because it's quantitative, and has a technical description. They're examples of _"On-Chain Governance"._ We have issues for discussing these in our public GitHub repository. As a non-profit, we must operate inline with a broad public mission, rather than to enrich a few. It’s difficult to pick a mechanism that gives a fair but effective representation and cannot be gamed.

Our approach—which we anticipate will evolve over time—will be to appoint a “Community Governance Panel,” consisting of a broad collection of people who have contributed in some way to the Zcash community via some public & visible presence. The challenges with this approach:

- Can we make it broad representation (e.g. not all US?)
- Not stacked with insiders to the Zcash Foundation directors, or to the Zcash Company
- The selection outcome is transparent.

The Foundation will be spearheading the selection of the panel and proactively reaching out to community members; the main criteria for selection will be that prospective panel members had some demonstrable public presence and/or contributed in some way to the ecosystem; both would work well in a system with a publicly verifiable ballot.

The Foundation will then contact members of the Panel and,
  - solicit their communication preferences (e.g., Twitter, GPG signed or not, etc.)
  - get their permission to acknowledge them in our transparent list of assented voters
  - encourage them to acknowledge their intent to participate via posting on their medium of choice

Example:
```
@socrates1024 says: I’m going to participate as an approval voter of the Zcash Foundation. My name’s on their spreadsheet here: <link to z.cash.foundation/election-2018-Q12>, with my permission. Correspondence as part of that will be GPG signed by me. I’ll also tweet about it after I vote.
```

The Executive Director will manage and maintain this list, and will publish it prior to the election within this repository. For members that believe they should be on the Panel, they can [apply here.](https://zcashfoundation.formstack.com/forms/community_governance)

**Please note: if you apply and are rejected, we are planning on making a public note of the rejection within this respository.** This is to maximize transparency on the vetting process, given the limitation of the Foundation selecting members unilaterally. Please consider this before applying.

## Ballot Structure

Ballots to be included on the vote will be discussed as Pull Requests to this repository. While the Community Governance Panel—those casting votes—will be limited in number, any member of the public can open a Pull Request for a new ballot item, and the public can discuss it at large via the PR. If anyone wants to suggest an item to be discussed for inclusion on the ballot but is unfamiliar with GitHub, they can email our Executive Director for assistance (josh [at] z [dot] cash [dot] foundation) and he will open a Pull Request on their behalf.

Within the 2018-Q2 folder in this repository, you'll find two separate folders:

- [Board-Nominations](2018-Q2/Board-Nominations)
- [General-Measures](2018-Q2/General-Measures)
 
The folders are self explanatory, but just in case: if you're nominating yourself for the Board, you'll put a markdown file in that folder which includes a brief statement to describe why you should be considered (e.g., your background or contributions to the community) and open a Pull Request to spark public debate. Board nomination votes will be done on a "Satisfaction Approval Voting" method (more on that below).

For general measures (e.g, "Should the Foundation put more resources into studying ASIC Resistance?" "Which of these five attributes of a privacy-preserving cryptocurrency should be prioritized?" etc.) a submitter should put a markdown file in the corresponding folder with their statement and possible responses as a Pull Request, and a brief background explaining the context of their proposal and their best-effort at pros/cons of each possible selection.

Proposals can be opened at any time, but Foundation personnel will make the ultimate decision whether to include a proposed ballot measure into the final ballot (signified by merging into the repository). The final ballot will be assembled **by May 31st, 2018.**

## Voting Structure and Outcome

After assembling the Community Governance Panel and proposals, we'll conduct an election of Board Members and General Measures remotely. We'll structure and collect votes online via [Helios](https://vote.heliosvoting.org/) and allow participants to publish the proof of their vote in whatever medium they prefer. Helios meets most of our design goals (no double-counted or suppressed votes, missing or changed votes would be easy to detect, private voting) although we'd love to have some private voting built into the [Zcash protocol for future elections.](https://eprint.iacr.org/2017/585.pdf)

1. Electing new Board Members

This will use the ["Satisfaction Approval Voting"](https://en.wikipedia.org/wiki/Satisfaction_approval_voting) voting method.

Suppose we have N candidates, and two seats to fill, 

Each voter will see an individual ballot item for each nominee:

- Candidate 1:  	approve/reject (or number between 0 and 1)
- Candidate 2: 	approve/reject (or number between 0 and 1)
...
- Candidate N: 	approve/reject (or number between 0 and 1)

The two candidates with the most total votes are the winners. The votes are weighted so that every voter contributes 1.0 total weight. If you pick two candidates, your vote counts 0.5 for each of them, 0 for the rest. If you pick 5 candidates, your vote counts 0.2 for each of them.

2. Voting on General Measures

Each approved general measure will be voted on individually, depending on the parameters of the ballot.

Voting will commence between the final ballot assembly (~~May 31st, 2018~~ June 8th, 2018) and two weeks afterward (~~June 14th, 2018~~ June 22nd, 2018), and will be managed by the Executive Director of the Foundation. Results will be announced at Zcon0 before being published widely. (Note: we have updated the dates to give more time for ballot discussion and governance panel applications)

Due to our bylaws, decisions must ultimately be made by majority vote of Board Members. Hence we cannot declare this election to be binding—instead the outcome of the election will have to be ratified by the Board Members before taking effect. But we find it unlikely that the Board would go against the will of the community in a fair, well-constructed election.


## Frequency and Feedback

We hope to make this process a regularly occurring event—perhaps yearly to coincide with Zcon0. This is still a nascent process, and we expect to receive lots of feedback to improve it in the future.
