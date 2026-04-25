# Plan: Restructure Graph Links for Keyword-Driven Connections

## Objective
To clean up the Obsidian graph view by removing hardcoded subject-to-subject links. The graph will transition to an organic structure: `MOC -> Topic -> Keyword -> Topic -> MOC`, allowing concepts to bridge subjects rather than rigid cross-referencing.

## Scope of Changes

1.  **Refactor MOC Files (`00-Index/`)**:
    *   Remove the "Related MOCs" section from all Subject MOCs (e.g., `MOC-Polity`, `MOC-History`, `MOC-Geography`, `MOC-Economy`, `MOC-Environment`, `MOC-Current-Affairs`).
    *   *Note*: `MOC-GS` will be maintained as the central root hub linking to the individual Subject MOCs, but peer-to-peer MOC links will be removed.

2.  **Refactor Topic Files (`10-Static/`)**:
    *   Scan all static notes (e.g., `Polity-Historical-Background.md`).
    *   Remove cross-subject MOC links from the "Links" section (e.g., remove `[[MOC-History]]`, `[[MOC-Current-Affairs]]` from Polity notes).
    *   Retain the link back to the parent MOC (e.g., `[[MOC-Polity]]`) to preserve the `MOC <-> Topic` relationship.
    *   Ensure cross-subject references use conceptual keywords (e.g., `[[Federalism]]`, `[[Decentralization]]`, `[[Nationalist Movement in India]]`) instead of broad subject MOCs.

3.  **Refactor Practice/PYQ Indexes (`40-Practice/`)**:
    *   Remove all `MOC-*` links from the bottom of `PYQ-Index-2025.md`.
    *   Ensure the index strictly links downward to individual PYQ subject files.

## Implementation Steps
1.  **MOC Cleanup**: Edit all `MOC-*.md` files in the `00-Index` folder to delete the "Related MOCs" list at the bottom.
2.  **PYQ Cleanup**: Edit `40-Practice/PYQ-2025/PYQ-Index-2025.md` to delete its "Links" section entirely.
3.  **Topic Cleanup**: 
    *   Search for all occurrences of `[[MOC-` within `10-Static/`.
    *   Remove any MOC links that don't represent the note's direct parent category.
    *   (Optional but recommended) In `Polity-Historical-Background.md`, ensure the conceptual links are prominent, as requested by the user.

## Verification
*   Open the Obsidian Graph view and confirm that `MOC-*` nodes are no longer clustering directly with each other (apart from connecting to `MOC-GS`).
*   Confirm that topics only bridge to other subjects through conceptual keyword nodes.