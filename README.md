# Bug Lens Triage Skill

> Official Agent Skill for **[Bug Lens](https://github.com/Aoyia/bug-lens)** — Browser bug evidence triage & AI code fix.

This repository distributes the official `bug-lens-triage` skill for modern AI coding assistants (Claude Code, Cursor, Windsurf, Antigravity, Codex, etc.).

## 🚀 Quick Install

Install globally to all supported AI assistants:

```bash
npx skills add Aoyia/bug-lens-skill -g -y
```

Or install in your current project workspace:

```bash
npx skills add Aoyia/bug-lens-skill -y
```

## 🔄 Updating Skill

```bash
npx skills update bug-lens-triage
```

## 🗑️ Uninstalling Skill

```bash
# Global uninstall
npx skills remove bug-lens-triage -g -y

# Or project-scoped uninstall
npx skills remove bug-lens-triage -y
```

## 📖 How It Works

Once installed, your AI programming assistant automatically gains the ability to:
1. Idempotently extract `web-bug-report-*.zip` and `bug-lens-screenshot-*.zip` archives into an isolated workspace directory with plain formatted `data/*.json` and an `INDEX.md` schema index.
2. Inspect key screenshots, extracted video frames, Console errors, Network payloads, and DOM/CSS cascade trees without polluting your workspace.
3. Automatically prune historical workspace packages via an LRU cache (defaulting to the 10 most recent packs).

## 🔗 Links & Feedback

- **Main Repository & Browser Extension**: [Aoyia/bug-lens](https://github.com/Aoyia/bug-lens)
- **Issue Tracker**: [Report a Bug or Feature Request](https://github.com/Aoyia/bug-lens/issues)
- **License**: AGPL-3.0 (same as Bug Lens core)
