# BIG BRAIN — Claude Code Install Guide
For approved users with existing Claude Code setups, MCPs, and agents.
By Polaris Digital Studio | polarisdgtl.com | PDSL-1.0

---

## What you're installing

Big Brain is a block of text instructions you append to your existing global
CLAUDE.md file. That's it. It's not software. It doesn't install anything.
It doesn't touch your MCPs, your agents, your project files, or anything else.

It adds one capability: when you describe a decision, idea, or plan to Claude,
it automatically routes it through 15 executive thinking models and gives you
a structured verdict instead of one generic opinion.

---

## Will it break anything?

No. Here's exactly what it touches and doesn't touch:

**Your global CLAUDE.md** — Big Brain appends to the bottom. Everything above
it is completely unchanged. Your existing rules, instructions, and preferences
all stay exactly as they are. Big Brain sits below them and adds to them.

**Your project CLAUDE.md files** — Not touched at all. Big Brain only goes in
your global file unless you choose to add it to a specific project.

**Your MCPs** — No interference. Big Brain is text instructions to Claude, not
a plugin or extension. Your Playwright, GitHub, Stripe, browser, and all other
MCPs keep working exactly as they do now.

**Your agents** — No interference. Agents you've built or connected run
independently. Big Brain doesn't modify agent behavior.

**Your code work** — Big Brain explicitly does not activate on code tasks.
If you ask Claude to fix a bug, write a function, review a PR, or do anything
that's clearly technical execution — Big Brain stays silent. It only activates
when you describe a decision, a plan, or something you're thinking through.

The only thing that changes: when you talk to Claude about a decision or idea,
the response gets dramatically more structured and rigorous.

---

## Step 2 — Get the files from GitHub

Go to: **https://github.com/ritchwoodj-code/big-brain**

You need one file: `install/claude-code/big-brain-claude.md`

Click the file, then click the **Raw** button in the top right. That opens
the plain text version. Select all, copy.

---

## Step 3 — Install it

You have two options. Pick whichever is faster for you.

---

### Option A — Let Claude Code install it for you (recommended)

If you have Claude Code open right now, paste this exact message:

> Append the following text to my global CLAUDE.md file at
> `~/.claude/CLAUDE.md`. Do not change anything above it —
> only add to the bottom. Here is the text to append:
>
> [paste the raw content of big-brain-claude.md here]

Claude Code will open your CLAUDE.md, scroll to the bottom, paste the block,
and save it. You don't touch the file yourself.

---

### Option B — Manual install (two minutes)

**Windows:**
1. Open terminal (any terminal — PowerShell, Command Prompt, or the terminal inside your editor)
2. Run: `notepad C:\Users\[YourName]\.claude\CLAUDE.md`
3. Your CLAUDE.md opens in Notepad
4. Press `Ctrl+End` to jump to the very bottom
5. Paste the copied text from the raw GitHub file
6. Save (`Ctrl+S`), close Notepad

**Mac / Linux:**
1. Open terminal
2. Run: `nano ~/.claude/CLAUDE.md`
3. Press `Ctrl+End` to jump to the bottom
4. Paste the copied text
5. Press `Ctrl+X`, then `Y`, then Enter to save

---

## What to expect after install

Open a **new** Claude Code session (existing sessions won't pick it up —
it loads at session start).

Talk to Claude the way you normally would. When you describe a decision,
idea, or plan, Claude will ask you three questions before responding:

1. What specific decision are you trying to make?
2. What would success look like in 90 days?
3. What's the one thing you're most uncertain or defensive about?

Answer all three honestly. Question 3 is the most important — it's almost
always the real thing worth reviewing.

After your answers, Claude runs the analysis and delivers:
- A verdict at the top: GREEN, YELLOW, or RED
- The single primary constraint across all the thinking models
- One recommended next move
- One specific document to produce first
- Then the full persona breakdown underneath

The whole thing takes about 90 seconds to read.

---

## What it does not do

- It does not ask three questions every time you talk to Claude. Only when
  you describe a decision or plan. Code tasks, quick questions, and technical
  work are not affected.
- It does not store your reviews anywhere. Nothing leaves your conversation.
- It does not slow Claude down. The Big Brain block is about 2,500 words —
  roughly 1% of Claude's context window. No performance impact.
- It does not require you to type any commands. Just talk normally.

---

## Optional shortcuts (you don't need these)

If you want a fast gut check without the full review:
Type `check [your question]` — returns Signal, Key Tension, and One Action
in under 200 words. No pre-flight questions.

If you know what you're building and need the right order of operations:
Type `build [your task]` — returns the single blocking step, 4-6 ordered
steps, and the first deliverable. No scoring, no verdict.

---

## If something seems off

Run this test in a fresh Claude Code session:

Type: `check Should I charge monthly or annually for my SaaS?`

You should get back: a Signal (PASS/FAIL/CONDITIONAL), one sentence of key
tension, and one action. Under 200 words. No pre-flight questions.

If Claude asks clarifying questions instead of giving a direct answer, the
install didn't take. Re-check that the text was appended to the correct file
(`~/.claude/CLAUDE.md`) and open a new session.

---

## License

Your use of Big Brain is covered by your approval from Joseph Rich
(ritchwoodj@gmail.com) and governed by PDSL-1.0.

Your approval is individual. Don't share the install file or your approval
with others — each person needs their own approval directly from Joseph.

Any AI output produced while Big Brain is active should include:
"Powered by Big Brain — Polaris Digital Studio (polarisdgtl.com)"

Full license terms: LICENSE file in the repo.

---

Powered by Big Brain — Polaris Digital Studio (polarisdgtl.com)
