---
type: concept
tags: [method, knowledge-management, ai, meta]
created: 2026-07-05
updated: 2026-07-05
sources: ["[[llm-wiki-gist]]", "[[how-i-built-this-tutorial]]", "[[How to create a Second Brain]]"]
---

# LLM wiki pattern

The method this vault is built on (from Karpathy's *llm-wiki* gist — full source:
[[llm-wiki-gist]]). It's the "why" behind [[CLAUDE|the schema]].

## Core idea
Most LLM + document workflows are RAG: upload files, retrieve chunks at query time,
generate an answer. The LLM rediscovers knowledge from scratch every question —
nothing accumulates. The LLM wiki is different: the LLM **incrementally builds and
maintains a persistent, interlinked wiki** between you and your raw sources. Add a
source and the LLM reads it, extracts what matters, and integrates it — updating
entity pages, revising summaries, flagging contradictions. Knowledge is compiled
once and kept current.

The wiki is a **compounding artifact**: cross-references already exist, contradictions
already flagged, synthesis already reflects everything read. It gets richer with
every source and every question.

## The three moves (practical framing)
A beginner-friendly way to say the same thing (see [[how-i-built-this-tutorial]]):
**collect → compile → ask.**
1. **Collect** — gather good sources into one folder (`Clippings/`). Start with ~10
   solid ones, not 100. Tip: for a YouTube video, copy its transcript into a text
   file and drop it in.
2. **Compile** — the LLM reads it all and writes/updates the connected wiki.
3. **Ask** — question the wiki; answers come from *your* knowledge, with links back
   to source. Two standout queries: *"where do my sources agree and disagree?"* and
   *"where are the gaps — what should I learn next?"*

## Three layers
1. **Raw sources** (immutable) — here, `Clippings/`.
2. **The wiki** (LLM-owned) — here, `wiki/`.
3. **The schema** — here, `CLAUDE.md`.

## Operations
- **Ingest** — process a new source into summary + entity/concept pages + index + log.
- **Query** — answer from the wiki with citations; file good answers back as pages.
- **Lint** — periodically health-check for contradictions, stale claims, orphans,
  missing pages/links, gaps.

## Why it works
The hard part of a knowledge base isn't reading or thinking — it's the bookkeeping
(cross-refs, keeping summaries current, consistency across dozens of pages). Humans
abandon wikis because maintenance grows faster than value. LLMs don't get bored and
can touch 15 files in one pass, so maintenance cost approaches zero. Spiritually
related to Vannevar Bush's **Memex** (1945) — the part Bush couldn't solve was who
does the maintenance; the LLM handles that.

## Optional tooling (not yet set up)
- `qmd` — local hybrid BM25/vector markdown search (CLI + MCP) for when the index
  file isn't enough at scale.
- Obsidian: Web Clipper (sources → markdown), graph view (shape of the wiki), Marp
  (slides from pages), Dataview (queries over frontmatter).

## Related
- [[How to create a Second Brain]] — a complementary "business/personal OS" folder
  structure (context / daily / projects / resources / skills) that could be layered
  in later if the vault grows beyond a pure knowledge wiki.
