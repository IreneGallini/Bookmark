---
id: 05
title: Ingestion & integrations
status: idea
figma: []
wireframes: []
code: []
---

# 05 — Ingestion & integrations

> No wireframe yet. **Next design step:** an import/connect screen (pick a source, authorize, preview, import) and a PDF reader view with annotations.

## Problem
Users' research already lives in other places: PDFs, Obsidian vaults, Notion, Google Drive, local folders. Bookmark has to bring that material in, or it starts out empty and nobody switches to it.

## User stories
- As a researcher, I want to upload or drag in a PDF and annotate it just like a web page ([01](01-save-annotate.md)).
- As an Obsidian user, I want to connect my vault so my notes and `[[links]]` become items and connections.
- As a Notion / Google Drive user, I want to import pages and docs from a chosen folder.
- As a researcher, I want to point Bookmark at a local folder and have its contents indexed.

## Sources (suggested build order)
| Source | Method | Notes |
|---|---|---|
| PDF upload | text extraction plus metadata (DOI, references) | prerequisite for citations in [03](03-connections.md) |
| Local folder | File System Access API in the browser | Chromium only |
| Obsidian | import the vault folder (markdown + wikilinks) | can reuse the local folder method |
| Notion | Notion API with OAuth | |
| Google Drive | Drive API with OAuth | |

## Acceptance criteria
- [ ] Uploaded PDFs are rendered, searchable and annotatable.
- [ ] Imported items keep a link back to the original and record their source.
- [ ] Re-syncing a source updates changed items without creating duplicates.
- [ ] Every connected source can be disconnected, which removes its imported data if the user chooses.

## Open questions
- One-way import, or two-way sync (e.g. write annotations back to Obsidian)?
- What file size and page limits should PDFs have?

## Changelog
- 2026-10-12 — spec created from the ideation notes
