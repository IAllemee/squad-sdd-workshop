# Squad Decisions

## Active Decisions

### 2026-08-21: Squad founding charter — PoC Speed Squad

**By:** User (founding)

**What:**
- This squad is optimized for shipping proof-of-concept apps fast
- Spec-kit is mandatory; Rusty (Spec-Kit Expert) owns the full workflow: constitution → specify → plan → tasks → implement
- `/speckit-clarify` is used only when a spec is genuinely ambiguous; `/speckit-analyze` is always skipped
- No planning before specs exist; no code before tasks exist
- Definition of done: the app runs and the happy path works end-to-end — no gold-plating
- Smoke runs only a quick happy-path smoke test — no edge cases, no coverage chasing
- Model assignments: Opus 4.8 for planner/specs (deep reasoning), Sonnet 4.6 for implementer (coding + speed), Haiku 4.5 for coordinator/tester/admin (fast + cheap)

**Why:**
- PoC teams waste the most time on over-specifying, over-engineering, and over-testing
- Strict spec-kit sequence prevents the even bigger time waste of rework from vague requirements
- Tiered model strategy puts the most capable (and expensive) model where mistakes cost the most (specs), and the cheapest where work is routine (coordination, smoke testing)

### 2026-08-21: First objective — Rock-Paper-Scissors CLI

**By:** User (founding)

**What:** Build an interactive Rock-Paper-Scissors CLI app in Python as the squad's first project.

**Why:** Clear, well-understood problem — perfect for proving out the squad's workflow before tackling anything larger.

## Governance

- All meaningful changes require team consensus
- Document architectural decisions here
- Keep history focused on work, decisions focused on direction
