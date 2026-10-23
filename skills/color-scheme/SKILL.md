---
name: color-scheme
description: >-
  Define or rebalance a site’s UI color scheme: named roles (bg/surface/text/accent),
  60-30-10 (or similar) ratios, imagery↔palette harmony, and one intentional accent
  that makes a page “pop.” Use when improving muddy/flat palettes, extracting colors
  from a hero photo, assigning token roles, or deciding where accent belongs
  (focal keyword, CTA, small icon)—not for full restyle, SEO, or layout redesign.
---

# Color Scheme — roles, balance, and pop

Own **color roles & balance** only. For full de-AI restyle use [restyle](../restyle/SKILL.md); for landings with heavy art direction also invoke Taste (`design-taste-frontend`); for craft/responsive beyond color use [ux-improve](../ux-improve/SKILL.md). Standards: [ui-ux-standards.md](../../ui-ux-standards.md). Ratio deep-dive: [color-balance.md](../../references/color-balance.md).

Pack: [ui-ux-agent-skills](https://github.com/Faizal-Malek/ui-ux-agent-skills).

## When to use

- “Make this palette pop” / “rebalance these colors” / “pull colors from the hero”
- Muddy, flat, or rainbow UI; unclear bg vs text vs accent
- Need a token table + placement map before CSS changes
- After [ux-audit](../ux-audit/SKILL.md) flags purple defaults or weak hierarchy by color

**Not for:** full visual rewrite ([restyle](../restyle/SKILL.md)), greenfield screen design ([ux-design](../ux-design/SKILL.md)), PR-only comments ([ux-review](../ux-review/SKILL.md)), SEO.

## Teaching refs (before → after)

| System | Before | After | Lesson |
| --- | --- | --- | --- |
| **Sage · Walnut · Amber** | [before](../../media/color-scheme/sage-walnut-before.jpg) | [after](../../media/color-scheme/sage-walnut-amber-after.jpg) | Nature interiors: Sage `#87A96B` + Walnut `#5A3E2B` from hero; **Amber Glow `#D5851F`** only on the keyword *alive* (and tiny chrome if needed). Cream field carries the page. |
| **Jet · Amethyst · Cyan** | [before](../../media/color-scheme/jet-amethyst-before.jpg) | [after](../../media/color-scheme/jet-amethyst-cyan-after.jpg) | Dark luxury: Jet `#050505` canvas + Royal Amethyst `#3B0A6B` in imagery/mood; **Electric Cyan `#00E5FF`** as sparkle on focal edges—not large fills. |
| **Charcoal · Silver · Red** | [before](../../media/color-scheme/charcoal-silver-before.jpg) | [after](../../media/color-scheme/charcoal-silver-red-after.jpg) | Neutrals first: Charcoal `#2A2A2A` + Moonlit Silver `#C0C0C0`; **Signal Red `#E10600`** on *brighter* + one accent plane tied to the hero—still ~10%, not red chrome. |

Shared craft across all three: **serif headline + quiet sans chrome**; neutrals do the work; accent is the punchline.

## Hard rules

1. **One intentional accent** — a single hue for focus. No competing neon siblings.
2. **Neutrals carry most UI** — bg, surfaces, borders, nav, body text. Accent is scarce.
3. **Don’t rainbow** — status/tags stay muted; charts need labels, not a carnival.
4. **Don’t default purple-AI kit** unless the brief names purple/amethyst as brand (Jet–Amethyst is briefed dark luxury—not “AI premium” purple-on-black with glow). Ban unearned violet/indigo SaaS defaults per [standards](../../ui-ux-standards.md).
5. **Accent targets only:** one focal keyword, primary CTA, small icon/underline—or **one** intentional accent plane that echoes the hero (≤ ~10% surface). Never paint large chrome, cards, or body fills in accent.
6. **Imagery ↔ palette harmony** — extract or justify colors from the hero/subject (sofa→sage, wood→walnut, light→amber; iris→amethyst; caustics→red glow). Don’t invent a third mood.
7. **Contrast / a11y** — body text ≥ **4.5:1** on its bg; large text (≥18px/14px bold) ≥ **3:1**. Accent-on-light for a keyword is emphasis—if it fails AA for small text, keep it display-size only and use neutrals for body/links. Focus rings visible; never color-alone for status.
8. **Quiet chrome** — thin borders, solid surfaces, restrained top bar. Serif (or strong display) for the headline; calm sans for nav/UI.

## Roles (name them)

| Role | Typical ratio | Owns |
| --- | --- | --- |
| **Dominant** | ~60% (light) or ~70–85% (dark luxury) | Page/section background, large quiet fields |
| **Secondary** | ~25–30% | Text, surfaces, structural imagery tones, borders |
| **Accent** | ~5–10% (often ≤5% dark sparkle) | Focal word, primary CTA, tiny icon, optional one hero-tied plane |

Optional fourth token: **muted** (secondary text, hairlines)—still neutral, not a second accent.

CSS mental model: `--bg`, `--surface`, `--text`, `--muted`, `--border`, `--accent` (exactly one accent).

## Balance recipes (from refs)

### Light / nature (Sage–Walnut–Amber)

| Token | Hex | Placement |
| --- | --- | --- |
| Field (dominant) | warm cream / off-white | Section bg |
| Sage (secondary mood) | `#87A96B` | Hero subject, plants, soft panels—not every card |
| Walnut (secondary structure) | `#5A3E2B` | Headline/nav text, wood tones, strong type |
| Amber (accent) | `#D5851F` | **One** keyword (*alive*), maybe CTA fill or underline |

Approx **60 / 30 / 10** (field+quiet · sage/walnut structure · amber).

### Dark luxury (Jet–Amethyst–Cyan)

| Token | Hex | Placement |
| --- | --- | --- |
| Jet (dominant) | `#050505` | Full canvas |
| Amethyst (secondary mood) | `#3B0A6B` | Hero blooms / depth—not purple buttons everywhere |
| Light text | near-white | Headline + body on Jet |
| Cyan (accent) | `#00E5FF` | Sparkle edges, one highlight—**never** big fills |

Approx **80 / 15 / 5** (jet · amethyst-in-image · cyan sparkle).

### Neutral + signal (Charcoal–Silver–Red)

| Token | Hex | Placement |
| --- | --- | --- |
| Silver (dominant) | `#C0C0C0` or lighter grey field | Main bg |
| Charcoal (secondary) | `#2A2A2A` | Type, rock/structure in image |
| Red (accent) | `#E10600` | Keyword (*brighter*) + ≤one accent strip/glow tied to hero |

Approx **60 / 30 / 10** (silver field · charcoal type/structure · red pop).

## Process

1. **Subject / mood** — one line: surface, audience, vibe (nature calm / dark luxury / industrial signal…). Reject “generic SaaS purple.”
2. **Extract or propose 2–4 named hexes** — prefer hero-derived. Name them (Sage, Walnut, Amber…), not only roles.
3. **Assign roles + ratios** — dominant / secondary / accent (+ muted). Pick a recipe above or adapt with the same scarcity.
4. **Apply map** — where each token lands: `--bg`, text, surfaces, **accent targets** (keyword? CTA? icon? one plane?).
5. **Before/after checklist** — flat→pop without rainbow; contrast OK; chrome still quiet.

## Output (required)

### 1. Token table

| Name | Hex | Role | Ratio (approx) | Notes |
| --- | --- | --- | --- | --- |
| … | `#……` | dominant/secondary/accent/muted | % | … |

### 2. Placement map

| Region | Token | Do |
| --- | --- | --- |
| Page / section bg | | |
| Surfaces / cards | | |
| Headline / body / muted | | |
| Nav / chrome | | |
| Accent targets | | keyword / CTA / icon / optional one plane |
| Hero imagery | | which hues already live in the photo |

### 3. Code / CSS changes

List concrete edits: CSS variables, Tailwind theme keys, component class swaps. Prefer tokens over scattered hex. Example shape:

```css
:root {
  --bg: …;
  --surface: …;
  --text: …;
  --muted: …;
  --border: …;
  --accent: …; /* one only */
}
```

Call out: which headline span gets accent; CTA uses solid `--accent`; strip competing purple/gradients.

### 4. A11y note

State contrast assumptions (e.g. Walnut on cream AA; Amber keyword display-only; white on Jet AA; Red keyword on silver—verify).

## Checklist before done

- [ ] 2–4 **named** colors with hex + roles
- [ ] One accent only; neutrals dominate
- [ ] Accent limited to focus targets (not large UI fills)
- [ ] Colors justified by subject/hero (or explicit brief)
- [ ] Ratios stated (~60-30-10 or dark ~80-15-5)
- [ ] Serif/display headline + quiet chrome preserved or proposed
- [ ] No unearned purple-AI / glow / rainbow kit
- [ ] Contrast checked for text pairs; accent failure → display-size only
- [ ] Token table + placement map + CSS change list delivered

## What NOT to do

- Don’t restyle layout, type families, or SEO—**color roles & balance only**.
- Don’t add a second “pop” color “for variety.”
- Don’t put accent on every link, badge, chart series, and header.
- Don’t swap purple slop for cream+terracotta (or any other meme) unless the brief earns it.
- Don’t use Electric Cyan / Signal Red / Amber as section backgrounds.
- Don’t leave raw hex scatter—tokenize first.

## Companion skills

| Need | Skill |
| --- | --- |
| Full de-AI / visual rewrite | [restyle](../restyle/SKILL.md) |
| Vague fix across viewports | [ux-improve](../ux-improve/SKILL.md) |
| Greenfield screen | [ux-design](../ux-design/SKILL.md) |
| Landing art direction | Taste / `design-taste-frontend` ([taste-skill](https://github.com/Leonxlnx/taste-skill)) |
| Detect-only | [ux-audit](../ux-audit/SKILL.md) |
