---
name: ux-improve
description: >-
  Autonomously improve existing UI with minimal prompting: find AI tells and
  craft/responsive issues, apply fixes, then report what changed and why across
  mobile (375), tablet (768), laptop (1024), and desktop (1440). Use for “fix
  this UI”, “make it better”, “improve the layout”, “it looks AI”, or when the
  user does not want to spell out every visual change.
---

# UX Improve — find, fix, explain (all viewports)

Default skill when the user wants **better UI without a long brief**. You already know what to look for: [UI/UX Standards](../../ui-ux-standards.md), [craft QA](../../references/craft-qa.md), [responsive breakpoints](../../references/responsive-breakpoints.md).

Do **not** ask the user to list every color, card, or breakpoint issue one-by-one. Infer the product job from the code/screen, then act.

## When to use

- “Fix / improve / clean up this UI”
- “Make it less AI” **and** actually change the code
- “Check mobile and desktop” / “make it responsive”
- Vague visual dissatisfaction with an existing screen

Prefer [ux-audit](../ux-audit/SKILL.md) for detect-only. Prefer [ux-design](../ux-design/SKILL.md) for greenfield. Prefer [ux-review](../ux-review/SKILL.md) for PR comments only. Prefer [restyle](../restyle/SKILL.md) when the ask is explicitly “de-AI / restyle” with a strong visual rewrite focus—**ux-improve** still covers de-AI but also craft + responsive.

## Default stance

1. **Autonomous** — invent the checklist; don’t wait for a pixel brief.
2. **Fix by default** — unless user says “audit only”.
3. **Four viewports always** — Mobile 375 · Tablet 768 · Laptop 1024 · Desktop 1440.
4. **Explain every change** — what / why / which viewport(s).
5. **Preserve product job** — no feature invention; keep design system if present.

## Process

### 1. Orient (silent, short)

- Surface: `landing` | `dashboard` | `product`
- Job in one sentence (from copy/routes/components)
- Stack cues from the repo (CSS/Tailwind/etc.)

### 2. Scan (no user Q&A unless blocked)

Walk in order:

1. De-AI five tells + Linear decisions + shared bans (standards)
2. Craft QA priorities ([craft-qa.md](../../references/craft-qa.md))
3. Responsive failure patterns ([responsive-breakpoints.md](../../references/responsive-breakpoints.md))

Rank P0 → P2. Cap implementation to high-impact items unless user asks for exhaustive polish.

### 3. Fix

Apply changes in risk order (from [restyle](../restyle/SKILL.md) priority): type → color/surfaces → hierarchy → data/copy honesty → density/borders/alignment → states → motion → responsive reflow.

Hard rules: one accent; no purple/glow/grid defaults; no second-order tasteful-AI swaps; no hover-only primary actions on mobile; no horizontal scroll at the four widths.

### 4. Verify

Mentally (or via preview/screenshots if available) check all four viewports. Re-scan for leftover P0 tells.

### 5. Report (required)

```markdown
# UX improve: <screen>

## Job + surface
<one sentence> · landing|dashboard|product

## What I changed
| Change | Why | Viewports |
| --- | --- | --- |
| … | … | 375 / 768 / 1024 / 1440 |

## Viewport notes
| Viewport | Before risk | After |
| --- | --- | --- |
| Mobile 375 | … | … |
| Tablet 768 | … | … |
| Laptop 1024 | … | … |
| Desktop 1440 | … | … |

## Left for later
P1/P2 not fixed (if any) — one line each

## Verdict
Ship-ready for visual QA? Yes / with follow-ups
```

## What NOT to do

- Don’t interview the user for a full design brief when the UI already exists.
- Don’t only recolor and call it done.
- Don’t skip tablet/laptop because “mobile + desktop is enough.”
- Don’t expand scope into new product features.
- Don’t paste a giant essay—table of changes + why is enough.

## Sources adapted

- Local standards — de-AI five maps + Linear decisions
- https://github.com/nextlevelbuilder/ui-ux-pro-max-skill — craft priority categories (a11y, touch, forms, responsive)
- https://github.com/kylezantos/responsive-craft — four-width discipline + AI responsive failure patterns
- https://github.com/mblode/agent-skills — audit→fix→ship-verdict autonomy
