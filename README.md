# Buyer Profiler

**Read your prospect. Close with precision.**

A folder-based AI specialist for Claude. Drop the folder into a Claude project. Claude becomes the specialist. Reusable. Shareable. Portable.

---

## How to Use It

1. Create a new Claude project at [claude.ai](https://claude.ai)
2. Upload this entire folder to the project
3. (Optional but recommended) Open `reference/user-profile.md` and fill in your own seller profile — unlocks the Seller-Buyer Dynamic section
4. Paste a sales call transcript or call notes and say: **"Profile this buyer and give me my close strategy."**

Expect output that looks like the example below.

---

## What You Get

Every run produces:

1. **Buyer Profile** — cognitive type, behavioral driver, evidence, failure mode for this deal
2. **Sandler Frame Check** — what's known and unknown across Pain / Budget / Decision / Control
3. **Close Strategy** — exact language for the next call, what to hold back

If `reference/user-profile.md` is filled out, you also get:

4. **Seller-Buyer Dynamic** — how your natural selling style interacts with this buyer's type, and where you need to compensate

---

## Example Output

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

---

## What It Will Not Do

- Write your proposal (it advises on framing — you write it)
- Guarantee a read from a single 10-minute call (it tells you its confidence level)
- Make the decision for you — it gives you the read, you make the call

---

## Folder Contents

```
buyer-profiler/
├── identity.md          ← Who the specialist is
├── rules.md             ← How it responds, output format, activation logic
├── examples.md          ← Three worked examples (high/medium/low confidence)
├── reference/
│   ├── buyer-types.md          ← All 16 buyer types with Sandler lever per type
│   ├── sandler-pain-funnel.md  ← Pain funnel + 4-frame deal check
│   ├── signal-reading-guide.md ← How to read T/F, E/I, J/P from a transcript
│   └── user-profile.md         ← Your seller profile (fill this in)
└── README.md            ← You are here
```

---

## Built By

Curtis Hays, Collideascope — [collideascope.co](https://collideascope.co)
Sandler-trained since 2011. Built from 15 years of applying that methodology to marketing agency sales, combined with behavioral profiling from 16Personalities, DISC, and Terry Bean's behavioral driver theory.

Also cohost of **Bullhorns & Bullseyes** — a podcast on marketing, brand, and revenue architecture: [bullhornsbullseyes.com](https://bullhornsbullseyes.com/)

## Acknowledgments

- **Jake Van Clief** — Interpretable Context Methodology (ICM) framework that this folder architecture is built on. [Clief Notes](https://www.skool.com/cliefnotes/about?ref=5d6ee1c3f7d14214967dc0fd5aa0888e)
- **Clief Notes / Skool** — Week 3 competition prompt that sparked this build
- **Sandler Training** — Pain funnel and qualification framework (trained 2011)
- **16Personalities** — Personality type framework and naming conventions

## License

MIT — free to use, fork, and adapt. Attribution appreciated but not required.
