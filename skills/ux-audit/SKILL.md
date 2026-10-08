---
name: ux-audit
description: >-
  Find every AI tell and craft/responsive issue in an existing UI (dashboard,
  product, or landing) across mobile 375, tablet 768, laptop 1024, and desktop
  1440. Use for “does this look AI-made?”, design QA, and pre-fix inventories—
  detect-only unless asked to fix (then hand off to ux-improve or restyle).
---

# UX Audit — find every AI tell (+ craft + responsive)

Scan an existing screen (code, screenshot, or live UI) against [UI/UX Standards](../../ui-ux-standards.md), [craft QA](../../references/craft-qa.md), and [responsive breakpoints](../../references/responsive-breakpoints.md). List every violation with severity, evidence, and a one-line fix direction.

## When to use

- “Does this look AI-made?” / design QA / “what’s wrong with this UI?”
- Pre-restyle / pre-improve inventory
- Whole-screen review (not PR-scoped—use [ux-review](../ux-review/SKILL.md) for diffs)

**Detect-only by default** (no edits). When the user wants fixes, hand off to [ux-improve](../ux-improve/SKILL.md) (default) or [restyle](../restyle/SKILL.md) (de-AI rewrite focus). Mode split borrowed from [`avoid-ai-design`](https://github.com/funboy322/avoid-ai-design) (`detect` vs `rewrite`).

## Hard rules

1. Map findings to **explicit tells** (dashboard §A, landing §C, Linear §B, shared bans)—no vibe-only scores.
2. Also run **craft QA** and **four-viewport** checks—not only purple/glow.
3. Cite **evidence** (file/class/region). Tag confidence: **code-certain** | **rendered** | **inferred**.
4. Severity: **P0** layperson spots AI or blocked use · **P1** designer/template or clear craft miss · **P2** polish.
5. Run a **silhouette/sameness test** when a screenshot exists: could this be any other SaaS page?
6. Flag **second-order** clusters (cream+terracotta, acid-green-on-black, etc.), not only purple.
7. Cover copy clichés and 3-equal feature cards.
8. If a design system forces a pattern, note it—still flag optional AI tells.

## Process

1. Identify surface: `landing` | `dashboard` | `product`.
2. Walk tell tables + shared bans.
3. Walk craft QA priorities (a11y → touch → responsive → forms…).
4. Score Linear’s five decisions for product/list UIs.
5. Check **375 / 768 / 1024 / 1440** (or note missing evidence).
6. Rank P0→P2; group duplicates.
7. Emit the report format.

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

### Responsive (all surfaces)
| Width | Fail if… |
| --- | --- |
| 375 | Horizontal scroll; no mobile nav; hover-only primary; tiny tap targets |
| 768 | Awkward half-collapsed grids; unusable side panels |
| 1024 | App shell broken; competing columns without hierarchy |
| 1440 | Content stretches unreadably; empty “luxury” padding theater |

Scan AI responsive failures in [responsive-breakpoints.md](../../references/responsive-breakpoints.md).

### Shared / second-order / craft
- Inter/Roboto/Arial as unearned default; ALL-CAPS eyebrows; decorative `01/02/03`
- Cream+terracotta or acid-green-on-black as unearned “tasteful” swap
- Low contrast; missing focus/empty/error states; placeholder-only labels

## Output expectations

```markdown
# UX audit: <screen>

## Verdict
Pass | Fail — <one line>
Surface: landing | dashboard | product

## Findings
| Sev | Tell / craft / viewport | Evidence | Confidence | Fix direction |
| --- | --- | --- | --- | --- |
| P0 | Landing #1 | ... | rendered | ... |
| P0 | Responsive 375 | ... | code-certain | ... |

## Counts
P0: N · P1: N · P2: N

## Viewport coverage
375 | 768 | 1024 | 1440 — checked / inferred / unknown

## Next step
Recommend `ux-improve` | `restyle` | targeted fixes | no action
```

## What NOT to do

- Don’t restyle unless asked (use `ux-improve` / `restyle`).
- Don’t ignore landing, Linear, craft, or viewport checks when they apply.
- Don’t accuse authorship—“default left untouched,” not “a model made this”.

## Sources adapted

- https://github.com/funboy322/avoid-ai-design — detect mode, severity, confidence tags, silhouette test
- https://github.com/narenkatakam/ux-audit — guide/review split, task-first / hierarchy principles
- https://github.com/marten-osieka/de-ai-ui — tells-catalog + self-audit report mindset
- https://github.com/nextlevelbuilder/ui-ux-pro-max-skill — craft priority categories
- https://github.com/kylezantos/responsive-craft — four-width + failure patterns
- Local Design Motion refs — five-tell maps + Linear decisions
