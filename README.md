# Big Brain v1.1

**The board of directors you never had, now installed in your AI.**

Built by Polaris Digital Studio.

Most founders and builders make decisions from one mental model — the one
they're strongest in. A technical founder thinks like a CTO. A marketer
thinks like Nike. A growth operator thinks like Zuckerberg. That single-lens
thinking is where avoidable mistakes live.

Big Brain installs 15 executive thinking models into any AI tool you already
use. When you submit an idea, plan, or decision, it routes automatically to
the most relevant personas, runs each one's lens with hard questions and a
clear signal, and delivers a verdict with one concrete next move. No generic
advice. No "it depends." Every persona gives a PASS, FAIL, or CONDITIONAL.

---

## Before You Install

**Use requires written approval.**

This repo is public so you can evaluate what you're requesting. Use without
approval violates PDSL-1.0. To request access:

1. Email **ritchwoodj@gmail.com**
2. Subject: **Big Brain Access Request**
3. Include your name, what you're building, and which AI tool you use

For teams of 5 or more, see [docs/enterprise-license.md](./docs/enterprise-license.md)
for team and studio pricing.

---

## What It Does

You run three quick pre-flight questions to frame your decision. Then Big Brain:

1. Identifies the decision type (idea validation, tech architecture, brand, execution, etc.)
2. Selects the 4-6 most relevant personas plus an adversarial counterweight
3. Each persona gives a signal (PASS / FAIL / CONDITIONAL), a key insight, and one hard question
4. The Mega Room Verdict leads: GREEN / YELLOW / RED, one primary constraint, one next move, one artifact to produce first

The most important rule in the system: no mono-persona governance. Musk without CTO creates operational damage. Bezos without Jony yields efficient blandness. Jony without Bezos yields beautiful irrelevance. Big Brain enforces the combination.

---

## The 15 Mega Room Personas

| Persona | Cluster | Primary Lens |
|---|---|---|
| CTO | Architecture & Reliability | "What will break and who owns it?" |
| Bill Gates | Architecture & Reliability | "Where is the compounding leverage?" |
| Sundar Pichai | Architecture & Reliability | "How do we scale without breaking trust?" |
| SpaceX / Starlink | Architecture & Reliability | "Where are the single-point failures?" |
| ChatGPT Coordinator | Architecture & Reliability | "Where does the system fail at scale?" |
| Nasty Investor | Capital & Discipline | "What kills this before the upside matters?" |
| Shark Tank | Capital & Discipline | "Pain obvious, numbers credible, why now?" |
| Jeff Bezos | Capital & Discipline | "What's the PR/FAQ and which proxy misleads us?" |
| Elon Musk | Speed & Integration | "Which assumptions are inherited norms, not facts?" |
| Jensen Huang | Speed & Integration | "What's the software moat?" |
| Tesla | Speed & Integration | "Where's the real bottleneck?" |
| Mark Zuckerberg | Speed & Integration | "How does this become a network?" |
| Jony Ive | Emotional Leverage | "What can be removed?" |
| Nike | Emotional Leverage | "What identity does this signal?" |
| Disney / Pixar | Emotional Leverage | "What emotional truth extends into experience?" |

For full persona profiles, thinking models, artifacts, and exit criteria:
[docs/personas-reference.md](./docs/personas-reference.md)

---

## Install Instructions

### Option 1 — Claude Code (Global)

1. Open terminal
2. Run: `notepad C:\Users\[YourName]\.claude\CLAUDE.md` (Mac/Linux: `nano ~/.claude/CLAUDE.md`)
3. Scroll to the bottom of your existing CLAUDE.md
4. Copy all of `install/claude-code/big-brain-claude.md`
5. Paste at the bottom. Save.

Active in every Claude Code session. Commands:
- `@BigBrain review [decision]` — auto-routes to relevant personas
- `@BigBrain /mega-room [decision]` — all 15 personas
- `@BigBrain /persona [name]` — single persona
- `@BigBrain /cluster [name]` — one cluster

For per-project install: paste into your project's `CLAUDE.md` instead.

---

### Option 2 — Cursor or Windsurf

1. Copy `install/cursor/.cursorrules` into your project root
2. Restart Cursor or Windsurf

For Cursor's rules format: also add to `.cursor/rules/` renamed as `big-brain.mdc`.

---

### Option 3 — ChatGPT Custom Instructions

1. ChatGPT → profile icon → Settings → Personalization → Custom Instructions
2. Click "How should ChatGPT respond?"
3. Copy `install/chatgpt/custom-instructions.txt` and paste in
4. Save

---

### Option 4 — Any AI (Universal)

1. Copy all of `install/universal/system-prompt.txt`
2. Paste at the very start of a new conversation with any AI
3. Submit your decision

Works with Claude.ai, Gemini, Copilot Chat, Perplexity, and any AI with
a system prompt or context window.

---

## Commands

| Command | What It Does |
|---|---|
| `@BigBrain review [decision]` | Pre-flight + auto-routes to 4-6 personas |
| `@BigBrain /mega-room [decision]` | All 15 personas across all 5 stages |
| `@BigBrain /persona [name]` | Single persona mode |
| `@BigBrain /cluster [name]` | One cluster only |

---

## For Teams

Big Brain is built for individual use but deploys well across teams.
See [docs/team-deployment.md](./docs/team-deployment.md) for:
- Who should own Big Brain on your team
- How to run async and live team reviews
- Version management across multiple installs
- When to run a full Mega Room vs. a quick 4-persona check

For team and studio licensing: [docs/enterprise-license.md](./docs/enterprise-license.md)

---

## File Map

```
big-brain/
├── LICENSE                              PDSL-1.0
├── README.md                            This file
├── CHANGELOG.md                         Version history
├── APPROVAL-TEMPLATE.md                 For Joseph's use (approval emails, referrals)
├── install/
│   ├── claude-code/
│   │   └── big-brain-claude.md         Claude Code install block
│   ├── cursor/
│   │   └── .cursorrules                Cursor / Windsurf
│   ├── chatgpt/
│   │   └── custom-instructions.txt     ChatGPT Custom Instructions
│   └── universal/
│       └── system-prompt.txt           Universal (any AI)
└── docs/
    ├── friend-guide.md                 Plain-English guide for new users (start here)
    ├── personas-reference.md           Full 15 persona profiles + adoption guide
    ├── review-example.md               Sample review output
    ├── reading-signals-correctly.md    How to interpret GREEN/YELLOW/RED
    ├── eval-suite.md                   5 canonical test cases for QA
    ├── team-deployment.md              Engineering team deployment guide
    └── enterprise-license.md          Pricing tiers for teams and orgs
```

---

## Version

Current: **v1.1** — May 2026
See [CHANGELOG.md](./CHANGELOG.md) for what changed.
Check CHANGELOG monthly and update your install file if behind.

---

## License

Big Brain is licensed under the Polaris Digital Studio License v1.0 (PDSL-1.0).

Use requires written approval. No sublicensing. No resale.
Attribution required: "Powered by Big Brain — Polaris Digital Studio (polarisdgtl.com)"

See [LICENSE](./LICENSE) for full terms.
See [docs/enterprise-license.md](./docs/enterprise-license.md) for team pricing.

---

*Polaris Digital Studio — polarisdgtl.com*
*ritchwoodj@gmail.com*
