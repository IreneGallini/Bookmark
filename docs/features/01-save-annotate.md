---
id: 01
title: Save & annotate
status: wireframed
figma: ["https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-2"]
wireframes: ["../wireframes/01-save-annotate.png"]
code: []
---

# 01 — Save & annotate

![Save & annotate wireframe](../wireframes/01-save-annotate.png)

## Problem
Research happens in the browser: papers, articles, docs. Saving and annotating them usually means switching tools and losing context, so ideas never get captured.

## User stories
- As a researcher, I want to save the page I'm reading to a project in one click, so it doesn't get lost in my tabs.
- As a researcher, I want to highlight a passage and attach a note to it, so I remember why it mattered.
- As a researcher, I want to tag a save, so I can find it again and connect it to related work.
- As a researcher, I want to send a page to my working queue, so I can read it properly later.

## Wireframe walkthrough (frame `1:2`)
- **Page content area:** the user selects text, the highlight appears, and an **"Add a note"** popover with a **Save note** button opens next to the selection.
- **Extension side panel** (right side, 344px wide):
  - "Save this page"
  - **Project** dropdown (e.g. "Reaction prediction lit review ▾")
  - **Tags** as chips (e.g. `chemistry`, `ML`)
  - **Highlighted passage** preview
  - **Save to queue** button (the primary action)

## Acceptance criteria
- [ ] The extension saves the URL, title and metadata (authors, venue, year, DOI when present) of the current page.
- [ ] The user can choose an existing project or create a new one from the panel.
- [ ] The user can add and remove tags, with autocomplete from existing tags.
- [ ] Selecting text on a page creates a highlight that the user can attach a note to.
- [ ] Highlights are anchored, so they show up again when the user revisits the page.
- [ ] "Save to queue" adds the item to the working queue ([02](02-working-queue.md)).
- [ ] Everything saved in the extension shows up in the web app right away.

## Out of scope (for now)
- PDF annotation inside the browser's PDF viewer (see [05](05-ingestion-integrations.md))
- Offline saving

## Open questions
- Which browser comes first: Chrome only (MV3), or Chrome and Firefox?
- How should highlights be anchored? Options: text quote + position (like the W3C Web Annotation model) or DOM ranges.
- Should the side panel use Chrome's `sidePanel` API or a page overlay that the extension injects?

## Changelog
- 2026-10-12 — spec created from the wireframe
