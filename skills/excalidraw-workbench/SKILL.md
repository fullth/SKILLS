---
name: excalidraw-workbench
description: Create or revise editable Excalidraw diagrams, including architecture, workflows, and design discussions. Use when the user requests an Excalidraw canvas or editable Excalidraw deliverable.
---

# Excalidraw workbench

Create diagrams that make the requested relationships and decisions easy to follow. Separate source-confirmed behavior, user-provided assumptions, proposals, and unknowns using labels as well as color. Include concise, traceable sources when diagramming an existing system; do not treat source inspection as runtime verification.

## Setup

Prefer an available Excalidraw MCP or CLI connection. Inspect the existing scene before changing it. If a compatible tool is unavailable, consult the official project instructions at https://github.com/yctimlin/mcp_excalidraw. Its `mcp-excalidraw-server` package offers a local canvas and CLI; check its current prerequisites and installation instructions before setup. Keep the server bound to loopback unless the user explicitly requests network access and its security implications are understood. Do not change account, server, or agent configuration without authorization.

## Draw and verify

1. Establish the scope and audience. For a process, show the trigger, sequence, meaningful decisions, outcomes, and relevant boundaries. For architecture or design, show the relationships supported by the evidence and label unresolved connections.
2. Preserve existing work. Do not clear or replace a shared canvas, overwrite an unrelated file, or import a scene in replace mode without an explicit request. When appending, leave a clear gap and make the new section identifiable.
3. Bind arrows to shapes where supported and label non-obvious branches. Allow generous spacing and text padding. When changing font size, resize or reflow the entire affected layout, including bound labels, decision shapes, arrows, and captions; avoid relying on automatic wrapping alone.
4. Inspect a rendered screenshot at a readable scale. Check text clipping, line breaks, overlapping shapes, arrow endpoints, branch labels, and whether the meaning matches the source. Correct and recheck. Rendering and font metrics can differ across systems, especially for non-Latin text; report any unverified client-specific behavior.

## Save and synchronize

- When saving is requested, export an editable `.excalidraw` file and any requested images. Verify that the exported scene includes all intended elements and their bindings, excludes unrelated canvas content, and opens or renders as expected. Avoid treating PNG as the editable source.
- Canvas state, exported files, Git commits, and remote synchronization are separate. Do not assume automatic sync. Before an authorized remote update, confirm the repository, visibility, target branch, changed files, and absence of credentials or unintended private content; follow the user's applicable Git and security rules. Preserve unrelated files and verify the remote result after pushing.
- Never publish a private diagram, configure a public listener, or overwrite existing remote work merely because this skill is invoked.

Report where the user can access the result, what evidence supports it, what was actually verified, and whether it was saved or synchronized.
