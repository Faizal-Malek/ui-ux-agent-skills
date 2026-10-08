# UI/UX Agent Skills (De-AI)

Installable agent skills plus durable standards so coding agents stop shipping AI-looking dashboards, product UI, and landing pages.

**Owner:** [Faizal-Malek](https://github.com/Faizal-Malek) · **License:** MIT

## Skills

| Skill | Invoke | Purpose |
| --- | --- | --- |
| [ux-design](skills/ux-design/SKILL.md) | `/ux-design` | Design a screen from a brief |
| [ux-audit](skills/ux-audit/SKILL.md) | `/ux-audit` | Find every AI tell |
| [ux-review](skills/ux-review/SKILL.md) | `/ux-review` | Review UI in a PR/diff |
| [restyle](skills/restyle/SKILL.md) | `/restyle` | Kill the AI look / restyle an existing screen |

Standards live in [ui-ux-standards.md](ui-ux-standards.md). Index: [skills-index.md](skills-index.md). Reference media: [media/](media/).

### Suggested use order

1. **Greenfield** → `ux-design`
2. **Existing AI-looking UI** → `ux-audit` then `restyle`
3. **PR gate** → `ux-review`

## Repo layout

```text
.
├── .cursor-plugin/plugin.json   # Cursor plugin manifest
├── plugin.json                  # Agent Plugins (portable) manifest
├── skills/
│   ├── ux-design/SKILL.md
│   ├── ux-audit/SKILL.md
│   ├── ux-review/SKILL.md
│   └── restyle/SKILL.md
├── media/                       # before/after reference images
├── ui-ux-standards.md
├── skills-index.md
├── LICENSE
└── README.md
```

## Install

### Cursor (project skills)

From this repo root, copy skills into your project:

```bash
mkdir -p .agents/skills .cursor/skills
cp -R skills/ux-design skills/ux-audit skills/ux-review skills/restyle .agents/skills/
cp -R skills/ux-design skills/ux-audit skills/ux-review skills/restyle .cursor/skills/
# optional: keep the standards next to the skills for relative links
cp ui-ux-standards.md skills-index.md .
mkdir -p media && cp media/*.jpg media/ 2>/dev/null || cp -R media .
```

Or clone once and symlink:

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git ~/ui-ux-agent-skills
mkdir -p .agents/skills
for s in ux-design ux-audit ux-review restyle; do
  ln -sfn ~/ui-ux-agent-skills/skills/$s .agents/skills/$s
done
```

Cursor loads skills from `.agents/skills/` and `.cursor/skills/` (project) and `~/.agents/skills/` / `~/.cursor/skills/` (user).

### Cursor (user / global)

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git ~/ui-ux-agent-skills
mkdir -p ~/.agents/skills ~/.cursor/skills
for s in ux-design ux-audit ux-review restyle; do
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.agents/skills/$s
  ln -sfn ~/ui-ux-agent-skills/skills/$s ~/.cursor/skills/$s
done
```

### Cursor plugin / marketplace

This repo ships `.cursor-plugin/plugin.json` (Cursor Plugin) and root `plugin.json` (Agent Plugins). Skills are discovered under `skills/`. Import the GitHub repo in Cursor **Plugins → Team Marketplaces** / **From GitHub Repository**, or copy the folder into `~/.cursor/plugins/local/ui-ux-agent-skills` and reload the window.

### Antigravity / other harnesses

Copy or symlink the four folders under `skills/` into your harness skills directory (commonly `.agents/skills/` in a project, or the tool’s user skills path). Each skill is a self-contained `SKILL.md` with YAML `name` + `description` frontmatter.

## Clone

```bash
git clone git@github.com:Faizal-Malek/ui-ux-agent-skills.git
# or
git clone https://github.com/Faizal-Malek/ui-ux-agent-skills.git
```

## Sources

Skills cite published GitHub sources summarized in [ui-ux-standards.md](ui-ux-standards.md#sources-published-skills-we-borrowed-from). Primary borrows: Anthropic `frontend-design`, `avoid-ai-design`, `redesign-skill`, `ux-audit`, `de-ai-ui`, `ui-ux-kit`, `impeccable`.
