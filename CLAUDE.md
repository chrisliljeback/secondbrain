# Second Brain — Wiki Schema

This vault is an **LLM-maintained personal wiki**, built on the pattern from
Karpathy's *llm-wiki* (https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).

The idea: instead of re-deriving knowledge from raw documents on every question,
you (the LLM) **incrementally build and maintain a persistent, interlinked wiki**
that sits between Christoffer and his raw sources. Knowledge is compiled once and
kept current, not re-discovered every query.

**Division of labor:** Christoffer sources, explores, and asks questions. You do
all the grunt work — reading, summarizing, cross-referencing, filing, and
bookkeeping. He never writes wiki pages by hand; you write and maintain all of them.

Obsidian is the IDE, you are the programmer, the wiki is the codebase.

---

## Three layers

1. **Raw sources** — `Clippings/`. Immutable. You read from these, never edit them.
   New sources arrive here (usually via the Obsidian Web Clipper as markdown with
   YAML frontmatter). This is the source of truth.

2. **The wiki** — `wiki/`. LLM-generated markdown. You own this layer entirely:
   create pages, update them when new sources arrive, maintain cross-references,
   keep everything consistent.

3. **The schema** — this file. It tells you how the wiki is structured and what
   workflows to follow. Co-evolve it with Christoffer as conventions change.

---

## Directory structure

```
second-brain/
├── CLAUDE.md              ← this file (the schema / brain)
├── Clippings/             ← raw sources (immutable)
└── wiki/
    ├── index.md           ← catalog of every wiki page (content-oriented)
    ├── log.md             ← append-only chronological record of activity
    ├── overview.md        ← the map / high-level synthesis of the whole wiki
    ├── sources/           ← one summary page per ingested source
    ├── entities/          ← people, companies, products, tools, places
    └── concepts/          ← ideas, methods, themes, frameworks
```

Add new page types (e.g. `comparisons/`, `journal/`) only when a real need shows up,
and record the convention here when you do.

**Recurring/snapshot sources** (e.g. a weekly analytics dashboard export): don't
create a new wiki page per clip. Write one source summary per clip as usual (for
traceability), but route the content into a single evolving `entities/` page with
a "Latest snapshot" section that gets **overwritten** each time — it tracks
current state, not history. Note in the source page that it's part of a
recurring series. First example: [[strandberg-web-analytics-dashboard]] →
[[strandberg-web-performance]].

---

## Page conventions

- **Filenames**: kebab-case, no dates in the name (e.g. `strandberg-guitars.md`).
  The filename is the link target.
- **Links**: use Obsidian wikilinks by filename only — `[[strandberg-guitars]]`.
  Obsidian resolves these globally regardless of folder, so no paths needed.
- **Frontmatter**: every wiki page starts with YAML frontmatter so Obsidian's
  Dataview/graph tooling works:
  ```yaml
  ---
  type: entity | concept | source | overview | index | log
  tags: [ ... ]
  created: YYYY-MM-DD
  updated: YYYY-MM-DD
  sources: [ list of source page links ]   # for entity/concept pages
  ---
  ```
- **Source summary pages** additionally record: original source path/URL, date
  clipped, key takeaways, and which entity/concept pages it touched.
- **Every claim should be traceable** to a source. When two sources disagree,
  don't silently overwrite — add a `> [!warning] Contradiction` callout noting
  both claims and their sources.
- Keep prose tight. These are reference pages, not essays.

---

## Operations

### Ingest
When Christoffer drops a source in `Clippings/` and asks to process it:
1. Read the source in full.
2. Briefly discuss the key takeaways with him (unless told to batch silently).
3. Write/update a summary page in `wiki/sources/`.
4. Create or update relevant `entities/` and `concepts/` pages, adding cross-links
   in both directions.
5. Update `wiki/index.md` (add/refresh entries).
6. Update `wiki/overview.md` if the source changes the big picture.
7. Append an entry to `wiki/log.md`.

A single source may touch 5–15 pages. Default to ingesting one source at a time and
staying involved; batch only when asked.

### Query
When he asks a question:
1. Read `wiki/index.md` first to find relevant pages, then drill in.
2. Synthesize an answer **with citations** to the wiki pages (and through them,
   the raw sources).
3. If the answer is valuable and durable (a comparison, an analysis, a discovered
   connection), offer to **file it back into the wiki** as a new page so the
   exploration compounds instead of disappearing into chat.

### Lint
When asked to health-check the wiki, look for:
- Contradictions between pages
- Stale claims superseded by newer sources
- Orphan pages (no inbound links)
- Concepts mentioned repeatedly but lacking their own page
- Missing cross-references
- Gaps that a web search could fill
Report findings and suggest new questions to investigate or sources to look for.

---

## index.md and log.md

- **index.md** is content-oriented: a catalog of every page, grouped by category,
  each with a link and one-line summary. Read it first on any query. Update it on
  every ingest.
- **log.md** is chronological and append-only. Each entry starts with a consistent
  prefix so it's greppable:
  `## [YYYY-MM-DD] ingest | Source Title` (or `query` / `lint`).
  Then `grep "^## \[" wiki/log.md | tail -5` gives the last 5 events.

---

## Notes for future sessions

- This is a **general personal brain** — domain-agnostic. Christoffer works in
  video/content production at Strandberg Guitars, so guitar/content topics will
  recur, but treat any subject (health, ideas, research, hobbies) as first-class.
- Start small; let structure emerge. Don't over-build folders or pages ahead of need.
- When Christoffer says "remember this in my second brain," file it to the most
  specific relevant page and log it.
- If you struggle to navigate the wiki, that's a signal to improve this file.


---

# Second Brain Integration

## Purpose

This workspace is part of a larger personal knowledge system.

Think of it as three connected layers:

1. **about-me.md** — long-term operating manual. Stable. Defines who Christoffer is, how he works, how decisions are made, and how you should collaborate.

2. **memory.md** — working memory. Frequently updated. Tracks active projects, decisions, progress and changelog.

3. **Second Brain (Obsidian wiki)** — long-term knowledge. Contains durable information about work, home, finances, tools, vehicles, learning, health, faith, ideas and research.

These layers complement each other. Do not duplicate them unnecessarily.

---

## Using external context

Before answering substantial questions or processing new information:

- Read `about-me.md` when working style, priorities or long-term preferences matter.
- Read `memory.md` when project status or recent decisions matter.
- Read the Second Brain when durable knowledge or historical context matters.

Treat them as separate sources with different purposes.

---

## Knowledge Routing

When processing information, decide where it belongs.

### about-me.md

Store only long-term operating principles.

Examples:

- working style
- communication preferences
- decision framework
- career direction
- creative standards

Avoid project status or temporary notes.

### memory.md

Store:

- active project status
- recent decisions
- changelog
- open work

Overwrite current project status instead of duplicating it.

### Second Brain

Store durable knowledge.

Examples:

- insurance
- mortgage
- manuals
- product knowledge
- AI research
- workflows
- meeting conclusions
- personal frameworks
- lessons learned

If information will probably still be useful in a year, it usually belongs here.

---

## Sync workflow

When Christoffer asks to sync:

1. Identify new or changed files.
2. Read markdown, PDFs, images and documents when possible.
3. Classify each item.
4. Create or update knowledge pages.
5. Prefer updating existing pages over creating duplicates.
6. Add useful internal links.
7. Detect contradictions and stale information.
8. Update indexes where appropriate.
9. Produce a concise sync report including:
   - new sources
   - pages created
   - pages updated
   - links added
   - issues found
   - suggested next actions

Never respond only with "Sync complete".

---

## PDF handling

Treat PDFs as source material.

Do not leave valuable information trapped inside documents.

Extract:

- key facts
- important dates
- costs
- obligations
- limitations
- risks
- review dates
- decisions

Create or update Markdown pages that summarize the practical knowledge while preserving the original PDF as the authoritative source.

---

## Writing principles

The wiki should read like a practical handbook.

Prefer:

- concise writing
- tables
- checklists
- timelines
- important numbers
- decisions
- actionable notes

Avoid:

- generic summaries
- unnecessary prose
- repeating the source document
- AI clichés

The goal is fast retrieval, not impressive writing.
