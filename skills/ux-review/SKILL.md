---
name: ux-review
description: >-
  Review UI changes in a PR or diff against de-AI UI standards (dashboard,
  landing, and Linear-style product UI). Use when reviewing pull requests or
  staged frontend for AI tells, hierarchy regressions, and copy/layout clichés.
---

# UX Review — review the UI of a PR

Review **changed UI** in a PR/diff. Block merge-quality issues that reintroduce AI-looking patterns. Align with [UI/UX Standards](../../ui-ux-standards.md).

## When to use

- PR / code review / “check this diff for UI quality”
- Agent-authored frontend before merge

Prefer [ux-audit](../ux-audit/SKILL.md) for whole-screen inventories. Prefer [restyle](../restyle/SKILL.md) to fix in place.

## Hard rules

1. Scope to **changed files and visible impact**. Flag pre-existing issues only if the PR worsens them or blocks understanding.
2. Map every blocker to a **standards tell/ban** (dashboard §A, landing §C, Linear §B, shared bans).
3. Labels: **Blocker** | **Should fix** | **Nit** (aligned with P0 / P1 / P2 from [`avoid-ai-design`](https://github.com/funboy322/avoid-ai-design)).
4. Prefer file:line or component references.
5. Preserve the repo design system; don’t demand a new brand mid-PR unless the PR invents one.
6. Watch for **second-order** cluster swaps (purple→cream+terracotta, purple→acid green) as still-blocked defaults.
7. Landing diffs: enforce hero budget, brand-first, no 3-card openers, specific copy.
8. Product/list diffs: check density, hairline borders, one accent, keyboard affordances, alignment.

## Process

1. List UI surfaces touched (routes, components, CSS/tokens, copy).
2. Diff-read for: accents, `backdrop-filter`/glow, KPI grids, feature cards, gradient text, sample data, hero structure, typography defaults, shortcut UI.
3. Ask: what is loudest **after** this PR?
4. Run the relevant five-tell / Linear gate on post-diff UI.
5. Write comments + summary.

## Block gate

| Block if PR introduces… | Prefer… |
| --- | --- |
| Purple/indigo AI accent or glow/grid atmosphere | Tokenized single accent; flat surfaces |
| Glass chrome / chart glow | Solid surface + hairline border |
| Clone KPIs or equal-weight card grids | Hero metric + varied deltas |
| Landing: gradient headline kit, vague AI copy, 3 feature cards | Outcome headline, product proof, solid CTA |
| Product: loose alignment, rainbow tags, zero keyboard model | Linear five decisions |
| Second-order tasteful-AI cluster unearned | Subject-grounded direction |

## Checklist

- [ ] No new AI palette / glow / glass
- [ ] Hierarchy & data honesty OK (dashboards)
- [ ] Landing hero rules OK if touched
- [ ] Product density/borders/alignment/keyboard OK if touched
- [ ] Copy not generic AI marketing
- [ ] Contrast, focus, reduced-motion not degraded
- [ ] Mobile hierarchy holds

## Output expectations

```markdown
# UI PR review: <PR or branch>

## Summary
Approve | Request changes — <one line>

## Blockers
- `path:line` — Tell <id> — <issue> → <fix>

## Should fix
- ...

## Nits
- ...

## Standards notes
- Dashboard / Landing / Linear: pass|fail|n/a per relevant set
```

## What NOT to do

- Don’t bikeshed unrelated refactors.
- Don’t approve if any P0 tell is newly introduced.
- Don’t demand a full restyle of untouched legacy UI unless asked.
- Don’t write abstract theory—tie comments to code + tells.

## Sources adapted

- https://github.com/funboy322/avoid-ai-design — severity tiers, evidence-not-accusation
- https://github.com/narenkatakam/ux-audit — review-mode checklist mindset
- https://github.com/pbakaus/impeccable — critique/review command framing
- https://github.com/mblode/agent-skills — `ui-design` PR/UX review trigger patterns
- Local Design Motion refs — tell maps + Linear decisions
