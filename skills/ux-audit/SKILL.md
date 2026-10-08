---
name: ux-audit
description: >-
  Find every AI tell in an existing UI (dashboard, product, or landing). Use for
  “does this look AI-made?”, pre-restyle inventories, and design QA—maps findings
  to dashboard/landing five-tell lists and Linear expensive-UI decisions.
---

# UX Audit — find every AI tell

Scan an existing screen (code, screenshot, or live UI) against [UI/UX Standards](../../ui-ux-standards.md). List every violation with severity, evidence, and a one-line fix direction.

## When to use

- “Does this look AI-made?” / design QA
- Pre-restyle inventory
- Whole-screen review (not PR-scoped—use [ux-review](../ux-review/SKILL.md) for diffs)

Detect-only by default (no edits). Hand off to [restyle](../restyle/SKILL.md) when the user wants fixes. Mode split borrowed from [`avoid-ai-design`](https://github.com/funboy322/avoid-ai-design) (`detect` vs `rewrite`).

## Hard rules

1. Map findings to **explicit tells** (dashboard §A, landing §C, Linear §B, shared bans)—no vibe-only scores.
2. Cite **evidence** (file/class/region). Tag confidence: **code-certain** | **rendered** | **inferred** (from avoid-ai-design).
3. Severity: **P0** layperson spots AI · **P1** designer spots template · **P2** craft gaps.
4. Run a **silhouette/sameness test** when a screenshot exists: could this be any other SaaS page?
5. Flag **second-order** clusters (cream+terracotta, acid-green-on-black, etc.), not only purple.
6. Cover copy clichés (“supercharge,” “streamline,” “elevate”) and 3-equal feature cards.
7. If a design system forces a pattern, note it—still flag optional AI tells.

## Process

1. Identify surface: `landing` | `dashboard` | `product`.
2. Walk the matching tell tables below + shared bans.
3. For product/list UIs, score Linear’s five decisions.
4. Rank P0→P2; group duplicates.
5. Emit the report format.

## Checklists

### Dashboard five tells
| # | Look for |
| --- | --- |
| 1 | Purple/indigo premium accent overload |
| 2 | Glass search, chart glow, decorative blur |
| 3 | Identical KPI deltas |
| 4 | Equal 4-card → chart → table template |
| 5 | Loud chrome / emoji welcome / flat hierarchy |

### Landing five tells
| # | Look for |
| --- | --- |
| 1 | Glow blooms + tech grid + light beams |
| 2 | Gradient headlines / gradient CTAs / sticker badges |
| 3 | Vague AI marketing copy |
| 4 | Three equal Fast/Secure/Easy (or similar) cards |
| 5 | Fake logo strips; dual equal CTAs; weak brand |

### Linear expensive (product UI)
| Decision | Fail if… |
| --- | --- |
| Density | Huge empty padding; sparse rows for a tool UI |
| Borders | Thick cards/glows instead of hairline structure |
| One color | Rainbow neon tags; many competing accents |
| Keyboard | No shortcuts/focus model on a power tool |
| Alignment | Columns/baselines drift |

### Shared / second-order
- Inter/Roboto/Arial as unearned default; ALL-CAPS eyebrows; decorative `01/02/03`
- Cream+terracotta or acid-green-on-black as unearned “tasteful” swap
- Low contrast; missing focus/empty/error states (note as P1/P2 craft)

## Output expectations

```markdown
# UX audit: <screen>

## Verdict
Pass | Fail — <one line>
Surface: landing | dashboard | product

## Findings
| Sev | Tell / decision | Evidence | Confidence | Fix direction |
| --- | --- | --- | --- | --- |
| P0 | Landing #1 | ... | rendered | ... |

## Counts
P0: N · P1: N · P2: N

## Next step
Recommend `restyle` | targeted fixes | no action
```

## What NOT to do

- Don’t restyle unless asked.
- Don’t ignore landing or Linear checks when the surface matches.
- Don’t accuse authorship—“default left untouched,” not “a model made this” ([avoid-ai-design](https://github.com/funboy322/avoid-ai-design)).

## Sources adapted

- https://github.com/funboy322/avoid-ai-design — detect mode, severity, confidence tags, silhouette test
- https://github.com/narenkatakam/ux-audit — guide/review split, task-first / hierarchy principles
- https://github.com/marten-osieka/de-ai-ui — tells-catalog + self-audit report mindset
- https://github.com/elayadesign/redesign-skill — copy/layout tell inventory
- Local Design Motion refs — five-tell maps + Linear decisions
