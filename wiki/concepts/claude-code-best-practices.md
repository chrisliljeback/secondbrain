---
type: concept
tags: [ai-tooling, claude-code, workflow, reference]
created: 2026-07-05
updated: 2026-07-05
sources: ["[[claude-code-best-practices-guide]]"]
---

# Claude Code best practices

Distilled patterns for working effectively with Claude Code, relevant to
[[christoffer-liljeback]]'s habit of building in-house tools with Claude
(Ad Creator, Launch Hub, Product Image Editor, Content Hub).

## Core constraint
Context window fills fast; performance degrades as it fills. Most other
practices exist to manage this.

## Practices
- **Give Claude a way to verify its work** — tests, a build, a screenshot diff.
  Without a check, "looks done" is the only signal, and every mistake waits for
  a human to notice. A pass/fail check lets Claude iterate unattended.
- **Explore, then plan, then code** — separate research/planning from
  implementation on anything non-trivial (multi-file changes, unfamiliar code).
  Skip planning when the diff could be described in one sentence.
- **Be specific in prompts** — reference exact files, state constraints, point
  to existing patterns to follow. Vague prompts are fine for open-ended
  exploration, costly for anything you want done right the first time.
- **Write and maintain an effective CLAUDE.md** — persistent project context
  (commands, code style, workflow rules) Claude can't infer from code alone.
  Keep it short and human-readable; refine over time rather than front-loading.
- **Manage context aggressively** — course-correct early, don't let a session
  run long on a wrong path, use subagents for investigation so exploration
  doesn't consume the main context window.
- **Scale via automation** — non-interactive/scriptable runs, multiple parallel
  sessions, an adversarial review step (fresh model checks the work) for
  higher-stakes changes.

## Relevance to Christoffer's work
Direct application to his in-house tool stack: writing a real CLAUDE.md for each
tool repo (e.g. `chrisliljeback/launch-hub`), giving build/test checks so Claude
can iterate on the apps unattended, and using subagents when debugging across
the Ad Creator / Launch Hub / Product Image Editor / Content Hub codebases.

## Related
- [[christoffer-liljeback]] — builds tools with Claude day-to-day.
- Source: [[claude-code-best-practices-guide]]
