# Codex Skill Playbook (local)

This is a lightweight “what to use when” index for your installed Codex skills, plus a place to stash useful patterns you want available across projects.

## Start Here
- Canonical entrypoint: `skills.md` (repo root; from here: `../../skills.md`)
- Global rules: `.codex/instructions.md`
- Skill standards: `.codex/skill_refs/SKILL_AUTHORING_STANDARDS.md`

## Installed skills (high impact)

### Coding / GitHub
- `gh-fix-ci`: When CI is red; paste logs + ask for minimal fix.
- `gh-address-comments`: When you need to respond to PR review comments and update code accordingly.

### Context + long-running work
- `filesystem-context`: Offload big outputs to files; keep a scratchpad + persistent plan.
- `context-compression`: Summarize/compact long histories while preserving constraints + decisions.
- `context-optimization`: Mask/cull low-signal tokens; cache stable context; keep “active” context small.
- `context-degradation`: Diagnose lost-in-the-middle, distraction, poisoning, and instruction clashes.
- `context-fundamentals`: Canonical mental model for what “context” includes (system/tools/memory/history/retrieval).

### Agent architecture / toolcraft
- `tool-design`: Design tools/CLIs/APIs that agents can use reliably.
- `memory-systems`: Short/long-term memory patterns, schemas, and retrieval strategies.
- `multi-agent-patterns`: Supervisor/worker, peer, and hierarchical patterns; delegation and coordination.

### Evaluation
- `evaluation`: Build eval harnesses, metrics, and regression checks.
- `advanced-evaluation`: LLM-as-judge patterns, rubrics, bias mitigation, pairwise vs direct scoring.

## Installed but more niche (keep if you use them)
- `analyzing-financial-statements`
- `creating-financial-models`

## Not installed (good source material)
From `muratcankoylan/Agent-Skills-for-Context-Engineering`:
- `project-development` (pipeline patterns + case studies)
- `bdi-mental-states` (formal BDI ontology + RDF/SPARQL patterns)

From `eastlondoner/vibe-tools`:
- Not a Codex skill repo; it’s a separate Node CLI that adds commands like `web`, `repo`, `browser`, `mcp`, `youtube`.

## Browsing / research without extra tools
- Prefer lightweight fetch + parse: `curl -L <url>`, save to a file, then extract what you need.
- For JS-heavy sites, use a headless browser (Playwright) if/when installed.

## References
- Full ranked list snapshot: `top100_ranked.md`
- Skill standards: `SKILL_AUTHORING_STANDARDS.md`
- vibe-tools notes: `VIBE_TOOLS.md`
- Agent Skills notes: `AGENT_SKILLS_CONTEXT_ENGINEERING.md`
