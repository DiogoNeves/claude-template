# Claude Template

A template for quickly setting up [Claude Code](https://code.claude.com/docs/en/overview) in new or existing projects.

## Why?

Setting up Claude Code with consistent settings and commands across projects can be repetitive. This template provides:

- **Pre-configured settings** with sensible defaults and security rules
- **Useful commands** for common workflows
- **Safe updates** via a dedicated update command

Since `.claude/` is committed to your repo, your whole team shares the same Claude configuration.

## Quick Start

1. Open your project in [Claude Code](https://code.claude.com)
2. Ask Claude Code to copy the `.claude` folder from this repository
3. Start using Claude Code as normal

## What's Included

```
.claude/
├── settings.json           # Permissions and security settings
└── commands/
    ├── commit-push-pr.md   # Stage, commit, push, and create PR
    └── update-template.md  # Update template files from this repo
```

### Settings

The default `settings.json` includes:

- **Allowed**: Git commands, GitHub CLI, common read operations
- **Denied**: Access to `.env` files, dangerous commands (`rm -rf`, `sudo`, `chmod 777`)

### Commands

Run these with `/commit-push-pr` or `/update-template` in Claude Code.

| Command            | Description                                  |
| ------------------ | -------------------------------------------- |
| `/commit-push-pr`  | Stage changes, commit, push, and create a PR |
| `/update-template` | Pull latest template files from this repo    |

## Updating

To get the latest template files, run `/update-template` in Claude Code. It will:

1. Fetch the latest files from this repository
2. Ask before overwriting any existing files
3. Merge new commands and settings

## What's Not Included

**`CLAUDE.md`** is intentionally left out of this template. This file contains project-specific instructions (tech stack, conventions, architecture) that vary between projects. Create your own `CLAUDE.md` in your project root with context relevant to your codebase.

## License

[MIT](LICENSE)
