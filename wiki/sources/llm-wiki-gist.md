---
type: source
tags: [source, method, knowledge-management, ai, meta]
created: 2026-07-05
updated: 2026-07-05
source_path: "Clippings/llm-wiki.md"
source_url: "https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f"
author: Andrej Karpathy
clipped: 2026-07-05
---

# Source: llm-wiki (Karpathy gist)

The original idea file that this whole vault is built on. Author: Andrej Karpathy.
It describes the pattern, not an implementation — deliberately abstract, meant to be
handed to an LLM agent to instantiate. See the compiled concept page:
[[llm-wiki-pattern]].

## Key takeaways
- **Problem with plain RAG:** the LLM rediscovers knowledge from scratch every query;
  nothing accumulates. This pattern instead maintains a persistent, compounding wiki.
- **Three layers:** raw sources (immutable) → LLM-owned wiki → schema file
  (`CLAUDE.md` / `AGENTS.md`) that makes the LLM a disciplined maintainer.
- **Three operations:** ingest, query (file good answers back as pages), lint.
- **index.md + log.md** carry navigation and history; the greppable log-prefix trick
  (`## [date] ingest | Title`) comes from here.
- **Scales** to ~100 sources / hundreds of pages on the index file alone before you
  need real search (e.g. `qmd`, a local BM25/vector markdown search w/ CLI + MCP).
- **Use cases:** personal (goals/health/self), research, reading a book (fan-wiki
  style, cf. Tolkien Gateway), business/team, competitive analysis, trip planning.
- **Obsidian tips:** Web Clipper for sources, local image download, graph view,
  Marp (slides), Dataview (queries over frontmatter). The wiki is just a git repo.
- **Lineage:** spiritually Vannevar Bush's *Memex* (1945) — the part Bush couldn't
  solve was who maintains the trails; the LLM does.

## Pages touched
- [[llm-wiki-pattern]] (updated — now cites this clipped source directly)
- [[overview]], [[index]], [[log]] (updated)
