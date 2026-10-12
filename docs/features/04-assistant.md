---
id: 04
title: AI assistant ("second brain")
status: idea
figma: []
wireframes: []
code: []
---

# 04 — AI assistant ("second brain")

> No wireframe yet. **Next design step:** decide where the assistant lives: a side panel, a command bar (⌘K), or inline in the block view.

## Problem
A library of saved items and notes is only useful if the user can reason over it. Users want help organizing, brainstorming, and finding out what already exists.

## User stories
- As a researcher, I want to ask "what have I saved about X?" and get an answer that cites my own items.
- As a researcher, I want the assistant to suggest how to reorganize my notes (merge duplicates, cluster items into themes, suggest tags).
- As a researcher, I want to brainstorm from a note and have the assistant bring up connected ideas from my library.
- As a researcher, I want to ask "has this been done before?" and have the assistant search outside my library (e.g. Semantic Scholar, arXiv) for prior work.

## Acceptance criteria
- [ ] Answers cite the specific items and highlights they draw on, and clicking a citation opens the source.
- [ ] Suggested reorganizations are proposals that the user accepts or rejects, never silent edits.
- [ ] "Has this been done before" results are clearly marked as external sources and can be saved into the library.
- [ ] The assistant only uses the current workspace's data, and respects sharing permissions ([06](06-collaboration.md)).

## Technical notes
- Retrieval over embeddings of items, highlights and notes. This is the same index that powers semantic connections in [03](03-connections.md).
- LLM: Claude through the Anthropic API.

## Open questions
- Should the assistant chat be saved as a note in the library?
- What does it cost per user, and should there be rate limits on the free tier?

## Changelog
- 2026-10-12 — spec created from the ideation notes
