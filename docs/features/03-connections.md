---
id: 03
title: Connections (block + graph view)
status: wireframed
figma:
  - "https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-88"
  - "https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-108"
wireframes: ["../wireframes/03a-connections-block.png", "../wireframes/03b-connections-graph.png"]
code: []
---

# 03 — Connections (block view + graph view)

| Block view (`1:88`) | Graph view (`1:108`) |
|---|---|
| ![Block view](../wireframes/03a-connections-block.png) | ![Graph view](../wireframes/03b-connections-graph.png) |

## Problem
The value of a second brain comes from links between ideas: shared concepts, citations, similar annotations. These connections should appear on their own, and each one should say *why* two items are related.

## User stories
- As a researcher, when I open a note I want to see related items and the reason each is related, so I can find connections I'd otherwise miss.
- As a researcher, I want to switch to a graph that shows how an item sits within my project.
- As a researcher, I want to see citations between my items and to concepts outside my library.

## Wireframe walkthrough
- **03A Block view:** an open note (title, project, body) with a **Related** list underneath. Each related card gives the **reason** for the link:
  - "Shares tag: steric effects"
  - "Cited in your annotation above"
  - "Same project: lit review"
  - "You annotated a similar passage" (semantic similarity)
- **03B Graph view:** the current item at the center, with the same related items as nodes around it, joined by edges.

## Connection types (from the wireframe)
| Type | Source | Needs AI? |
|---|---|---|
| Shared tag | tags | no |
| Same project | project membership | no |
| Explicit reference / citation | links and mentions in notes; DOIs/references in papers | no (parsing only) |
| Similar passage / concept | embeddings of highlights and notes | yes |

## Acceptance criteria
- [ ] Opening an item shows a Related list, and every entry names the reason for the link.
- [ ] Block view and graph view use the same connection data and can be toggled.
- [ ] Clicking a node or card opens that item.
- [ ] The graph handles at least a few hundred nodes per project without lag.

## Decision needed: block, graph, or both?
This is the main UI question. Record the decision and the reasoning here once it's made.
- **Option A:** block view by default, graph as a secondary "zoom out" view
- **Option B:** graph as the main canvas, blocks open in a side panel
- **Decision:** _TBD_

## Open questions
- Do users create links by hand (e.g. `[[wikilinks]]` like Obsidian), or only automatically?
- Should there be a minimum similarity score before a semantic link appears?

## Changelog
- 2026-10-12 — spec created from the wireframes
