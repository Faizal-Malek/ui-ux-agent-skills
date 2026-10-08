# Skills set — UI/UX (De-AI)

Installable skill drafts plus durable standards so agents stop shipping AI-looking dashboards, product UI, and landing pages—and fix craft/responsive issues without a long brief.

## Standards

- [UI/UX Standards](ui-ux-standards.md) — (A) dashboard five tells/fixes · (B) Linear “expensive” five decisions · (C) landing five tells/fixes · (D) four viewports · (E) craft QA · shared bans · cited sources
- [Responsive breakpoints](references/responsive-breakpoints.md) — 375 / 768 / 1024 / 1440 + AI failure patterns
- [Craft QA](references/craft-qa.md) — a11y, touch, forms, nav, motion, charts

## Reference media

| Asset | Path |
| --- | --- |
| Dashboard before | [de-ai-ui-before.jpg](media/de-ai-ui-before.jpg) |
| Dashboard after | [de-ai-ui-after.jpg](media/de-ai-ui-after.jpg) |
| Landing before (Lumen) | [de-ai-landing-before-lumen.jpg](media/de-ai-landing-before-lumen.jpg) |
| Landing after (Lumen) | [de-ai-landing-after-lumen.jpg](media/de-ai-landing-after-lumen.jpg) |
| Linear expensive · 1 | [linear-expensive-part1.jpg](media/linear-expensive-part1.jpg) |
| Linear expensive · 2 | [linear-expensive-part2.jpg](media/linear-expensive-part2.jpg) |

## Skills

| Skill | Command vibe | Purpose |
| --- | --- | --- |
| [ux-improve](skills/ux-improve/SKILL.md) | `/ux-improve` | **Default:** find + fix + explain across 4 viewports (low prompting) |
| [ux-design](skills/ux-design/SKILL.md) | `/ux-design` | Design a screen from a brief |
| [ux-audit](skills/ux-audit/SKILL.md) | `/ux-audit` | Detect-only inventory (AI + craft + responsive) |
| [ux-review](skills/ux-review/SKILL.md) | `/ux-review` | Review UI in a PR/diff |
| [restyle](skills/restyle/SKILL.md) | `/restyle` | Kill the AI look / restyle an existing screen |

Each skill is a `SKILL.md` package with YAML `name` + `description` frontmatter.

## Suggested use order

1. **Vague “fix / improve this UI”** → `ux-improve`
2. **Greenfield** → `ux-design`
3. **Detect-only** → `ux-audit` then `ux-improve` or `restyle`
4. **Explicit de-AI rewrite** → `restyle`
5. **PR gate** → `ux-review`

## External sources (summary)

Full citation table lives in [ui-ux-standards.md](ui-ux-standards.md#sources-published-skills-we-borrowed-from). Primary borrows: Anthropic `frontend-design`, `avoid-ai-design`, `redesign-skill`, `ux-audit`, `de-ai-ui`, `ui-ux-kit`, `impeccable`, `ui-ux-pro-max` (craft ladder), `responsive-craft`, mblode `ui-design`.
