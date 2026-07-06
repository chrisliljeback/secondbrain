---
type: source
tags: [source, ai-tooling, claude-code, reference]
created: 2026-07-05
updated: 2026-07-05
source_path: "Clippings/Best practices for Claude Code.md"
source_url: "https://code.claude.com/docs/en/best-practices"
clipped: 2026-07-05
---

# Source: Best practices for Claude Code (official docs)

Anthropic's official best-practices guide for Claude Code. Not Strandberg- or
person-specific, but relevant to [[christoffer-liljeback]]'s in-house tool
building (Ad Creator, Launch Hub, Product Image Editor, Content Hub — all built
collaboratively with Claude, per [[about-me-operating-manual]]).

## Key takeaways
- Core constraint: context window fills fast and performance degrades as it
  fills — most other advice follows from managing this.
- Give Claude a way to verify its own work (tests, build, screenshot diff) so
  sessions can run unattended instead of needing constant review.
- Explore → plan → code as separate phases for non-trivial changes; skip
  planning for one-sentence-describable diffs.
- Specific, scoped prompts (reference files, constraints, examples) beat vague
  ones — cuts down on correction cycles.
- Write and maintain an effective CLAUDE.md per project — persistent context
  Claude can't infer from files alone.
- For scale: non-interactive/scriptable mode, running multiple sessions in
  parallel, subagents for investigation, and an adversarial review step for
  higher-stakes changes.

## Pages touched
- [[claude-code-best-practices]] (created — distilled concept page)
