# Reusable development workspace

A language/framework-neutral template for fullstack/backend projects.

## Adopt

Copy these six files, preserving relative paths:

- [AGENTS.md](AGENTS.md): workflow and approval boundaries.
- This README: adoption instructions.
- [docs/engineering.md](docs/engineering.md): task-specific SWE guidance.
- [Requirements](docs/templates/requirements.md), [plan](docs/templates/plan.md), and [review](docs/templates/review.md) templates: fields for each stage.

Exclude this source workspace's docs/requirements.md, docs/plans/, and docs/reviews/: they record template development, not application requirements or approvals.

1. Discuss the project and create docs/requirements.md from its template. Keep unknowns explicit; approve requirements before implementation.
2. Replace the opening template context in AGENTS.md with the approved project summary; adapt this README. Preserve links to the workflow and engineering guidance.
3. Save an editable task plan in docs/plans/ and obtain approval. During approved setup, select the stack, supported versions, exact check commands, and CI. No tooling is preselected here.
4. Implement, verify, and save a concise self-review in docs/reviews/; hand off for human review.

For existing repositories, merge compatible guidance with their instructions, layout, and tooling; preserve existing files and resolve conflicts openly.

AGENTS.md holds shared policy. Supporting files load when relevant; avoid repeating policy in templates. Documentation does not enforce CI checks.
