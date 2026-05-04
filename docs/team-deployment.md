# BIG BRAIN — TEAM DEPLOYMENT GUIDE
Big Brain by Polaris Digital Studio | polarisdgtl.com
License: PDSL-1.0 | Team licenses available — see enterprise-license.md

This guide is for engineering teams, startups, and agencies deploying
Big Brain across multiple people. Individual install instructions are in
README.md. This document covers team structure, ownership, and protocols.

---

## Who Owns Big Brain on Your Team

Designate one person as the Big Brain owner. That person is responsible for:
- Keeping the install files current (check CHANGELOG.md monthly)
- Running the eval suite after any system prompt update
- Collecting and submitting the 30-day feedback to Joseph
- Managing which team members have active installs

In a startup of 1-10 people, this is usually the founder or product lead.
In an engineering team of 10-50, this is usually the engineering manager or
head of product.

Without a designated owner, installs drift. Different team members end up
on different versions. Reviews produce inconsistent output. The owner role
prevents that.

---

## How to Deploy Across a Team

**Step 1 — License first.**
Every person who installs Big Brain needs to be covered by a license.
Individual approvals work up to 3 people. Beyond that, a team or studio
license is cleaner. See enterprise-license.md for pricing.

**Step 2 — Pick one platform standard.**
Decide which install format your team uses. Don't mix. If your team is
on Claude Code, everyone gets big-brain-claude.md. If your team is on
Cursor, everyone gets .cursorrules. Mixing platforms creates version drift.

**Step 3 — Install and verify.**
Each person installs the file per README.md instructions, then runs
Test Case 1 from docs/eval-suite.md. If the output signals match the
expected signals, the install is correct. If not, troubleshoot before
the team starts using it on real decisions.

**Step 4 — Set a review cadence.**
Big Brain is most valuable when it's embedded in existing decision points,
not used ad-hoc. Recommended cadence:

- Weekly: Any new product or feature idea gets a Big Brain review before
  it enters the backlog. Takes 10 minutes. Prevents planning sessions
  built on unexamined assumptions.
- Monthly: Any strategic shift (new market, pricing change, architecture
  decision) gets a full Mega Room review before it's resourced.
- Quarterly: The team's current roadmap gets reviewed as a portfolio.
  Which bets would Nasty Investor kill? Which ones does Bezos love?

---

## How Team Reviews Work

Big Brain is designed for individual use, but team reviews are possible
and often more valuable. Two formats:

**Async review:** One person (usually the proposal owner) runs the pre-flight
and submits the review. They share the output in Slack/Notion/Linear with
the team. The team uses the signals and hard questions to structure their
discussion. This works well for product decisions.

**Live review:** One person drives the Big Brain session on a shared screen
during a planning meeting. The pre-flight answers are agreed on by the group
before the review starts. Each persona's output is read aloud and discussed
before moving to the next. The Mega Room Verdict becomes the meeting's
decision framework. This works well for strategic decisions.

Both formats work. The live format creates more buy-in. The async format
is faster and scales better.

---

## What Big Brain Doesn't Replace

Big Brain is a decision support tool. It doesn't replace:

- Customer interviews. Big Brain has no access to your actual customers.
  Its Shark Tank persona can ask the right questions. It can't answer them.
- Technical due diligence. The CTO persona identifies risks. It can't read
  your codebase, run your tests, or audit your infrastructure.
- Financial modeling. The Nasty Investor persona asks the right questions
  about unit economics. It's not a spreadsheet.
- Legal review. The SpaceX/Starlink reliability and CTO personas surface
  compliance and operational risks. They're not lawyers.

The reviews surface the questions. Your team provides the answers.

---

## When to Escalate to a Full Mega Room

Most decisions need 4-6 personas. Reserve the full Mega Room (all 15) for:

- A funding decision (raise vs. bootstrap, valuation, terms)
- A major product pivot
- A new market entry
- A key hire (CEO, CTO, head of sales — anyone who changes the company's
  trajectory)
- An acquisition or partnership that changes your strategic position

Full Mega Room reviews take 20-30 minutes. Budget accordingly.

---

## Version Management

Check CHANGELOG.md monthly. When a new version ships:

1. The Big Brain owner downloads the updated install file for your team's platform
2. Runs Test Cases 1 and 5 from eval-suite.md to confirm the update is clean
3. Distributes the updated file to all team members
4. Team members update their installs before the next review session

Don't let the team run on mixed versions. It produces inconsistent output
and undermines trust in the reviews.

---

## Giving Feedback That Improves the Framework

At 30 days, Joseph will send a one-question email to your license contact:
"Did Big Brain change a decision you were going to make?"

The most useful responses include:
- Which personas gave the sharpest signal on your actual decisions
- Which personas felt generic or didn't add value for your use case
- Any decision type that didn't fit any of the routing options

This data drives routing improvements in future versions. Teams with
enterprise licenses get those improvements first.

---

Powered by Big Brain — Polaris Digital Studio (polarisdgtl.com)
License: PDSL-1.0 | ritchwoodj@gmail.com for team and enterprise licenses
