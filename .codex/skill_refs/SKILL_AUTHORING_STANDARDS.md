# Skill Authoring Standards

These standards exist to prevent “hand-wavy” skills that look good but fail at execution.

## Required sections in every SKILL.md

* **When to Activate** (clear triggers; keywords; examples)
* **Inputs** (what must be provided; what to fetch)
* **Outputs / DoD** (what “done” means; verification)
* **Procedure** (numbered steps; explicit tools/commands)
* **Edge cases / Failure modes** (what breaks; how to recover)

## Anti-patterns to remove

* “…” as a placeholder for missing steps
* “etc.” when the list of requirements matters
* “Do something like X” without exact commands/paths
* “Handle errors” without what errors and how

## Minimum quality bar checklist

Before merging a skill change:

* [ ] A newcomer can execute it without guessing
* [ ] Inputs are explicit
* [ ] Outputs are verifiable
* [ ] At least one worked example exists
* [ ] No secret-handling violations
