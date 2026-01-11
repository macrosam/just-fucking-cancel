# Sam’s Codex Skills — Start Here

This repo contains a modular “skills pack” for an IDE agent (Codex/Cursor-style) under `.codex/`.

## Quick start (how to use this pack)
1) Read the global operating rules: **`.codex/instructions.md`**
2) Choose the best skill:
   - Start with **`.codex/skill_refs/PLAYBOOK.md`** (practical “what to use when”)
   - Or jump to the installed skills list below
3) Open the chosen skill’s `SKILL.md` and follow its checklist end-to-end.
4) For multi-step work, create/update a **project state log** (template in `.codex/instructions.md`) so the agent stays consistent across turns.
5) If unsure, ask **one** clarifying question or default to a “foundation” skill (context-fundamentals / filesystem-context).

## Installed skills (primary entrypoints)
### Code + GitHub
- **gh-fix-ci** → `.codex/skills/gh-fix-ci/SKILL.md`
- **gh-address-comments** → `.codex/skills/gh-address-comments/SKILL.md`

### Context + long-running work
- **filesystem-context** → `.codex/skills/filesystem-context/SKILL.md`
- **context-compression** → `.codex/skills/context-compression/SKILL.md`
- **context-optimization** → `.codex/skills/context-optimization/SKILL.md`
- **context-degradation** → `.codex/skills/context-degradation/SKILL.md`
- **context-fundamentals** → `.codex/skills/context-fundamentals/SKILL.md`
- **memory-systems** → `.codex/skills/memory-systems/SKILL.md`

### Evaluation
- **evaluation** → `.codex/skills/evaluation/SKILL.md`
- **advanced-evaluation** → `.codex/skills/advanced-evaluation/SKILL.md`

### Architecture / Tooling
- **multi-agent-patterns** → `.codex/skills/multi-agent-patterns/SKILL.md`
- **tool-design** → `.codex/skills/tool-design/SKILL.md`

### Finance (niche / optional)
- **analyzing-financial-statements** → `.codex/skills/analyzing-financial-statements/SKILL.md`
- **creating-financial-models** → `.codex/skills/creating-financial-models/SKILL.md`

## Skill selection (fast routing)
Use this routing rule:
- **If the work touches a repo/PR/CI** → start with `gh-fix-ci` or `gh-address-comments`
- **If the work is large / many steps / lots of tool output** → start with `filesystem-context`
- **If the thread is long / needs summarization** → `context-compression`
- **If the agent is confused / losing constraints** → `context-degradation` then `context-fundamentals`
- **If you need evaluation / scoring / quality gates** → `evaluation` or `advanced-evaluation`
- **If designing tools / agents** → `tool-design` or `multi-agent-patterns`

## Repo map
- `.codex/instructions.md` = global operating rules (must-read)
- `.codex/skills/*/SKILL.md` = skill modules
- `.codex/skill_refs/PLAYBOOK.md` = “what to use when” index
- `.codex/skill_refs/top100_ranked.md` = external reference snapshot (optional)

## Security / secrets (non-negotiable)
- Never paste tokens/keys into chat logs.
- Never commit secrets into the repo.
- Use GitHub Actions secrets / secret managers for credentials.
