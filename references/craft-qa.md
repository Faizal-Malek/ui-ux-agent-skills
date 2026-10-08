# Craft QA checklist (beyond de-AI tells)

Condensed from [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) priority categories and [`mblode/agent-skills` ui-design](https://github.com/mblode/agent-skills) rules. Use during audit / improve / review when the UI is not “AI-looking” but still weak.

Priority order (fix P0 craft before polish):

| # | Category | Must have | Avoid |
| --- | --- | --- | --- |
| 1 | **Accessibility** | Contrast ≥4.5:1 body; visible focus; labels/`for`; icon-only names; heading order; `prefers-reduced-motion` | Removed focus rings; color-only status; skip-level headings |
| 2 | **Touch & interaction** | ~44×44 targets (web: don’t go tiny); ≥8px gaps; loading feedback | Hover-only primary actions; 0ms state with no feedback |
| 3 | **Layout & responsive** | Four viewports ([responsive-breakpoints.md](responsive-breakpoints.md)); no horizontal scroll; viewport meta | Fixed 1200px shells; `100vh` traps; clipped sticky |
| 4 | **Forms & feedback** | Visible labels; inline errors near fields; empty/error/loading states | Placeholder-as-label; errors only at page top |
| 5 | **Typography & color** | Base ≥16px body; line-height ~1.5; tokenized colors | Gray-on-gray; raw hex scatter; `<12px` body |
| 6 | **Navigation** | Predictable back; clear current location; mobile nav pattern | Broken history; overloaded top chrome |
| 7 | **Motion** | 2–3 intentional motions; meaning > decoration | Bounce everywhere; animate width/height; ignore reduced-motion |
| 8 | **Charts & data** | Legend/tooltip; not color-alone; honest scales | Clone KPI deltas; rainbow series with no labels |
| 9 | **Performance UX** | Reserve image space; lazy non-LCP media | Layout jump / CLS from late images |

## Finding format

`Sev · Category · Evidence (file:line or region) · Why it hurts · Fix`

Severity: **P0** blocks use/trust · **P1** clear quality miss · **P2** polish.
