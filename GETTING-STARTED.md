# Getting Started — Buyer Profiler

Everything you need to go from clone to your first profile in under 15 minutes.

---

## What This Is

The Buyer Profiler is a folder-based AI specialist for Claude. Drop it into a Claude project and it turns Claude into a specialist who reads your sales prospects and tells you exactly how to close them — based on who they are, not a generic playbook.

Every output has two parts:
1. **Buyer Profile** — cognitive type, behavioral driver, what moves them, how deals die with this type
2. **Close Strategy** — exact language for the next call, Sandler frame check, what to hold back

If you've filled out `user.md`, you also get:
3. **Seller-Buyer Dynamic** — how *your* natural selling style interacts with *this* buyer's type, and where you need to compensate

---

## Step 1 — Set Up in Claude

1. Go to [claude.ai](https://claude.ai) and create a **new Project**
2. In the Project, click **Add content** → upload this entire folder
3. Claude is now the Buyer Profiler for every conversation in that project

> **One project = one specialist.** Keep this project dedicated to the Buyer Profiler. Don't mix it with other work — selective context loading only works if the folder is the whole project.

---

## Step 2 — Fill Out Your Seller Profile

Open `user.md` and complete it before running any transcripts. This takes 5–10 minutes and unlocks the Seller-Buyer Dynamic section in every output.

The most important fields:
- Your 16Personalities type (take the free test at [16personalities.com](https://www.16personalities.com) if you don't know it)
- Your primary behavioral driver (Fire / Earth / Water / Air)
- Your known Sandler gaps — be honest, these are the patterns costing you deals

You only do this once. Update it when your selling context changes.

---

## Step 3 — Get a Transcript

You need a record of a sales conversation. It doesn't need to be perfect — even rough notes work. Here's how to get one:

### AI Meeting Recorders (recommended)

These tools join your Zoom, Google Meet, or Teams call automatically and produce a transcript you can paste directly into Claude.

| Tool | Best for | Notes |
|---|---|---|
| **[Granola](https://granola.so)** | Mac users, clean summaries | Runs locally, combines your notes + audio |
| **[Otter.ai](https://otter.ai)** | Any platform, real-time | Free tier available, good accuracy |
| **[Fireflies.ai](https://fireflies.ai)** | Teams with shared meeting notes | CRM integrations available |
| **[Google Meet + Gemini Notes](https://workspace.google.com)** | Google Workspace users | Built into Meet if you have Gemini add-on |
| **[Fathom](https://fathom.video)** | Zoom-first, fast summaries | Free tier, very clean output |

### Manual options

- **Call notes** — bullet points from the call work fine. 5–10 sentences minimum.
- **Email thread** — a back-and-forth email exchange gives enough signal for a Low-confidence profile
- **Voice memo transcribed** — record a debrief right after the call, run it through Otter or [Whisper](https://openai.com/research/whisper)

---

## Step 4 — Run Your First Profile

Paste your transcript into the Buyer Profiler project and send this message:

> "Profile this buyer and give me my close strategy."

To get the best output, add one line of deal context after the transcript:

> "This was a first discovery call. I haven't proposed anything yet. She was referred by a mutual contact. We sell [what you sell] at [price range]."

That's it. The specialist activates immediately.

---

## Step 5 — Save the Output

Copy the profile output and save it to the `output/` folder using this naming convention:

```
YYYY-MM-DD-[prospect-slug]-profile.md
```

Examples:
- `2026-05-07-jane-smith-profile.md`
- `2026-05-14-acme-cfo-profile.md`

Pull it up before every subsequent call with that prospect. You don't need to re-run the full transcript each time — paste the saved profile and ask: *"I have a follow-up call tomorrow. What should I focus on?"*

---

## What Good Output Looks Like

See `examples.md` for three full worked examples:
- A high-confidence Commander read with exact close language
- A medium-confidence Logistician read with next-step strategy
- A thin transcript with a Low-confidence probe map

---

## Inbox Workflow (for teams or high volume)

If you're running multiple calls per week, set up a simple inbox:

1. Create an `inbox/` folder on your desktop (or in this repo)
2. After every sales call, drop the transcript file there
3. Name it: `YYYY-MM-DD-[prospect-name]-raw.txt`
4. At the start of each week, work through the inbox — paste each transcript into Claude, run the profile, save to `output/`

This keeps transcripts organized without any additional tooling.

---

## Troubleshooting

**"The output doesn't match the format in examples.md"**
Make sure you uploaded the entire folder to the Claude project, not just individual files. The `rules.md` file controls output format and must be present.

**"The confidence is always Low"**
Your transcripts are probably thin — under 5 minutes of substantive content, or mostly logistics talk. Try asking more open-ended questions on your calls: "Walk me through how you made your last big vendor decision" generates far more signal than "Are you interested?"

**"The type read feels wrong"**
Trust it as a working hypothesis, not a diagnosis. Add your own read in the deal context line: *"I think she might be more of a Logistician than a Commander — here's why..."* The specialist treats your note as additional signal and adjusts the read accordingly.

**"I want to update my seller profile"**
Open `user.md` in any text editor and edit it. Re-upload the folder to your Claude project. Changes take effect immediately.

---

## Built by

Curtis Hays, Collideascope — five years of Sandler methodology applied to marketing agency sales, combined with behavioral profiling from 16Personalities, DISC, and Terry Bean's behavioral driver theory. [collideascope.co](https://collideascope.co)
