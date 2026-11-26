# Bug Lens Triage Skill

[English Version](README.md) | **中文文档**

> **[Bug Lens](https://github.com/Aoyia/bug-lens)** 官方 Agent Skill — 浏览器缺陷证据排查与 AI 代码修复。

本仓库分发官方 `bug-lens-triage` Skill（内置原生 Rust `bug-lens-cli` 二进制），适用于 Claude Code、Cursor、Windsurf、Antigravity、Codex 等现代 AI 编程助手。

## 快速安装

全局安装到所有受支持的 AI 助手：

```bash
npx skills add Aoyia/bug-lens-skill -g -y
```

或仅安装到当前项目工作区：

```bash
npx skills add Aoyia/bug-lens-skill -y
```

随后安装原生 Rust `bug-lens-cli` 二进制（仅首次通过 SHA-256 校验从 GitHub Releases 下载，CLI 运行时严格零外联）：

```bash
# macOS / Linux
bash "<skillDir>/scripts/install.sh"

# Windows (PowerShell)
powershell -ExecutionPolicy Bypass -File "<skillDir>\scripts\install.ps1"
```

## 更新 Skill

```bash
npx skills update bug-lens-triage
```

## 卸载 Skill

```bash
# 全局卸载
npx skills remove bug-lens-triage -g -y

# 或项目级卸载
npx skills remove bug-lens-triage -y
```

## 工作原理

安装完成后，AI 编程助手将自动获得以下能力：
1. 使用原生 Rust `bug-lens-cli` 二进制将 `web-bug-report-*.zip` 与 `bug-lens-screenshot-*.zip` 流式解压到独立工作区，生成标准 `data/*.json` 与 `INDEX.md` 结构索引。
2. 在不污染当前工程目录的前提下，按需下钻检查关键截图、视频抽帧、Console 报错、Network 报文与 DOM/CSS 级联树。
3. 通过 LRU 缓存自动清理历史工作区证据包（默认保留最近 10 个包）。

## 相关链接与反馈

- **主仓库与浏览器扩展**：[Aoyia/bug-lens](https://github.com/Aoyia/bug-lens)
- **问题反馈**：[提交 Bug 或功能建议](https://github.com/Aoyia/bug-lens/issues)
- **开源协议**：AGPL-3.0（与 Bug Lens 主仓库一致）
