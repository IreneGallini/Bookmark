# Roadmap — next steps

These are the next steps for the project, in order. Check items off as they're done and add the date. Record decisions in the relevant spec or in `CLAUDE.md`, and keep this file as the checklist.

_Last updated: 2026-10-12_

## 1. Put the repo on GitHub
- [ ] Create a GitHub repository and push `main`
- [ ] Check that the README wireframe gallery and `.github/pull_request_template.md` render correctly
- [ ] Open one GitHub issue per feature (01–06), each linking its spec and Figma frame
- [ ] _Optional:_ create a GitHub Project board with columns that match the statuses: idea / wireframed / building / shipped

## 2. Choose the tech stack
Decide each item, then record the choices in the **Tech stack** section of `CLAUDE.md`.
- [ ] **Web app frontend:** e.g. React + Vite, or Next.js
- [ ] **Browser extension:** Chrome MV3 only, or cross-browser (e.g. WXT / Plasmo); side panel API vs. injected overlay (see [01](features/01-save-annotate.md) open questions)
- [ ] **Backend + database:** e.g. Supabase/Postgres, Firebase, or a custom API; needs to store embeddings (e.g. pgvector) for [03](features/03-connections.md) and [04](features/04-assistant.md)
- [ ] **Auth**
- [ ] **Real-time collaboration:** e.g. Yjs, Liveblocks ([06](features/06-collaboration.md))
- [ ] **LLM + embeddings provider** ([04](features/04-assistant.md))
- [ ] **Graph rendering library:** e.g. React Flow, Cytoscape, d3-force ([03](features/03-connections.md))
- [ ] After the stack is chosen: add the build/test/dev commands to `CLAUDE.md`

## 3. Decide block view vs. graph view
The main UI question. Compare frames `1:88` and `1:108`.
- [ ] Choose: A) blocks by default with graph as a secondary view, B) graph as the main canvas with blocks in a side panel, or something else
- [ ] Write the decision and the reasoning in the **Decision** section of [03-connections.md](features/03-connections.md)
- [ ] Update the Figma frames to match the decision

## 4. Wireframe the features that have no screens yet
For each one: design the frame in Figma, export it to `docs/wireframes/`, link it in the spec and in `FEATURES.md`, add it to the frame map in `CLAUDE.md`, and set the status to `wireframed`.
- [ ] **04 Assistant:** where it lives (side panel / ⌘K command bar / inline), and how answers show their citations
- [ ] **05 Ingestion & integrations:** connect-a-source flow (pick a source, authorize, preview, import) and the PDF reader with annotations
- [ ] **06 Collaboration:** share dialog, presence (avatars/cursors), workspace switcher

## 5. Clean up the Figma file (before building UI)
- [ ] Turn the repeated elements into Figma components: queue card, tag chip, note popover, sidebar nav item, related-item card, graph node
- [ ] Define colors, type and spacing as Figma variables, so they can be exported to a design-tokens file in the repo
- [ ] _Later, optional:_ Figma Code Connect to link components to code (needs a paid Figma Organization or Enterprise plan)

## 6. Answer the open questions in each spec
Go through the **Open questions** section of each spec and either answer each question or postpone it on purpose.
- [ ] [01 Save & annotate](features/01-save-annotate.md)
- [ ] [02 Working queue](features/02-working-queue.md)
- [ ] [03 Connections](features/03-connections.md)
- [ ] [04 Assistant](features/04-assistant.md)
- [ ] [05 Ingestion & integrations](features/05-ingestion-integrations.md)
- [ ] [06 Collaboration](features/06-collaboration.md)

## 7. Define the MVP and start building
- [ ] Pick the MVP features. A suggested first loop: **01 Save & annotate → 02 Working queue → 03 Connections (no AI, using tags, projects and explicit links only)**
- [ ] Scaffold the app and the extension with the chosen stack
- [ ] Build the first feature. Set its spec status to `building` and fill in its `code:` paths
