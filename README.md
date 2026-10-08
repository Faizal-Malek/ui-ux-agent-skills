# UI/UX Agent Skills (De-AI)

Installable agent skills plus durable standards so coding agents stop shipping AI-looking dashboards, product UI, and landing pages—and improve craft + responsive layout **without** a long pixel brief.

**Owner:** [Faizal-Malek](https://github.com/Faizal-Malek) · **License:** MIT

## Skills

| Skill | Invoke | Purpose |
| --- | --- | --- |
| [ux-improve](skills/ux-improve/SKILL.md) | `/ux-improve` | **Default:** find → fix → explain across mobile/tablet/laptop/desktop |
| [ux-design](skills/ux-design/SKILL.md) | `/ux-design` | Design a screen from a brief |
| [ux-audit](skills/ux-audit/SKILL.md) | `/ux-audit` | Detect-only inventory (AI tells + craft + responsive) |
| [ux-review](skills/ux-review/SKILL.md) | `/ux-review` | Review UI in a PR/diff |
| [restyle](skills/restyle/SKILL.md) | `/restyle` | Kill the AI look / restyle an existing screen |

Standards: [ui-ux-standards.md](ui-ux-standards.md). Index: [skills-index.md](skills-index.md). Refs: [references/](references/). Media: [media/](media/).

### Suggested use order

1. **Vague “fix this UI”** → `ux-improve`
2. **Greenfield** → `ux-design`
3. **Detect-only** → `ux-audit` then `ux-improve` / `restyle`
4. **PR gate** → `ux-review`

### Four viewports (every improve/design/restyle)

| Mobile | Tablet | Laptop | Desktop |
| --- | --- | --- | --- |
| 375px | 768px | 1024px | 1440px |

## Compared to other repos

| Repo | What it’s good at | How we relate |
| --- | --- | --- |
| [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Huge searchable style/palette/UX DB + Python search | We absorbed the **craft priority ladder** + responsive checks into lean markdown—not the full CSV/Python runtime |
| [responsive-craft](https://github.com/kylezantos/responsive-craft) | Breakpoint engineering + AI CSS failure patterns | Four-width protocol + failure list in `references/` |
| [mblode/agent-skills ui-design](https://github.com/mblode/agent-skills) | Autonomous audit→fix→ship verdict | Inspired **`ux-improve`** (low-prompt fix + change review) |
| [taste-skill](https://github.com/Leonxlnx/taste-skill) ([site](https://www.tasteskill.dev)) | Best-in-class **landing/portfolio** anti-slop; Design Read + dials; redesign audit | **Complementary** — use for marketing art direction; we own dashboards/product + 4-viewport improve |
| **This repo** | De-AI five-tell maps + Linear product bar + autonomous improve | Best when you want anti-slop **and** “just fix it” with why |

## Repo layout

```text
.
├── .cursor-plugin/plugin.json
├── plugin.json
├── skills/
│   ├── ux-improve/SKILL.md
│   ├── ux-design/SKILL.md
│   ├── ux-audit/SKILL.md
│   ├── ux-review/SKILL.md
│   └── restyle/SKILL.md
├── references/
│   ├── responsive-breakpoints.md
│   └── craft-qa.md
├── media/
├── ui-ux-standards.md
├── skills-index.md
├── LICENSE
└── README.md
```

## Install

### Cursor (project skills)

```bash
REPO=~/ui-ux-agent-skills   # or path to this clone
mkdir -p .agents/skills .cursor/skills media
for s in ux-improve ux-design ux-audit ux-review restyle; do
  cp -R "$REPO/skills/$s" .agents/skills/
  cp -R "$REPO/skills/$s" .cursor/skills/
done
cp "$REPO/ui-ux-standards.md" "$REPO/skills-index.md" .
mkdir -p references && cp "$REPO"/references/*.md references/
cp "$REPO"/media/*.jpg media/
```

Or symlink from a single clone:

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git ~/ui-ux-agent-skills
mkdir -p .agents/skills
for s in ux-improve ux-design ux-audit ux-review restyle; do
  ln -sfn ~/ui-ux-agent-skills/skills/$s .agents/skills/$s
done
```

### Cursor (user / global)

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git ~/ui-ux-agent-skills
mkdir -p ~/.agents/skills ~/.cursor/skills
for s in ux-improve ux-design ux-audit ux-review restyle; do
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.agents/skills/$s
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.cursor/skills/$s
done
```

### Antigravity (global)

```bash
mkdir -p ~/.gemini/config/skills ~/.gemini/antigravity/skills
for s in ux-improve ux-design ux-audit ux-review restyle; do
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.gemini/config/skills/$s
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.gemini/antigravity/skills/$s
done
```

### Cursor plugin / marketplace

`.cursor-plugin/plugin.json` + root `plugin.json` ship with this repo. Skills are under `skills/`.

## Clone

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git
# or
git clone https://github.com/Faizal-Malek/ui-ux-agent-skills.git
```
