# 🦞 ClawSkills

A collection of [OpenClaw](https://github.com/openclaw/openclaw) skills for extending your AI agent's capabilities.

## Skills

| Skill | Description |
|-------|-------------|
| [inkdrop](./inkdrop) | Read, create, update, search, and delete notes in [Inkdrop](https://inkdrop.app) via its local HTTP server API |

## Installation

### Via ClawHub (recommended)

```bash
npm i -g clawhub
clawhub install inkdrop
```

### Manual

Copy the skill folder into your OpenClaw workspace skills directory:

```bash
git clone https://github.com/iamngoni/clawskills.git
cp -r clawskills/inkdrop ~/.openclaw/workspace/skills/
```

Then restart your OpenClaw session so it picks up the new skill.

## Creating a New Skill

Each skill lives in its own folder with at minimum a `SKILL.md`:

```
clawskills/
├── inkdrop/
│   ├── SKILL.md          # Required — skill definition + instructions
│   └── scripts/          # Optional — helper scripts
├── another-skill/
│   ├── SKILL.md
│   ├── scripts/
│   └── references/
└── README.md
```

The `SKILL.md` frontmatter (`name` and `description`) is what OpenClaw uses to decide when to activate a skill, so make the description clear and comprehensive.

## Publishing to ClawHub

```bash
npm i -g clawhub
clawhub login
clawhub publish ./skill-folder --slug skill-name --name "Skill Name" --version 1.0.0
```

## License

MIT
