---
id: 02
title: Working queue
status: wireframed
figma: ["https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-40"]
wireframes: ["../wireframes/02-working-queue.png"]
code: []
---

# 02 — Working queue / pick up where you left off

![Working queue wireframe](../wireframes/02-working-queue.png)

## Problem
Saved items pile up and turn into a graveyard. Users need a clear answer to "what was I doing, and what should I read next?"

## User stories
- As a researcher, I want to open Bookmark and see the item I was last working on, so I can resume right away.
- As a researcher, I want an ordered queue of things to read or process, so saving something leads to actually reading it.
- As a researcher, I want to filter by project or tag, so I can focus on one line of work.

## Wireframe walkthrough (frame `1:40`)
- **Left sidebar** (220px wide): Inbox, All projects, the active project (highlighted), Tags.
- **"Continue where you left off"** card at the top: the item title, a preview of the content, and a **Resume** button.
- **Queue** list: each card has a thumbnail, title, preview lines, a tag chip and a note count (e.g. "3 notes").

## Acceptance criteria
- [ ] The home view shows the most recently active item, and Resume reopens it at the last scroll position and highlight.
- [ ] Items saved with "Save to queue" ([01](01-save-annotate.md)) appear in the queue.
- [ ] The user can drag to reorder the queue, mark an item done, or remove it.
- [ ] The sidebar filters the queue by Inbox, project or tag.
- [ ] Each card shows its tags and note count.

## Out of scope (for now)
- Automatic prioritization by the assistant (see [04](04-assistant.md))

## Open questions
- Should the queue be the same across projects, or separate for each project?
- What counts as "left off" (last opened, last annotated, or last edited), and does it sync across devices?
- Is "Inbox" the place for items with no project yet?

## Changelog
- 2026-10-12 — spec created from the wireframe
