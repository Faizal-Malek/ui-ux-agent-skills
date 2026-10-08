# Responsive breakpoints — four viewports

Canonical widths for design, audit, restyle, and improve. Always cover **all four** unless the surface is explicitly mobile-only or desktop-only.

| Viewport | Width | Typical role |
| --- | --- | --- |
| **Mobile** | `375px` | Single column; thumb reach; touch targets; bottom/sheet nav |
| **Tablet** | `768px` | 1→2 columns; denser toolbars; side panels start appearing |
| **Laptop** | `1024px` | App chrome (sidebar + main); multi-column product UI |
| **Desktop** | `1440px` | Full hierarchy; max content width; no sparse “empty luxury” |

Also drag-test between breakpoints (≈280→2560). Named widths catch cliffs; drag catches in-betweens.

## Required behavior notes (every screen)

Before coding or after auditing, state in one table:

| Region | Mobile 375 | Tablet 768 | Laptop 1024 | Desktop 1440 |
| --- | --- | --- | --- | --- |
| Shell / nav | … | … | … | … |
| Primary content | … | … | … | … |
| Secondary / aside | … | … | … | … |

## Escalation model

1. **Intrinsic** — `flex-wrap`, `auto-fit`/`minmax`, `clamp()`, `min-w-0`
2. **Container queries** — component adapts to *its* box (cards, widgets)
3. **Media queries** — page-level only (nav transform, sidebar visibility, column count)

Prefer mobile-first `min-width` queries. Prefer `svh`/`dvh` over bare `100vh`.

## AI responsive failure patterns (must scan)

Borrowed from [`responsive-craft`](https://github.com/kylezantos/responsive-craft):

1. `100vh` full-screen heroes → use `svh`/`dvh` (+ `vh` fallback)
2. Desktop-first `max-width` cascades → mobile-first `min-width`
3. Missing `min-width: 0` on flex children → overflow on long text
4. `overflow: hidden` on ancestors killing `position: sticky`
5. Hover-only critical actions → provide tap/click equivalents
6. Fixed px widths / grids that don’t reflow → fluid + structural breakpoints
7. Tables/tabs without horizontal scroll or card collapse on narrow
8. Inputs `<16px` on iOS zooming the page → `16px` body/inputs on mobile
9. Touch targets under ~44×44 CSS px with no spacing
10. Disabling pinch-zoom / wrong viewport meta

## Pass criteria

- No horizontal scroll at 375 / 768 / 1024 / 1440
- Nav usable on mobile (menu/sheet); desktop nav not shrunk into unreadability
- Hierarchy still clear (one primary focus) at every width
- Touch: primary actions reachable; no hover-only gates on mobile
