# vibe-tools (notes)

`eastlondoner/vibe-tools` is a separate Node CLI (not a Codex skill repo) that adds an “AI team” of commands you can call from an agent.

## Why it’s interesting
- Multi-provider model access (`ask`, `web`, `repo`, `plan`).
- Browser automation via Playwright + Stagehand (`browser`).
- MCP client (`mcp`) and integrations (GitHub, Linear, ClickUp, YouTube).

## Install (optional)
- `npm install -g vibe-tools`
- Run `vibe-tools install .` inside a repo to set up IDE integration.

## Command categories
- Research: `vibe-tools web "..."`
- Codebase Q&A: `vibe-tools repo "..."`
- Planning: `vibe-tools plan "..."`
- Docs: `vibe-tools doc "..."`
- Browser: `vibe-tools browser open|act|extract|observe ...`
- MCP: `vibe-tools mcp search|run ...`
- GitHub: `vibe-tools github pr|issue ...`
- Video: `vibe-tools youtube <url> --type summary|transcript|plan`

## When to use it vs Codex alone
- Use it when you want one command that wraps web search, big-context repo ingestion, or browser automation.
- Skip it if you don’t want extra tooling/API keys; Codex + `curl`/Python/Playwright can cover most needs.
