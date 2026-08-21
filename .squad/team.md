# Squad Team

> squad-sdd-workshop — PoC Speed Squad

## Coordinator

| Name | Role | Model | Notes |
|------|------|-------|-------|
| Squad | Coordinator | claude-haiku-4.5 | Routes work, enforces handoffs. Lightweight admin — fast and cheap. |

## Members

| Name | Role | Charter | Model | Status |
|------|------|---------|-------|--------|
| Rusty | Spec-Kit Expert & Lead Planner | `.squad/agents/rusty/charter.md` | claude-opus-4.8 | 🟢 Active |
| Flash | Implementer | `.squad/agents/flash/charter.md` | claude-sonnet-4.6 | 🟢 Active |
| Smoke | Tester (Happy-Path Smoke) | `.squad/agents/smoke/charter.md` | claude-haiku-4.5 | 🟢 Active |

## Coding Agent

<!-- copilot-auto-assign: false -->

| Name | Role | Charter | Status |
|------|------|---------|--------|
| @copilot | Coding Agent | — | 🤖 Coding Agent |

### Capabilities

**🟢 Good fit — auto-route when enabled:**
- Bug fixes with clear reproduction steps
- Small isolated features with clear specs
- Boilerplate/scaffolding generation

**🟡 Needs review — route to @copilot but flag for squad member PR review:**
- Medium features with clear specs and acceptance criteria

**🔴 Not suitable — route to squad member instead:**
- Architecture decisions and system design
- Ambiguous requirements needing clarification

## Team Philosophy

- **Optimize for:** Speed, working demos, shipping PoCs
- **Not optimized for:** Production readiness, scale, robustness, polish
- **Definition of done:** The app runs and the happy path works end-to-end
- **Spec-kit is mandatory:** No planning before specs, no code before tasks
- **No gold-plating:** If it works, ship it and move to the next build

## Model Strategy

| Role | Model | Why |
|------|-------|-----|
| Rusty (Planner/Specs) | claude-opus-4.8 | Deep reasoning — spec mistakes cost the most |
| Flash (Implementer) | claude-sonnet-4.6 | Strong coding + speed for high-volume work |
| Smoke (Tester) | claude-haiku-4.5 | Fast & cheap for lightweight smoke tests |
| Squad (Coordinator) | claude-haiku-4.5 | Fast & cheap for routing and admin |

## Project Context

- **Project:** squad-sdd-workshop
- **Created:** 2026-08-21
- **Squad type:** PoC Speed Squad
- **First objective:** Interactive Rock-Paper-Scissors CLI app in Python
