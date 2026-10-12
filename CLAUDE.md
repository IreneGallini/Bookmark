# Bookmark

A web-based research workspace: a browser extension plus a web app for saving and annotating sources, a working queue, a connections graph, and an AI assistant. The project is in the **ideation/design phase**, and no app code exists yet.

## Source of truth
- **What to build:** `docs/FEATURES.md` (the index) and `docs/features/NN-*.md` (one spec per feature).
- **How it looks:** Figma file `hzWrF1m4Lnz5pIspJj8gKa` ([Bookmark — Wireframes](https://www.figma.com/design/hzWrF1m4Lnz5pIspJj8gKa/Bookmark-%E2%80%94-Wireframes)).
- **What's next:** `docs/ROADMAP.md`. Check items off as they're done.
- `docs/wireframes/*.png` are static snapshots for reading on GitHub. Figma is always the current version.

## Feature ↔ Figma frame map
| Feature spec | Figma node | Snapshot |
|---|---|---|
| `docs/features/01-save-annotate.md` | `1:2` | `docs/wireframes/01-save-annotate.png` |
| `docs/features/02-working-queue.md` | `1:40` | `docs/wireframes/02-working-queue.png` |
| `docs/features/03-connections.md` | `1:88` (block), `1:108` (graph) | `docs/wireframes/03a-…`, `03b-…` |
| `docs/features/04-assistant.md` | — | — |
| `docs/features/05-ingestion-integrations.md` | — | — |
| `docs/features/06-collaboration.md` | — | — |

## Workflow rules
1. **Before building UI for a feature,** read its spec. Then use the Figma MCP (`get_design_context` / `get_screenshot` with the file key and node above) to get the current design. Don't work only from the PNG, because it may be out of date.
2. **When a feature changes status** (`idea → wireframed → building → shipped`), update both the spec's frontmatter and the table in `docs/FEATURES.md`. Add a line to the spec's Changelog.
3. **When code for a feature is added,** list its main paths in the spec's `code:` frontmatter and in the Code column of `FEATURES.md`.
4. **When a new Figma frame is added,** export it to `docs/wireframes/NN-name.png`, link it in the spec and in `FEATURES.md`, and add it to the map above.
5. **New features** start by copying `docs/features/_TEMPLATE.md`.
6. Record product decisions (e.g. block view vs. graph view) in the relevant spec's "Decision" section, not only in chat or commits.

## Tech stack
_TBD. Fill this in when it's chosen (frontend, extension framework, backend/DB, auth, LLM provider)._

## Commands
_TBD. Add build/test/dev commands once the app is scaffolded._
