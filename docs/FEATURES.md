# Features

This file is the index for every feature in the project. Each feature has a spec in `docs/features/`. The specs say **what** to build. The Figma frames show **how it looks**.

Figma file: [Bookmark — Wireframes](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes)

**Status values:** `idea` → `wireframed` → `building` → `shipped`

| # | Feature | Spec | Figma frame | Wireframe | Status | Code |
|---|---------|------|-------------|-----------|--------|------|
| 01 | Save & annotate (browser extension) | [spec](features/01-save-annotate.md) | [`1:2`](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-2) | [png](wireframes/01-save-annotate.png) | wireframed | — |
| 02 | Working queue / pick up where you left off | [spec](features/02-working-queue.md) | [`1:40`](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-40) | [png](wireframes/02-working-queue.png) | wireframed | — |
| 03 | Connections (block + graph view) | [spec](features/03-connections.md) | [`1:88`](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-88), [`1:108`](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes?node-id=1-108) | [block](wireframes/03a-connections-block.png), [graph](wireframes/03b-connections-graph.png) | wireframed | — |
| 04 | AI assistant ("second brain") | [spec](features/04-assistant.md) | — | — | idea | — |
| 05 | Ingestion & integrations (PDF, Obsidian, Notion, Drive, local) | [spec](features/05-ingestion-integrations.md) | — | — | idea | — |
| 06 | Workspaces, sharing & live collaboration | [spec](features/06-collaboration.md) | — | — | idea | — |

## Open product question
**How should everything connect in the UI: blocks, a graph, or both?** Frames 03A and 03B test this. The decision belongs in [03-connections.md](features/03-connections.md).
