---
id: 06
title: Workspaces, sharing & live collaboration
status: idea
figma: []
wireframes: []
code: []
---

# 06 — Workspaces, sharing & live collaboration

> No wireframe yet. **Next design step:** a share dialog, presence indicators (avatars and cursors), and a workspace switcher in the sidebar.

## Problem
Research is often done by a team, such as a lab or a study group. Shared projects let people see what others are reading and build on each other's annotations.

## User stories
- As a lab member, I want a shared workspace where saved items, highlights and notes are visible to the whole team.
- As a user, I want to share a single project with a link (view or edit).
- As a collaborator, I want to see who else is viewing a note and watch their edits appear live.
- As a collaborator, I want to see who wrote each annotation.

## Acceptance criteria
- [ ] Workspaces have members with roles (owner, editor, viewer).
- [ ] A project can be shared with a link, with view or edit permission.
- [ ] Concurrent edits to a note merge without conflicts.
- [ ] Presence shows the other users active in the same item.
- [ ] Every annotation and note shows its author.

## Technical notes
- Use a CRDT (e.g. Yjs) for real-time note editing.

## Open questions
- Are personal and shared items mixed, or kept in separate workspaces?
- Should comments be a separate thing from annotations?

## Changelog
- 2026-10-12 — spec created from the ideation notes
