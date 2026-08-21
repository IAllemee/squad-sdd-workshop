# Work Routing

How to decide who handles what.

## Routing Table

| Work Type | Route To | Examples |
|-----------|----------|----------|
| Spec-kit workflow | Rusty | Constitution, specify, plan, tasks, clarify |
| Implementation | Flash | Write Python code, build CLI, wire up logic |
| Testing | Smoke | Run the app, check happy path, pass/fail |
| Code review | Flash or Smoke | Quick review — Flash for code, Smoke for "does it run" |
| Scope & priorities | Rusty | What to build, what to cut, trade-offs |
| Session logging | Scribe | Automatic — never needs routing |
| RAI review | Rai | Content safety, bias checks, credential detection, ethical review |

## Workflow Sequence (MANDATORY)

```
Rusty: /speckit-constitution
  → Rusty: /speckit-specify
    → Rusty: /speckit-plan
      → Rusty: /speckit-tasks
        → Flash: /speckit-implement
          → Smoke: happy-path smoke test
```

**Hard rules:**
1. No planning before specs exist (Rusty must finish specify before plan)
2. No code before tasks exist (Flash waits for Rusty's tasks output)
3. No testing before code exists (Smoke waits for Flash)
4. Skip `/speckit-analyze` always — speed over consistency analysis
5. Use `/speckit-clarify` only when a spec is genuinely ambiguous

## Issue Routing

| Label | Action | Who |
|-------|--------|-----|
| `squad` | Triage: analyze issue, assign `squad:{member}` label | Rusty (Lead) |
| `squad:rusty` | Spec-kit workflow, planning | Rusty |
| `squad:flash` | Implementation | Flash |
| `squad:smoke` | Testing / validation | Smoke |

## Rules

1. **Spec-kit is the conveyor belt** — Rusty drives it start to finish, others follow the artifacts.
2. **Scribe always runs** after substantial work, always as `mode: "background"`. Never blocks.
3. **Quick facts → coordinator answers directly.** Don't spawn an agent for "what port does the server run on?"
4. **No gold-plating.** If the happy path works, it ships.
5. **Speed over polish.** Every decision defaults to the faster option.
6. **Definition of done:** The app runs and the happy path works end-to-end.
