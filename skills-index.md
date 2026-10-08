# Skills set — UI/UX (De-AI)

Installable skill drafts plus durable standards so agents stop shipping AI-looking dashboards, product UI, and landing pages.

## Standards

- [UI/UX Standards](ui-ux-standards.md) — (A) dashboard five tells/fixes · (B) Linear “expensive” five decisions · (C) landing five tells/fixes · shared bans · cited sources

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
| [ux-design](skills/ux-design/SKILL.md) | `/ux-design` | Design a screen from a brief |
| [ux-audit](skills/ux-audit/SKILL.md) | `/ux-audit` | Find every AI tell |
| [ux-review](skills/ux-review/SKILL.md) | `/ux-review` | Review UI in a PR/diff |
| [restyle](skills/restyle/SKILL.md) | `/restyle` | Kill the AI look / restyle an existing screen |

Each skill is a `SKILL.md` package with YAML `name` + `description` frontmatter. Skills cite published GitHub sources and fold useful checklists into these four—rather than vendoring unrelated skill trees.

## Suggested use order

1. **Greenfield** → `ux-design`
2. **Existing AI-looking UI** → `ux-audit` then `restyle`
3. **PR gate** → `ux-review`

## External sources (summary)

Full citation table lives in [ui-ux-standards.md](ui-ux-standards.md#sources-published-skills-we-borrowed-from). Primary borrows: Anthropic `frontend-design`, `avoid-ai-design`, `redesign-skill`, `ux-audit`, `de-ai-ui`, `ui-ux-kit`, `impeccable`.
