# Buyer Profiler

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Built with: Claude](https://img.shields.io/badge/Built%20with-Claude-D97757.svg)](https://claude.ai)
[![Methodology: ICM](https://img.shields.io/badge/Methodology-ICM-blue.svg)](https://www.skool.com/cliefnotes)

**Most deals don't die at the close. They die at the open.**

A folder-based AI specialist for Claude. Drop the folder into a Claude project. Claude becomes the specialist. Reusable. Shareable. Portable.

---

## Who This Is For

A peer told me once: *"The fortune is in the follow-up."*

I thought that was great advice. I repeated it for ten years. I built CRM workflows around it. I bought books about it. And I still wasn't closing the deals I should have been closing.

It took me a decade to realize the problem wasn't *that* I followed up — it was *how* I followed up. I was sending the same kind of follow-up to every prospect. The Commander got my "checking in" email. The Logistician got my "ready when you are" nudge. Both went silent. Not because I wasn't persistent. Because I was generic.

The fortune isn't in the follow-up. The fortune is in **knowing what to say to *this* person on the next call.** That's a read problem, not a persistence problem.

If you've ever lost a deal you should have won and couldn't say exactly why — this folder is for you.

**Specifically:**
- **Founders selling their own services** — closing a $5K–$50K deal where one bad call costs you a full month of revenue
- **Account executives carrying quota** — running discovery calls where the difference between read-the-room and miss-the-room is your variable comp
- **Agency owners** — proposing engagements where a single mismatch costs you a multi-month retainer
- **Sales coaches and managers** — reviewing rep transcripts and trying to diagnose *why* a deal stalled

If you can read your prospect, you can close them. This folder helps you read them.

---

## How to Use It

Three ways to run it. Pick the one that matches your setup.

### Option 1 — Claude Projects (claude.ai web app)

The cleanest path. The five-file ICM spec is what this is designed for.

1. Create a new project at [claude.ai](https://claude.ai)
2. Upload all files **except** `CLAUDE.md` (Anthropic's project system handles file loading automatically)
3. (Optional but recommended) Open `reference/user-profile.md` and fill in your own seller profile — unlocks the Seller-Buyer Dynamic section
4. Paste a transcript and say: **"Profile this buyer and give me my close strategy."**

### Option 2 — Claude Desktop (local folder mode)

Works as a standalone agent pointed at the folder on disk.

1. Clone this repo locally: `git clone https://github.com/chays77/buyer-profiler.git`
2. In Claude Desktop, point a new chat at the folder (the file picker shows `Instructions · CLAUDE.md` when loaded correctly)
3. (Optional) Fill in `reference/user-profile.md`
4. Paste a transcript and say: **"Profile this buyer and give me my close strategy."**

`CLAUDE.md` is the entry contract that tells Claude Desktop what to load and in what order. Without it, the agent reads files lazily and ignores the rules.

### Option 3 — Drop into your existing ICM workspace

Already running an ICM folder structure? You can fold this specialist into it.

1. Copy `identity.md`, `rules.md`, `examples.md`, and the `reference/` folder into your specialist directory
2. **Delete `CLAUDE.md`** — your parent ICM already governs file loading
3. Hand the user prompt to your routing layer the same way you do other specialists

Expect output that looks like the example below.

---

## What You Get

Every run produces a **two-tier output** — a Quick Read at the top so you know what to do in 30 seconds, then a Deep Read below the fold with the diagnostic reasoning if you want to see the work.

**Quick Read (above the fold):**
- Buyer name + type + confidence
- One-line plain-English read on how they decide
- Critical Sandler gap (the one thing most likely to kill the deal)
- Failure mode (how this deal specifically dies for this buyer)
- Your single most important next move

**Deep Read (below the fold):**
1. **Buyer Profile** — Jung cognitive function stack (Te-Si-Ne-Fi, Ti-Ne-Si-Fe, etc.) translated into plain English, behavioral driver, evidence with function tags, inferior-function blind spot
2. **Sandler Frame Check** — what's known and unknown across Pain / Budget / Decision / Control
3. **Close Strategy** — exact language for the next call, what to hold back

If `reference/user-profile.md` is filled out, you also get:

4. **Seller-Buyer Dynamic** — how your natural selling style interacts with this buyer's type, and where you need to compensate

If `reference/user-profile.md` is empty, the specialist asks once at the bottom whether you want to share your own type — answer if you want sharper close advice, ignore it if you don't.

---

## Example Output

```
## Quick Read

**Buyer:** Sarah Chen — Commander (ENTJ)
**Confidence:** High — three aligned signals
**How they decide:** Metrics first, vision second, gut feeling last. Rejects process theater, wants the number.
**Critical gap:** Pain has no dollar number — proposal without it anchors on price alone
**Failure mode:** Over-explain process or lead with relationship. Deal dies in the first 3 minutes.
**Your single most important move:** Open the next call asking what the unsolved problem has cost her in revenue or time. Get the dollar number on the table before pitching anything.

---

## Deep Read

### Buyer Profile

**Type:** Commander (ENTJ)
**Cognitive stack:** Te-Ni-Se-Fi — leads with metrics and external logic, backed by long-range vision; values sit underneath and surface late.

**Evidence:**
- "I don't need a strategy deck" → Te rejecting process theater, wants measurable output
- Asked for close rate metric before any relationship signal → Te dominant, Fi inferior
- References two past agencies → Te audit pattern before commitment

**Primary driver:** Fire — drive to acquire. Win-oriented.
**Blend notes:** Commander with Executive lean — appetite for proven-process accountability alongside the strategic horizon.
**Inferior function blind spot:** Inferior Fi — won't surface values misalignment themselves. If you sense it, name it for them.

---

### Sandler Frame Check

| Dimension | Status |
|---|---|
| Pain | Partially identified. Past failures are symptoms. Dollar cost not yet named. |
| Budget | Unknown. |
| Decision | Likely sole decision-maker — confirm. |
| Control | Theirs right now. Reclaim with a specific next step. |

---

### Close Strategy

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

The five-file ICM spec (identity, rules, examples, reference/, README) is unchanged. `CLAUDE.md` is a deployment helper that lets the folder run portably in Claude Desktop's local-folder mode — it is optional in Claude Project mode (Anthropic's project system already handles file loading). The diagnostic logic and output spec live in `identity.md` and `rules.md`; `CLAUDE.md` only restates the entry contract.

```
buyer-profiler/
├── CLAUDE.md                    ← Entry contract for Claude Desktop (optional in Claude Projects)
├── identity.md                  ← Who the specialist is
├── rules.md                     ← How it responds, output format, activation logic
├── examples.md                  ← Four worked examples (high/medium/low/multi-buyer)
├── reference/
│   ├── buyer-types.md           ← All 16 buyer types — cognitive stack + Sandler lever per type
│   ├── cognitive-functions.md   ← The 8 Jung functions (Te, Ti, Fe, Fi, Ne, Ni, Se, Si) — diagnostic engine
│   ├── sandler-pain-funnel.md   ← Pain funnel + 4-frame deal check
│   ├── signal-reading-guide.md  ← How to read functions and traits from a transcript
│   └── user-profile.md          ← Your seller profile (fill this in)
└── README.md                    ← You are here
```

---

## Troubleshooting

**The agent produces a coaching memo about *me* instead of profiling the buyer in the transcript.**
The seller-coaching pull from `reference/user-profile.md` is overriding the buyer diagnostic. Confirm two things: (1) you're running v3 or later (check that `identity.md` contains a "Your Job — Profile the Buyer" section), and (2) you're starting a fresh chat — earlier conversations anchor the agent's behavior even after rules change.

**The agent doesn't read the folder files in Claude Desktop.**
Claude Desktop's local-folder mode requires `CLAUDE.md` at the folder root. Without it, files load lazily and rules get ignored. Confirm `CLAUDE.md` is present and that the file picker shows `Instructions · CLAUDE.md` when the folder loads.

**The agent drafts a full email with subject line, body, and signature.**
That's the proposal-writing leak. v3 forbids it explicitly. If it still happens, you're either on an older version of the repo or running it inside a parent project whose rules override these. Pull latest and start a fresh session.

**The agent skips the buyer profile and goes straight to tactics.**
Your input may have been routed as a coaching question rather than a transcript. Try the explicit prompt: *"Profile this buyer and give me my close strategy."* That triggers the activation rule cleanly.

**The Quick Read or Sandler Frame Check is missing entirely.**
The agent isn't reading `rules.md`. Most likely cause in Claude Desktop: missing or malformed `CLAUDE.md`. In Claude Projects: the file may not have uploaded — check the project knowledge panel.

**The agent doesn't ask for my seller profile.**
By design — the prompt-back is non-blocking and appears at the bottom of the output, not the top. Scroll to the end. If `reference/user-profile.md` is filled in already, no prompt fires.

---

## Built By

Curtis Hays, Collideascope — [collideascope.co](https://collideascope.co)
Sandler-trained since 2011. Built from 15 years of applying that methodology to marketing agency sales, combined with behavioral profiling from 16Personalities, DISC, and Terry Bean's behavioral driver theory.

Also cohost of **Bullhorns & Bullseyes** — a podcast on marketing, brand, and revenue architecture: [bullhornsbullseyes.com](https://bullhornsbullseyes.com/)

## Acknowledgments

- **Dave Tear, Sales Coaches' Corner** — My sales coach. The principle that anchors this entire specialist — "most deals don't die at the close, they die at the open" — is Dave's. So is the discipline around qualifying pain, money, and decision authority before pitching. 30+ years coaching salespeople, originally Sandler-trained under Jerry Weinberg. [salescoachescorner.com](https://www.salescoachescorner.com/)
- **Jake Van Clief** — Interpretable Context Methodology (ICM) framework that this folder architecture is built on. [Clief Notes](https://www.skool.com/cliefnotes/about?ref=5d6ee1c3f7d14214967dc0fd5aa0888e)
- **Clief Notes / Skool** — Week 3 competition prompt that sparked this build
- **Terry Bean, Behavioral Elements** — The Fire / Earth / Water / Air behavioral driver framework that runs underneath every buyer type read. Terry's model maps primary drivers (acquire / defend / bond / learn) to how someone shows up in conversation. [behavioralelements.com](https://behavioralelements.com/)
- **Sandler Training** — Pain funnel and qualification framework (trained 2011)
- **Carl Jung** — The eight cognitive functions (Te, Ti, Fe, Fi, Ne, Ni, Se, Si) and the four-function stack model. The deepest diagnostic layer in this specialist — what makes a Commander different from an Executive, or a Logician different from an Architect, isn't trait scores. It's which functions they lead with and which one's their blind spot.
- **16Personalities** — Personality type framework and naming conventions (the 16 type names sit on top of Jung's stacks)

## License

MIT — free to use, fork, and adapt. Attribution appreciated but not required.
