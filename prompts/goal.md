```markdown
Complete all objectives, then open a PR that achieves a fully green state (all CI checks passing, all reviewer feedback addressed).

## Work Style

- **Task-based, red-green, data-backed, exploratory, science-driven.**
- Commit and push freely. Small, coherent commits.
- Address all non-trivial reviewer feedback and CI failures before moving to the next task.

## Fix Philosophy

| Failure type | Fix target |
|---|---|
| Production bug | Production code |
| Test bug | Test code |
| Fragile / unnecessary check | Remove or rewrite it |

- Prefer **data-driven tests** over repeated similar test cases.
- Add **diagnostics** when an issue is hard to understand without them.
- When a bug is found, **sweep the codebase** for the same class of problem and fix all instances — eliminate the entire failure mode, not just the immediate symptom.
- **Simplify aggressively.** Do not add tests, scripts, or abstractions unless they prevent a real, recurring issue.

## Quality Bar

Every change must be:

- **Robust and reliable** — not fragile or coupled to implementation details.
- **Complete** — the whole class of problem is addressed, not just the one example.
- **Non-bloating** — no unnecessary files, tests, or scaffolding.

Target: consensus among all reviewers that the result needs zero revisions.

## Progress Tracking

- Log work in `progress/session-NNN-brief-description.md` (literal `progress/` at repo root).
- Unified formatting; descriptive names for easy discovery.

## Sub-agent Loop

1. Use sub-agents for parallel or specialized work when required.
2. After a sub-agent completes, have an **adversarial sub-agent** review it critically.
3. If recommendations exist, have another sub-agent evaluate and implement them.
4. Repeat until all sub-agents agree the result is exceptional with zero issues (minor or otherwise).
5. If not using sub-agents, apply this adversarial review loop on the main thread.
```
