# BIG BRAIN — EVAL SUITE
Big Brain by Polaris Digital Studio | polarisdgtl.com
License: PDSL-1.0

This document contains 5 canonical test cases. Use these to verify that
a system prompt update has not degraded output quality. Run each test,
compare the output signals to the expected signals below, and flag any
significant deviation before shipping the update.

A "significant deviation" means:
- A PASS flips to FAIL (or vice versa) with no change to the submission
- The Overall Signal changes by more than one level (GREEN → RED)
- The primary constraint identified differs substantially from the expected one
- The routing decision selects materially different personas

Minor wording differences are expected and acceptable.

---

## TEST CASE 1 — Idea Validation (should return YELLOW)

**Pre-flight answers:**
1. Decision: Whether to build a meal planning app with AI menu generation.
2. 90-day success: 100 paying users at $9.99/month.
3. Most uncertain about: "Whether the AI output is good enough to retain users."

**Submission:**
An app that uses AI to generate weekly meal plans based on dietary preferences,
budget, and what's already in the fridge. Target user: busy professionals 25-40
who want to eat well but don't have time to plan. Business model: $9.99/month
subscription. Plan to acquire users through Instagram and TikTok content.

**Expected routing:** Idea validation — Shark Tank, Nasty Investor, Bezos, Jony Ive.
Adversarial: Nasty Investor doubles as the hardest check.

**Expected signals:**

| Persona | Expected Signal | Reason |
|---|---|---|
| Shark Tank | CONDITIONAL | Pain is real but market is very crowded. Proof of differentiation is weak. |
| Nasty Investor | FAIL | No moat stated. Competitors (Instacart, Kroger, MyFitnessPal) can ship this feature. No cohort data. |
| Jeff Bezos | CONDITIONAL | PR/FAQ could be written, but proxy trap: "retention" is not the same as "delight." |
| Jony Ive | CONDITIONAL | "AI-generated meal plan" has no coherent object. The UX is unresolved. |

**Expected Overall Signal:** YELLOW
**Expected Primary Constraint:** Competitive moat is absent. The product as described is a feature that incumbents can replicate. The AI output quality question (flagged in pre-flight) is actually secondary to the differentiation question.

---

## TEST CASE 2 — Tech Architecture (should return GREEN)

**Pre-flight answers:**
1. Decision: Whether to migrate from a monolithic Rails app to microservices.
2. 90-day success: Core checkout flow extracted into its own service, zero downtime.
3. Most uncertain about: "Whether the team is experienced enough to manage distributed systems."

**Submission:**
A 6-year-old e-commerce platform on Rails monolith, ~200k DAU, 8 engineers.
The checkout flow is the most business-critical piece. Plan is to extract it
first, then progressively decompose over 18 months. Team has one engineer with
microservices experience.

**Expected routing:** Tech architecture — CTO, SpaceX/Starlink, Musk, Tesla.
Adversarial: Bezos on customer value.

**Expected signals:**

| Persona | Expected Signal | Reason |
|---|---|---|
| CTO | CONDITIONAL | PRR must exist before checkout extraction. Single engineer with microservices experience is a key risk. Named ownership of the new service is unclear. |
| SpaceX / Starlink | PASS | Progressive decomposition is the right approach. Checkout-first is the right sequencing (highest criticality = highest learning value). |
| Elon Musk | CONDITIONAL | 18-month timeline suggests the decomposition plan hasn't been reduced to its physical constraints. What is the actual rate limiter? |
| Tesla | PASS | Phased approach (checkout → others) mirrors ramp logic. Rate limiter is team experience, not architecture. |
| Jeff Bezos (adversarial) | PASS | Customer impact is addressed by the zero-downtime goal. Proxy trap: "service extracted" is not the same as "checkout is more reliable." |

**Expected Overall Signal:** GREEN
**Expected Primary Constraint:** Team experience with distributed systems. The architectural decision is correct; the execution risk is human, not technical.

---

## TEST CASE 3 — Brand/Creative (should return YELLOW)

**Pre-flight answers:**
1. Decision: Whether to rebrand from "QuickBooks-style" to "premium/editorial."
2. 90-day success: New brand live, 20% increase in enterprise inquiry rate.
3. Most uncertain about: "Whether existing SMB customers will feel alienated."

**Submission:**
A B2B accounting software company, 5 years old, 3,000 SMB customers,
starting to win enterprise deals. Current brand is utilitarian and dated.
Wants to rebrand to attract CFOs at mid-market companies. Budget: $80k
for a full rebrand including new website, visual identity, and positioning.

**Expected routing:** Brand/narrative — Nike, Disney/Pixar, Jony Ive.
Adversarial: Shark Tank.

**Expected signals:**

| Persona | Expected Signal | Reason |
|---|---|---|
| Nike | CONDITIONAL | "Premium" is not an identity. What is the athlete truth for a CFO? The emotional positioning is undefined. |
| Disney / Pixar | PASS | The story is clear: "From scrappy tool to trusted financial intelligence." That's extendable. |
| Jony Ive | CONDITIONAL | $80k for a rebrand without a resolved product experience is backwards. The software UX should change first, or simultaneously. Brand coherence fails if the product still looks SMB while the brand looks enterprise. |
| Shark Tank (adversarial) | CONDITIONAL | The 20% enterprise inquiry increase metric doesn't prove the rebrand caused it. What's the current enterprise inquiry baseline? |

**Expected Overall Signal:** YELLOW
**Expected Primary Constraint:** Jony Ive's CONDITIONAL is the blocker — the product experience and the brand must move together. A premium visual identity on top of a utilitarian UX will create distrust at the sales stage.

---

## TEST CASE 4 — AI Platform Product (should return GREEN)

**Pre-flight answers:**
1. Decision: Whether to build a proprietary LLM fine-tuned on legal contracts.
2. 90-day success: 10 law firms in a pilot program, NPS > 40.
3. Most uncertain about: "Whether fine-tuning is actually better than prompt engineering for this use case."

**Submission:**
A legal tech startup building an AI contract review tool. The plan is to
fine-tune an open-source LLM on 500,000 anonymized contracts from willing
law firm partners. The software identifies risk clauses, suggests edits, and
flags non-standard terms. Target customer: mid-market law firms 20-150 attorneys.
Current revenue: $0. Funding: $1.2M seed.

**Expected routing:** AI platform — Jensen, Gates, Pichai, Zuckerberg, ChatGPT Coordinator.
Adversarial: Nasty Investor.

**Expected signals:**

| Persona | Expected Signal | Reason |
|---|---|---|
| Jensen Huang | CONDITIONAL | Fine-tuning vs. prompt engineering is the rate-limiting question. The throughput metric is contract accuracy, not model size. Resolve this before committing to fine-tuning infrastructure. |
| Bill Gates | PASS | Bottleneck in legal AI is data quality and trust, not raw model performance. The 500k contract dataset is the real moat if protected. |
| Sundar Pichai | CONDITIONAL | Launch narrow (one contract type, one jurisdiction) before expanding. Quality at scale requires a quality gate at launch. |
| Zuckerberg | PASS | Network loop exists: more law firms → more contract data → better model → more law firms. This compounds. |
| ChatGPT Coordinator | CONDITIONAL | Evals are undefined. "NPS > 40" is a user satisfaction metric, not a contract accuracy metric. The grader for this system needs to measure legal accuracy, not happiness. |
| Nasty Investor (adversarial) | CONDITIONAL | $1.2M seed with $0 revenue and a fine-tuning infrastructure decision is a high burn path. What is the runway, and when does the pilot need to convert to paying customers? |

**Expected Overall Signal:** GREEN
**Expected Primary Constraint:** The fine-tuning vs. prompt engineering decision must be resolved before infrastructure is built. Getting that wrong at this funding level means losing 3-4 months of runway.

---

## TEST CASE 5 — Execution Plan (should return RED)

**Pre-flight answers:**
1. Decision: Whether to launch in 5 countries simultaneously in Q3.
2. 90-day success: 1,000 paid users across all 5 countries.
3. Most uncertain about: "Whether the localization is complete enough."

**Submission:**
A SaaS project management tool, 18 months old, 800 paying customers in the US.
Plan to launch simultaneously in UK, Canada, Australia, Germany, and France in
Q3. The product has been partially localized (UI text translated, but not
payment flows, tax handling, customer support, or legal compliance). Team
is 12 people. No country managers hired. No local partnerships established.

**Expected routing:** Execution plan — Tesla, Bezos, Musk, CTO.
Adversarial: Nasty Investor.

**Expected signals:**

| Persona | Expected Signal | Reason |
|---|---|---|
| Tesla | FAIL | The rate limiter is not "localization is complete enough." The rate limiter is 4 unresolved operational systems (payments, tax, support, legal). Simultaneous 5-country launch with 12 people and no local presence is a ramp that violates basic execution logic. |
| Jeff Bezos | FAIL | There's no PR/FAQ for any of the 5 markets. "1,000 users across 5 countries" is a proxy for success, not a definition of it. What does a German customer's experience look like day 1? Nobody has written that yet. |
| Elon Musk | FAIL | The assumptions underlying this plan are inherited from US-market behavior, not first principles. The cost tree for UK+Canada (similar market) vs. Germany+France (different language, different compliance) is not the same. They shouldn't launch together. |
| CTO | FAIL | Payment flows, tax handling, and legal compliance are not localization — they're operational infrastructure. Launching without them is not a product risk. It's a legal and trust risk. |
| Nasty Investor (adversarial) | FAIL | 5 simultaneous country launches with incomplete infrastructure, no local staff, and 12 people is a dilution of every resource the company has. The most likely outcome is 5 bad launches instead of 1 strong one. |

**Expected Overall Signal:** RED
**Expected Primary Constraint:** The plan is structurally unsound. Five simultaneous launches with unresolved payment, tax, legal, and support infrastructure across markets with different compliance requirements will damage the brand in every market. The right answer is sequence: UK+Canada first (easiest compliance delta), then Australia, then Germany+France as a separate initiative after 6 months of operational learning.

---

---

## TEST CASE 6 — Discipline Gate: Gap Detection (should flag two gaps)

**How to run:**
Submit this as `@BigBrain review` with the pre-flight answers below. Do NOT add any
additional context. The sparse answers are intentional — they're what the gate is designed to catch.

**Pre-flight answers:**
1. Decision: Whether to build a productivity app for remote workers.
2. 90-day success: "Get users and grow."
3. Most uncertain about: "Not sure if people will pay for it."

**Submission:**
An app that helps remote workers stay focused. Features include a Pomodoro timer,
distraction blocker, and daily goal tracking. Business model TBD. Planning to launch
on Product Hunt and post about it on Reddit.

**Expected routing:** Idea validation — Shark Tank, Nasty Investor, Bezos | Adversary: Jony Ive

**Expected Discipline Gate output (before personas run):**

| Check | Expected Result |
|---|---|
| Shark Tank Check | UNANSWERED — No nameable customer. "Remote workers" is a demographic, not a customer. No evidence of demand. |
| Nasty Investor Check | UNANSWERED — "Not sure if people will pay" is not a named kill risk. Nothing specific stated. |
| Bezos Check | UNANSWERED — "Get users and grow" describes a goal for the builder, not an experience for the customer. |

**Expected behavior:** All three gaps flagged UNANSWERED. All three become the primary
constraint. The review proceeds. Persona signals should be mostly FAIL / CONDITIONAL
given the complete absence of market validation. Overall Signal should be RED or YELLOW.

**Deviation flag:** If the Discipline Gate skips or softens these gaps, the gate is
not firing correctly. Re-check that Step 2.5 is present in the install file before STEP 3.

---

## TEST CASE 7 — Quick Check (should return in under 200 words)

**How to run:**
Type this exactly into a fresh conversation with the system prompt active:

`@BigBrain check Should I charge monthly or annually for my SaaS?`

**Expected behavior:**
- No pre-flight questions asked
- No routing statement
- 2 personas selected (likely Nasty Investor + Bezos, or Shark Tank + Bezos)
- Output contains exactly three things: Signal, Key Tension, One Action
- Total output under 200 words
- Ends with attribution line

**Expected Signal:** CONDITIONAL

**Expected Key Tension:** Annual pricing creates cash flow advantages but increases
conversion friction for unproven products. Monthly de-risks the purchase and produces
faster retention data, but caps early revenue. The right answer depends on churn data
you may not have yet.

**Expected One Action:** Run monthly first for 90 days. Collect churn data. Add annual
as an option (with a discount) only after you can prove 3-month retention holds.

**Deviation flags:**
- If it asks pre-flight questions: Quick Check is not working correctly.
- If output exceeds 200 words significantly: output mode is not condensed correctly.
- If more than 2 personas run: routing limit is not being respected.

---

## TEST CASE 8 — Build Mode (should return execution sequence only)

**How to run:**
Type this exactly into a fresh conversation with the system prompt active:

`@BigBrain build Launch a waitlist for a new SaaS before the product is built`

**Expected behavior:**
- No pre-flight questions asked
- No persona signals (PASS/FAIL/CONDITIONAL)
- No overall verdict (GREEN/YELLOW/RED)
- Routes to CTO + Tesla + Musk internally (doesn't need to state this)
- Output contains exactly three things: Rate Limiter, Ordered Steps, First Deliverable
- Ordered Steps: 4 to 6 steps only
- Total output under 250 words

**Expected Rate Limiter:** The offer. Without a clear, specific promise to the waitlist
subscriber, everything else (landing page, traffic, email sequence) is decoration. Nothing
moves until the offer is defined in one sentence.

**Expected Ordered Steps (approximate):**
1. Write the one-sentence offer (what they get, when, why now)
2. Build a single landing page: headline, 3 bullet benefits, email capture, no navigation
3. Set up email confirmation + waitlist welcome sequence (2 emails max)
4. Drive first 50 signups through direct outreach, not ads
5. Send a weekly "building in public" update to keep the list warm
6. Define the conversion trigger: what event turns a waitlist member into a paying customer

**Expected First Deliverable:** The one-sentence offer statement. Everything else is
blocked until this exists.

**Deviation flags:**
- If it outputs PASS/FAIL/CONDITIONAL signals: Build mode is not working.
- If it outputs a GREEN/YELLOW/RED verdict: Build mode is not working.
- If steps exceed 6: output is not condensed correctly.
- If output exceeds 250 words significantly: output mode is not condensed correctly.

---

## How to Use This Eval Suite

**For the full review tests (Cases 1-5):**
1. Copy the pre-flight answers and submission text for the test case.
2. Open a fresh conversation with the system prompt pasted at the very top.
3. Submit the pre-flight answers when Big Brain asks them, then submit the main text.
4. Compare each persona's signal to the expected signal above.
5. If more than 2 signals deviate from expected, investigate before shipping.

**For the new command tests (Cases 6-8):**
1. Open a fresh conversation with the system prompt pasted at the very top.
2. For Case 6: submit the pre-flight answers, then the submission text, as a review.
3. For Cases 7-8: type the exact command shown and submit it directly.
4. Compare the output structure and content against what's expected.
5. Check the deviation flags — these are the specific failure modes to watch for.

**Sensitivity ranking:**
- Cases 1 and 5 are the most sensitive for the full review format. If either returns GREEN, the system has optimism bias.
- Case 6 is the most sensitive for the Discipline Gate. If all three gaps don't get flagged, the gate isn't running.
- Cases 7 and 8 are format tests. If either produces signals or verdicts it shouldn't, the command definitions aren't being respected.

---

Powered by Big Brain — Polaris Digital Studio (polarisdgtl.com)
License: PDSL-1.0 | Use requires written approval from ritchwoodj@gmail.com
