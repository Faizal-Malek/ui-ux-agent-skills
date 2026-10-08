# UI/UX Standards — De-AI Your UI

Durable design rules for coding agents shipping **dashboards**, **product UI**, and **landing/marketing** surfaces. Goal: professional interfaces—not generic AI templates.

**Skills:** [ux-improve](skills/ux-improve/SKILL.md) · [ux-design](skills/ux-design/SKILL.md) · [ux-audit](skills/ux-audit/SKILL.md) · [ux-review](skills/ux-review/SKILL.md) · [restyle](skills/restyle/SKILL.md) · [index](skills-index.md)

---

## Reference media

| Case | Before | After / model |
| --- | --- | --- |
| Dashboard de-AI · 01 | [de-ai-ui-before.jpg](media/de-ai-ui-before.jpg) | [de-ai-ui-after.jpg](media/de-ai-ui-after.jpg) |
| Landing de-AI · 02 (Lumen) | [de-ai-landing-before-lumen.jpg](media/de-ai-landing-before-lumen.jpg) | [de-ai-landing-after-lumen.jpg](media/de-ai-landing-after-lumen.jpg) |
| Linear “expensive” product UI | — | [linear-expensive-part1.jpg](media/linear-expensive-part1.jpg) · [linear-expensive-part2.jpg](media/linear-expensive-part2.jpg) |

---

## A. Dashboard de-AI — five tells → five fixes

From DE-AI YOUR UI · 01 (dashboard before/after).

| # | Tell (ban) | Fix (require) |
| --- | --- | --- |
| **1** | **Purple-on-dark cliché** — saturated purple/indigo/violet as the “premium” accent on near-black; purple headers, charts, buttons everywhere. | **One intentional accent** — brand-specific (mint, teal, coral, amber…), used sparingly for primary actions and meaningful emphasis. Neutrals carry the UI. |
| **2** | **Glassmorphism & glow for show** — frosted/blur search, neon chart glows, multi-layer decorative shadows. | **Solid surfaces, quiet depth** — opaque panels, hairline borders. Depth only when it clarifies layers (menus, modals)—never decoration. |
| **3** | **Clone KPI deltas** — every card shows the same trend pill (e.g. all `+12.5%`). | **Believable, varied data** — distinct deltas, units, periods; secondary metrics don’t mirror the hero. |
| **4** | **Default SaaS card grid** — four equal KPI cards → glowing chart → generic table, regardless of job. | **Hierarchy by job** — one primary metric owns attention; supporting metrics smaller/stacked; charts earn space with controls (7d/30d/90d); tables scan, don’t fill. |
| **5** | **Loud, flat hierarchy** — purple chrome, emoji greetings, Upgrade + search + bell + avatar all screaming. | **Quiet chrome, clear focus** — restrained top bar; one primary CTA; typography/spacing create focus. |

---

## B. Linear-style “expensive” product UI — five decisions

From “Why Linear feels expensive” (reverse-engineered). Apply to issue lists, tables, app shells, dense tools—not marketing fluff.

| Decision | Do this | Avoid |
| --- | --- | --- |
| **1. Density** | Compact row heights; high information per viewport; tight, consistent vertical rhythm. Every pixel earns its keep. | Oversized empty cards, huge padding “for premium,” sparse lists that force endless scroll. |
| **2. Borders** | 1px (or hairline) separators in a slightly lighter/darker neutral; structure without noise. | Heavy dividers, thick cards, glow outlines, stacked shadows as separation. |
| **3. One color** | One primary accent for selection/primary action. Status/tags use **muted, desaturated** semantic colors—not a rainbow carnival. | Multiple neon accents competing; rainbow tags at full saturation; gradient chrome. |
| **4. Keyboard** | Surface shortcuts on actions (`F` Filter, `D` Display, `C` New); design predictable focus order and command palette affordances. | Mouse-only chrome; hidden power; huge touch-only buttons as the only interaction model for pro tools. |
| **5. Alignment** | Strict column grid: IDs, titles, statuses, assignees, dates share vertical axes. Optical alignment, not “approximate.” | Wobbly columns, mixed left edges, icons that don’t share a gutter, baseline drift across rows. |

**Expensive = disciplined**, not decorated. Density + borders + one color + keyboard + alignment beat glass, glow, and KPI theater.

---

## C. Landing-page de-AI — five tells → five fixes

From DE-AI YOUR UI · 02 · LANDING (Lumen before/after).

| # | Tell (ban) | Fix (require) |
| --- | --- | --- |
| **1** | **Glow + grid atmosphere** — cyan tech grid, ungrounded purple/pink neon blooms, decorative light beams. | **Flat dark (or light) field** — atmosphere from real product imagery/UI, not ambient glow soup. Thin borders define sections. |
| **2** | **Gradient headline + gradient CTA kit** — purple→pink `bg-clip-text` titles, matching gradient primary buttons, floating badge stickers on copy. | **High-contrast type + one solid accent CTA** — headline in crisp white/near-black; primary button = solid accent; secondary = quiet text link. |
| **3** | **Generic AI copy** — “Supercharge your workflow with AI,” “all-in-one platform to streamline, automate and scale…” | **Specific outcome copy** — name the job and result (“Close the month in one afternoon. Bookkeeping for small teams, without the spreadsheet.”). |
| **4** | **Three equal feature cards** — Fast / Secure / Easy with stock icons and one-line fluff. | **Product-first proof** — show the real UI (dense, believable widgets) and/or one concrete testimonial next to the claim. Features earn sections later—don’t open with icon-card bingo. |
| **5** | **Fake social proof + template chrome** — pop-culture logo strips, dual equal CTAs, notification dots on headlines. | **Credible proof + quiet chrome** — real-sounding quotes with role/company; one primary CTA; brand name as hero-level signal in nav + composition. |

### Landing composition rules (always)

1. **One composition** in the first viewport—not a widget dashboard.
2. **Brand first** — if you strip the nav and the page could be another product, branding is too weak.
3. **Hero budget** — brand + one headline + one short supporting sentence + one CTA group + one dominant visual (prefer full-bleed product/place). No stats strips, schedules, or promo grids in viewport one.
4. **No hero overlays** — no floating badges, chips, or stickers on media.
5. **Cards only when interactive** — default: no cards in the hero.
6. **One job per later section** — one purpose, one headline, usually one short line.

---

## Shared bans (all surfaces)

### Color & effects
- Purple/violet/indigo as the default “AI premium” accent (dark or light).
- Glassmorphism / frosted blur chrome / chart glow for decoration.
- Multi-layer neon shadows; ungrounded ambient blooms; tech-grid backgrounds as the main idea.
- Gray-on-gray text failing contrast.

### Layout & components
- Equal-weight KPI rows or 3-up Fast/Secure/Easy cards as the automatic opening move.
- Identical trend pills / clone dummy metrics.
- Cards as default containers when border/shadow/radius aren’t needed.
- Stat strips, pill clusters, icon rows, emoji-hero greetings.

### Typography & copy
- Default stacks (Inter, Roboto, Arial, system) when the brief leaves type free—choose on purpose.
- Vague marketing verbs: *supercharge, streamline, seamlessly, elevate, unleash, all-in-one* without a concrete outcome.
- One random accented/gradient word in a headline as decoration.

### Second-order “tasteful AI” clusters (still defaults)

Also ban when the brief didn’t ask for them (see Sources): cream + terracotta + display serif; near-black + acid-green/vermilion as an unearned signature; broadsheet hairline newspaper layout; SaaS-card kit (identical rounded cards + soft grey shadow + gradient washes); ALL-CAPS eyebrows + middle-dot meta + decorative `01/02/03` markers.

**Don’t trade purple slop for a second-order default.** Fix = decisions grounded in the subject—not a different meme.

### Motion
- No scatter fade-up on every section/card. Prefer 2–3 intentional motions; respect `prefers-reduced-motion`.

---

## D. Responsive — four viewports (always)

Unless the surface is explicitly single-viewport, design and verify at:

| Viewport | Width |
| --- | --- |
| Mobile | **375px** |
| Tablet | **768px** |
| Laptop | **1024px** |
| Desktop | **1440px** |

Full protocol + AI failure patterns: [references/responsive-breakpoints.md](references/responsive-breakpoints.md).

**Minimums:** no horizontal scroll; mobile nav (not a shrunk desktop nav); `svh`/`dvh` over bare `100vh`; touch-reachable primary actions; `min-width: 0` on shrinking flex children; tables/tabs that don’t blow the layout.

---

## E. Craft QA (beyond de-AI)

De-AI clears the “template look.” Craft QA clears use/trust issues. Condensed checklist: [references/craft-qa.md](references/craft-qa.md).

Priority: accessibility → touch/interaction → responsive → forms/feedback → type/color → navigation → motion → charts → performance UX.

---

## What “professional” looks like

- **Decision, not decoration** — color, cards, charts, pills exist for a task.
- **Tokenized palette** — `--bg`, `--surface`, `--border`, `--text`, `--muted`, `--accent` (one accent).
- **Hierarchy** — one primary number/action/message per region; supporting content quieter.
- **Credible content** — varied names, dates, amounts, deltas; empty/loading/error states designed.
- **Product UI density** when showing app chrome in marketing—looks like a real tool (Linear-like discipline), not a toy mock.
- **Preserve design systems** when present; apply these rules as anti-slop constraints inside them.

---

## Agent ship gate

- [ ] Dashboard five tells cleared (or N/A)
- [ ] Landing five tells cleared (or N/A)
- [ ] If product/list UI: Linear five decisions considered (density, borders, one color, keyboard, alignment)
- [ ] No purple/indigo AI default; no glass/glow/grid decoration
- [ ] No second-order tasteful-AI cluster unless briefed
- [ ] Copy is specific; sample data is varied
- [ ] Hierarchy holds at **375 / 768 / 1024 / 1440**
- [ ] Craft QA P0s cleared (contrast, focus, touch, forms states) — see [craft-qa.md](references/craft-qa.md)

Fail → [ux-improve](skills/ux-improve/SKILL.md) (fix) · [ux-audit](skills/ux-audit/SKILL.md) (detect) · [restyle](skills/restyle/SKILL.md) (de-AI rewrite).

---

## Sources (published skills we borrowed from)

Patterns integrated into this standards doc and the four skills—not copied wholesale:

| Source | URL | What we borrowed |
| --- | --- | --- |
| Anthropic `frontend-design` | https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md | Plan→review-against-brief→build; second-order AI clusters; subject-grounded direction; restraint (“remove one accessory”); copy as design |
| `avoid-ai-design` | https://github.com/funboy322/avoid-ai-design | Detect vs rewrite modes; P0/P1/P2 severity; silhouette/sameness test; don’t swap one cliché for another; context profiles (landing vs dashboard) |
| `redesign-existing-projects` | https://github.com/elayadesign/redesign-skill | Diagnose-then-fix; ban Inter/Roboto defaults; one accent; no 3-equal feature columns; organic numbers; ban Elevate/Seamless copy; fix-priority order |
| `ui-ux-audit` (narenkatakam) | https://github.com/narenkatakam/ux-audit | Task-first CTA; CRAP hierarchy; guide vs review modes; color systems = semantic tokens + one accent |
| `de-ai-ui` | https://github.com/marten-osieka/de-ai-ui | Tells catalog mindset; self-audit report after generation; prevent 3-card grids / purple gradients / workflow clichés |
| `ui-ux-kit` | https://github.com/arham777/ui-ux-kit | Route by surface (landing/dashboard/product); countable anti-slop gate; persist a design-system memo across pages |
| `impeccable` | https://github.com/pbakaus/impeccable | Command-split critique/audit/polish; broad surface coverage for when to invoke design skills |
| `ui-ux-pro-max` | https://github.com/nextlevelbuilder/ui-ux-pro-max-skill | Craft priority ladder (a11y→touch→responsive→forms…); we keep checklists, not the Python search DB |
| `responsive-craft` | https://github.com/kylezantos/responsive-craft | Four-width discipline + AI responsive failure patterns |
| `ui-design` (mblode) | https://github.com/mblode/agent-skills | Autonomous audit→fix→ship-verdict posture |
| Design Motion references | Local media (DE-AI · 01/02, Linear expensive) | Concrete five-tell maps and Linear’s five decisions |

---

## Related skills

| Skill | Use when |
| --- | --- |
| [ux-improve](skills/ux-improve/SKILL.md) | **Default:** fix existing UI with low prompting; explain changes across 4 viewports |
| [ux-design](skills/ux-design/SKILL.md) | Design a screen from a brief |
| [ux-audit](skills/ux-audit/SKILL.md) | Detect-only inventory (AI tells + craft + responsive) |
| [ux-review](skills/ux-review/SKILL.md) | Review UI in a PR/diff |
| [restyle](skills/restyle/SKILL.md) | Kill the AI look / restyle an existing screen |
