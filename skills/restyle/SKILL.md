---
name: restyle
description: >-
  Kill the AI look and restyle an existing dashboard, product UI, or landing
  page. Use when UI looks generic/AI-made (purple glow, grid atmosphere, clone
  KPIs, 3 feature cards, vague copy) and needs concrete visual/structural fixes.
---

# Restyle — kill the AI look

Restyle an existing screen to [UI/UX Standards](../../ui-ux-standards.md)—same product job, professional execution. “Five tells, gone.”

## When to use

- “Make this less AI” / “de-AI this page”
- After [ux-audit](../ux-audit/SKILL.md) finds P0/P1 tells
- Matches before refs: [dashboard](../../media/de-ai-ui-before.jpg), [landing](../../media/de-ai-landing-before-lumen.jpg)

Not for greenfield ([ux-design](../ux-design/SKILL.md)) or PR-only comments ([ux-review](../ux-review/SKILL.md)).

## Modes

- **Full restyle** (default): audit → direction → edit → re-check.
- **Surgical**: inside a design system or small component—swap tells, keep structure/tokens.

Borrowed from [`avoid-ai-design`](https://github.com/funboy322/avoid-ai-design) rewrite calibration and [`redesign-skill`](https://github.com/elayadesign/redesign-skill) diagnose-then-fix.

## Hard rules

1. Clear **all** relevant five tells (dashboard and/or landing). Leaving any P0 tell = failed restyle.
2. For product/list UIs, apply **Linear five decisions** (density, borders, one color, keyboard, alignment). Refs: [part1](../../media/linear-expensive-part1.jpg), [part2](../../media/linear-expensive-part2.jpg).
3. **Keep the product job** — don’t invent unrelated features.
4. Prefer token/CSS + layout changes over rewriting business logic.
5. **Don’t trade clichés** — purple→cream+terracotta or purple→acid-green neon is still a fail unless briefed.
6. One intentional accent; solid surfaces; hairline borders; quiet chrome.
7. Landing: outcome copy, product-first proof, solid primary CTA, quiet secondary link; kill glow/grid/3-cards.
8. Preserve functionality, a11y, and meaning of copy (sharpen generics; don’t invent claims).
9. If a design system exists, restyle **into** it.

## Fix maps

### Dashboard five fixes
| Fix | Actions |
| --- | --- |
| Intentional accent | One `--accent`; recolor CTA/meaningful deltas/chart series; strip purple defaults |
| Solid surfaces | Remove glass/glow; opaque `--surface` + `--border` |
| Honest metrics | Unique deltas/periods; no cloned pills |
| Hierarchy by job | Hero metric + supporting stack; chart range controls |
| Quiet chrome | Neutral top bar; one accent CTA; demote greetings |

### Landing five fixes
| Fix | Actions |
| --- | --- |
| Flat field | Kill grid/glow/beams; use product imagery/UI |
| Type + CTA | Crisp headline; solid accent button; text-link secondary |
| Outcome copy | Specific job/result; ban supercharge/streamline/seamlessly |
| Product proof | Real dense UI / testimonial; no Fast/Secure/Easy opener |
| Credible chrome | Real proof; one primary CTA; brand-first |

### Linear decisions (product)
Tighten density → hairline borders → one accent + muted statuses → surface shortcuts → lock column alignment.

## Fix priority (max impact, min risk)

Adapted from [`redesign-skill`](https://github.com/elayadesign/redesign-skill):

1. Font / type hierarchy  
2. Color & surface cleanup (palette, kill gradients/glow)  
3. Hierarchy / layout (hero metric or hero budget)  
4. Data & copy honesty  
5. Borders, density, alignment (product)  
6. States (hover/focus/empty/error)  
7. Motion restraint  

## Process

1. Snapshot tells (or run audit) by surface.
2. Lock tokens (bg/surface/border/text/muted/accent) + type if free.
3. Restructure hierarchy; strip effects; fix content.
4. Product pass: Linear five.
5. Landing pass: hero budget + brand test.
6. Re-audit; success = tells gone **and** coherent subject-grounded direction (not a token-swap)—from avoid-ai-design success tests.
7. Compare spirit to after refs: [dashboard after](../../media/de-ai-ui-after.jpg), [landing after](../../media/de-ai-landing-after-lumen.jpg)—principles, not pixel clone.

## Checklist before done

- [ ] Relevant five tells removed
- [ ] No second-order default swap
- [ ] Linear decisions applied if product UI
- [ ] Accent sparingly; no glass/glow/grid
- [ ] Clear primary focus; quiet chrome
- [ ] Varied credible data; specific copy
- [ ] Design system preserved when present
- [ ] Responsive hierarchy holds

## Output expectations

1. **Before → after tell map** (per relevant five + Linear if any)
2. **Token diff**
3. **Structural changes**
4. **Code changes** (or patch plan)
5. **Re-audit verdict** + residual risks

## What NOT to do

- Don’t only recolor purple to teal and keep clone KPIs / 3 feature cards.
- Don’t add more cards, badges, or stat strips.
- Don’t pixel-clone reference mint/teal demos unless asked—match principles.
- Don’t expand into unrelated product features.
- Don’t break working behavior for aesthetics.

## Sources adapted

- https://github.com/funboy322/avoid-ai-design — rewrite workflow, anti–second-order swap, success tests
- https://github.com/elayadesign/redesign-skill — diagnose-then-fix, fix priority, copy/layout bans
- https://github.com/marten-osieka/de-ai-ui — prevent-then-self-audit
- https://github.com/AntonioSpagnol/UI-Deslopify-Skill — restyle-as-replace-slop framing (structure only; we don’t require 21st.dev)
- Local Design Motion refs — dashboard/landing after targets; Linear expensive decisions
