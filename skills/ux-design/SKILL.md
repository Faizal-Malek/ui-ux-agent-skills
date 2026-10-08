---
name: ux-design
description: >-
  Design a screen from a brief using professional, non-AI-looking UI standards
  (dashboards, product UI, landing pages). Use when asked to design, layout, or
  build a new screen from requirements—avoid purple glow, 3-card features,
  clone KPIs, and generic SaaS templates.
---

# UX Design — design a screen from a brief

Produce implementable UI that passes [UI/UX Standards](../../ui-ux-standards.md). Prefer hierarchy and subject-grounded decisions over templates.

## When to use

- New screen from a brief, ticket, or requirements
- Dashboard, **product/list UI**, or **landing/marketing**
- Structural design (IA + layout + tokens)—not only a color tweak

Not for: PR-only critique ([ux-review](../ux-review/SKILL.md)), tell-hunting without design ([ux-audit](../ux-audit/SKILL.md)), or “make this less AI” on existing UI ([restyle](../restyle/SKILL.md)).

## Process (plan → review → build)

Borrowed from Anthropic [`frontend-design`](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md):

1. **Ground in the subject** — product, audience, primary job (one sentence).
2. **Route the surface** — `landing` | `dashboard` | `product` (list/tool). Borrowed from [`ui-ux-kit`](https://github.com/arham777/ui-ux-kit) routing.
3. **Write a compact plan** before code:
   - Color: 4–6 named hex roles (include one `--accent`)
   - Type: 1–2 families with roles (not Inter/Roboto/Arial/system by default)
   - Layout: one-sentence concept + ASCII wireframe; alignment notes
   - Signature: one memorable element; everything else quiet
4. **Self-review the plan** — would you produce this for *any* similar brief? If yes, revise. Reject first-order *and* second-order AI clusters (cream+terracotta, acid-green-on-black, SaaS-card kit, etc.).
5. **Build** to the plan; critique once (screenshots if available).

## Hard rules by surface

### All surfaces
- One intentional accent; neutrals carry the UI.
- No purple/indigo AI default, glass/glow/grid decoration, or gradient-headline kit unless briefed.
- Don’t land in a second-order “tasteful AI” cluster.
- Copy is specific outcomes, not “supercharge / streamline / seamlessly.”
- Cards only when interaction or understanding needs a container.
- Preserve an existing design system when present.

### Dashboard
- Apply **Dashboard five fixes** (standards §A): hero metric, varied deltas, solid surfaces, quiet chrome, chart controls.
- Prefer hierarchy over four equal KPI cards.

### Product / list UI (Linear bar)
- Apply **Linear five decisions** (standards §B): **density, borders, one color, keyboard, alignment**.
- Compact rows; 1px separators; muted status colors; show shortcuts where power users live; strict column alignment.

### Landing
- Apply **Landing five fixes** (standards §C) + hero budget: brand-first, full-bleed/product visual, one CTA group, no feature-card opening, no overlays.
- Prefer real product UI in the hero over Fast/Secure/Easy cards.
- Primary CTA = solid accent; secondary = text link.

## Checklist before done

- [ ] Job + surface route stated
- [ ] Plan reviewed against AI clusters
- [ ] Correct five-tell map cleared for that surface
- [ ] Product UI: Linear five decisions considered
- [ ] Tokens + type intentional
- [ ] Sample content specific and varied
- [ ] Mobile + desktop hierarchy holds

## Output expectations

1. **Job** (1 sentence) + **surface**
2. **Plan** (tokens, type, layout, signature) + what you changed in the default review
3. **Spec or implemented UI**
4. **Sample content**
5. **Standards pass** against the relevant five tells / Linear decisions

## What NOT to do

- Don’t start from 4 KPI cards or 3 feature cards.
- Don’t use glow grids, glass search, or gradient CTAs as defaults.
- Don’t write a design essay—ship a buildable layout.
- Don’t invent a parallel theme when a design system exists.

## Sources adapted

- https://github.com/anthropics/skills — `frontend-design` (plan/review loop, clusters, restraint)
- https://github.com/arham777/ui-ux-kit — surface routing
- https://github.com/elayadesign/redesign-skill — copy bans, one-accent, anti–3-column features
- Local Design Motion refs — dashboard/landing five maps; Linear five decisions
