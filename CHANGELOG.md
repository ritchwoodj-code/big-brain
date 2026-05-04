# BIG BRAIN — CHANGELOG
Big Brain by Polaris Digital Studio | polarisdgtl.com

All versions documented here. Approved users should check this file
periodically to know if their install is current.

---

## v1.2.0 — 2026-05-04

### Added
- **Discipline Gate** (Step 2.5) — automatic 3-check filter that runs after routing,
  before every review. Shark Tank Check (real customer?), Nasty Investor Check (what
  kills it first?), and Bezos Check (day-one customer success). Any unanswered gap
  becomes the primary constraint regardless of persona signals.
- **Quick Check command** (`@BigBrain check [thing]`) — 2 personas, no pre-flight,
  Signal + Key Tension + One Action, under 200 words. For fast decisions.
- **Build command** (`@BigBrain build [task]`) — CTO + Tesla + Musk, returns Rate Limiter
  + Ordered Steps (4-6) + First Deliverable. No signals. No verdict. Pure execution planning.
- `docs/friend-guide.md` — plain-English guide covering workflow, storage, memory usage,
  verification, and commands for new users unfamiliar with the framework.
- Operating rules updated: 9 → 12 rules to cover Discipline Gate, Quick Check, and Build mode.

### Changed
- All install files updated to include Discipline Gate, Quick Check, and Build commands.
- Commands table expanded from 4 to 6 commands across all platforms.
- `@BigBrain review` now explicitly includes Discipline Gate in its description.

---

## v1.1.0 — 2026-05-04

### Added
- Pre-flight intake block (3 questions run before every review)
- Verdict-first format (Mega Room Verdict now leads, persona breakdown follows)
- `docs/reading-signals-correctly.md` — signal calibration guide
- `docs/eval-suite.md` — 5 canonical test cases with expected signal outputs
- `docs/team-deployment.md` — team and engineering group deployment guide
- `docs/enterprise-license.md` — pricing tiers for teams and organizations
- `CHANGELOG.md` — this file
- `APPROVAL-TEMPLATE.md` — approval email template + referral nomination path
- VERSION line added to all install files
- Adversarial persona requirement formalized in all install formats
- Required artifact + exit criteria added to every persona section
- `/cluster` command added (run one cluster only)
- `docs/reading-signals-correctly.md` replaces simple wrong-answer example

### Changed
- Scoring matrix upgraded from 1–5 to 1–10 scale
- Four archetype clusters added as primary organizing structure
- Routing matrix now includes adversarial counterweight column
- Staged review protocol (5 stages) formalized in system prompt

---

## v1.0.0 — 2026-05-04

### Initial release
- 15 Mega Room personas with primary lens, question, and blind spot
- Auto-routing matrix by decision type
- Standardized review output format
- Install formats: Claude Code, Cursor/Windsurf, ChatGPT, Universal
- PDSL-1.0 license
- `docs/personas-reference.md` — full persona profiles + adoption guide
- `docs/review-example.md` — sample review output

---

To verify your current version: check the VERSION line at the top of your
install file. If it doesn't match the latest above, re-download your platform's
install file from the repo.
