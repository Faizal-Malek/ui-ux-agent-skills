---
name: ux-design
description: >-
  Design a screen from a brief using professional, non-AI-looking UI standards
  (dashboards, product UI, landing pages) with explicit mobile 375, tablet 768,
  laptop 1024, and desktop 1440 behavior. Use when asked to design, layout, or
  build a new screen from requirements—avoid purple glow, 3-card features,
  clone KPIs, and generic SaaS templates.
---

# UX Design — design a screen from a brief

Produce implementable UI that passes [UI/UX Standards](../../ui-ux-standards.md). Prefer hierarchy and subject-grounded decisions over templates. Plan all four viewports up front ([responsive-breakpoints.md](../../references/responsive-breakpoints.md)).

## When to use

- New screen from a brief, ticket, or requirements
- Dashboard, **product/list UI**, or **landing/marketing**
- Structural design (IA + layout + tokens)—not only a color tweak

Not for: PR-only critique ([ux-review](../ux-review/SKILL.md)), tell-hunting without design ([ux-audit](../ux-audit/SKILL.md)), “make this less AI” on existing UI ([restyle](../restyle/SKILL.md) / [ux-improve](../ux-improve/SKILL.md)).

## Process (plan → review → build)

Borrowed from Anthropic [`frontend-design`](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md) + brief-read / dials from [`taste-skill`](https://github.com/Leonxlnx/taste-skill):

1. **Design Read (one line, before code)** —  
   `Reading this as: <surface> for <audience>, with a <vibe> language, leaning toward <system or aesthetic>.`  
   Infer from the brief; ask **at most one** clarifying question only if the read truly forks. Do not dump a questionnaire.
2. **Route the surface** — `landing` | `dashboard` | `product` (list/tool).
3. **Set three dials** (defaults unless the read overrides):
   | Dial | Default | Notes |
   | --- | --- | --- |
   | `DESIGN_VARIANCE` | 5–7 | 1 = symmetry · 10 = artsy chaos. Landings lean higher; product/dashboards lower |
   | `MOTION_INTENSITY` | 3–6 | 1 = static · 10 = cinematic. Prefer 2–3 intentional motions |
   | `VISUAL_DENSITY` | landing 3–4 · product/dash 7–9 | 1 = gallery · 10 = cockpit |
4. **Write a compact plan** before code:
   - Color: 4–6 named hex roles (include one `--accent`)
   - Type: 1–2 families with roles (not Inter/Roboto/Arial/system by default)
   - Layout: one-sentence concept + ASCII wireframe; alignment notes
   - **Responsive table** for shell/nav + primary + secondary at 375 / 768 / 1024 / 1440
   - Signature: one memorable element; everything else quiet
   - Craft defaults: focus rings, ≥16px body, touch targets, empty/loading/error
5. **Self-review the plan** — would you produce this for *any* similar brief? If yes, revise. Reject first-order *and* second-order AI clusters (including taste-skill’s cream+brass “premium consumer” default when unearned).
6. **Build** to the plan; critique once (screenshots if available) at four widths.

**Companion:** for marketing/portfolio landings with heavy art direction, also invoke installed `design-taste-frontend` (Taste Skill). Keep **this** skill for dashboards/product + de-AI standards.

## Hard rules by surface

### All surfaces
- One intentional accent; neutrals carry the UI.
- No purple/indigo AI default, glass/glow/grid decoration, or gradient-headline kit unless briefed.
- Don’t land in a second-order “tasteful AI” cluster.
- Copy is specific outcomes, not “supercharge / streamline / seamlessly.”
- Cards only when interaction or understanding needs a container.
- Preserve an existing design system when present.
- Mobile-first; no horizontal scroll; no hover-only primary actions.

### Dashboard
- Apply **Dashboard five fixes** (standards §A): hero metric, varied deltas, solid surfaces, quiet chrome, chart controls.
- Prefer hierarchy over four equal KPI cards.
- KPI grids: 1 col → 2 (tablet) → purposeful denser layout (laptop+), not four equal cards by default.

### Product / list UI (Linear bar)
- Apply **Linear five decisions** (standards §B): **density, borders, one color, keyboard, alignment**.
- Compact rows; 1px separators; muted status colors; show shortcuts where power users live; strict column alignment.
- Tables: horizontal scroll or card rows on mobile—never crushed columns.

### Landing
- Apply **Landing five fixes** (standards §C) + hero budget: brand-first, full-bleed/product visual, one CTA group, no feature-card opening, no overlays.
- Prefer real product UI in the hero over Fast/Secure/Easy cards.
- Primary CTA = solid accent; secondary = text link.
- Hero must still read as one composition at 375 (stack), not a shrunk desktop collage.

## Checklist before done

- [ ] Job + surface route stated
- [ ] Plan reviewed against AI clusters
- [ ] Correct five-tell map cleared for that surface
- [ ] Product UI: Linear five decisions considered
- [ ] Tokens + type intentional
- [ ] Sample content specific and varied
- [ ] Responsive table for 375 / 768 / 1024 / 1440
- [ ] Craft defaults (focus, contrast, touch, states) considered

## Output expectations

1. **Job** (1 sentence) + **surface**
2. **Plan** (tokens, type, layout, signature, **viewport table**) + what you changed in the default review
3. **Spec or implemented UI**
4. **Sample content**
5. **Standards pass** against the relevant five tells / Linear decisions / craft QA

## What NOT to do

- Don’t start from 4 KPI cards or 3 feature cards.
- Don’t use glow grids, glass search, or gradient CTAs as defaults.
- Don’t write a design essay—ship a buildable layout.
- Don’t invent a parallel theme when a design system exists.
- Don’t design only “mobile + desktop” and skip tablet/laptop.

## Sources adapted

- https://github.com/anthropics/skills — `frontend-design` (plan/review loop, clusters, restraint)
- https://github.com/arham777/ui-ux-kit — surface routing
- https://github.com/elayadesign/redesign-skill — copy bans, one-accent, anti–3-column features
- https://github.com/kylezantos/responsive-craft — viewport planning
- https://github.com/nextlevelbuilder/ui-ux-pro-max-skill — craft defaults
- Local Design Motion refs — dashboard/landing five maps; Linear five decisions
