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

## 📖 How It Works

Once installed, your AI programming assistant automatically gains the ability to:
1. Inspect `web-bug-report-*.zip` and `bug-lens-screenshot-*.zip` archives directly in memory.
2. Auto-extract key screenshots with user annotations and red-ring click markers.
3. Drill down into Console logs, Network payloads, and DOM/CSS cascade trees without polluting your workspace.

## 🔗 Links & Feedback

- **Main Repository & Browser Extension**: [Aoyia/bug-lens](https://github.com/Aoyia/bug-lens)
- **Issue Tracker**: [Report a Bug or Feature Request](https://github.com/Aoyia/bug-lens/issues)
- **License**: AGPL-3.0 (same as Bug Lens core)
