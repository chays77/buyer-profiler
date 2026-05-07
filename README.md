# Buyer Profiler

**Read your prospect. Close with precision.**

A folder-based AI specialist for Claude that profiles sales prospects from call transcripts and tells you exactly how to close them — based on who they are, not a generic playbook.

## What This Does

Drop this folder into a Claude project. Paste a sales call transcript or discovery call notes. Get back two things in one output:

1. **A buyer type diagnosis** — who this person is, how they decide, what drives them
2. **A tailored close strategy** — exactly how to run the next call using Sandler methodology, adapted to this specific buyer

If you've filled out `user.md`, you also get:

3. **Seller-Buyer Dynamic** — how *your* natural selling style interacts with *this* buyer's type, and where you need to compensate

## Prerequisites

- A Claude account ([claude.ai](https://claude.ai) — Free, Pro, or Team)
- Claude Projects enabled (available on Pro and Team plans)

## How to Use It

1. Create a new Claude project
2. Upload this entire folder
3. Fill out `user.md` with your seller profile (unlocks the Seller-Buyer Dynamic section)
4. Paste your transcript or call notes and say: **"Profile this buyer and give me my close strategy."**

Claude becomes the Buyer Profiler for every conversation in that project.

> See `GETTING-STARTED.md` for the full onboarding guide including transcript tool recommendations and a step-by-step walkthrough.

## What Good Output Looks Like

```
## Buyer Profile

Type: Commander (ENTJ)
Confidence: High — 3+ aligned signals (data-first open, rejected process talk, asked for a specific metric)

Evidence:
- "I don't need a strategy deck" → explicit rejection of process theater, output-only orientation
- Asked for close rate metric before any relationship signal → T lead, Fire driver
- References two past agencies → auditing before buying, control instinct

Primary driver: Fire — drive to acquire. Win-oriented.
Failure mode: Over-explain process or lead with relationship. Deal dies in the first 3 minutes.

---

## Sandler Frame Check

| Dimension | Status |
|---|---|
| Pain | Partially identified. Past failures are symptoms. Dollar cost not yet named. |
| Budget | Unknown. |
| Decision | Likely sole decision-maker — confirm. |
| Control | Theirs right now. Reclaim with a specific next step. |

Critical gap: Pain has no dollar number. Proposal without it anchors on price alone.

---

## Close Strategy

Open with: "Before I answer your question — walk me through what this has cost you while it's been unsolved. Revenue, time, whatever you can put a number on."

Next step: "Can we get 30 minutes Thursday? I'll bring two options — I want your reaction before I build anything."

Hold back: Don't send a proposal unsolicited. Don't over-detail scope in writing before a second call.
```

## How to Give It Context (optional but improves output)

Paste your transcript, then add one line of deal context if you have it:

> "This is a first discovery call. I haven't proposed anything yet. She was referred by a mutual contact."

The specialist activates on the transcript alone — context makes the close strategy more specific.

## What It Needs From You

- A transcript, call notes, or a written summary of what the prospect said
- Deal context (stage, what you've proposed, what the ask is) — optional

## What It Will Not Do

- Write your proposal (it advises on framing — you write it)
- Guarantee a read from a single 10-minute call (it will tell you its confidence level)
- Make the decision for you — it gives you the read, you make the call

## Who Built This

Curtis Hays, Collideascope — [collideascope.co](https://collideascope.co)
Sandler-trained since 2011. Built from 15 years of applying that methodology to marketing agency sales, combined with behavioral profiling from 16Personalities, DISC, and Terry Bean's behavioral driver theory.

## Acknowledgments

- **Jake Van Clief** — Interpretable Context Methodology (ICM) framework that this folder architecture is built on. [Clief Notes](https://www.skool.com/clief-notes)
- **Clief Notes / Skool** — Week 3 competition prompt that sparked this build
- **Sandler Training** — Pain funnel and qualification framework (trained 2011)
- **16Personalities** — Personality type framework and naming conventions

## License

MIT — free to use, fork, and adapt. Attribution appreciated but not required.
