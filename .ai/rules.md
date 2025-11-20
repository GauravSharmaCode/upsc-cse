# UPSC Obsidian Vault: Structure, Templates, and Setup Guide

This file is a single-source setup guide you can drop into your vault. It contains folder structure, naming conventions, templates (MOC, topic, CA), frontmatter examples, PowerShell helpers, and a short migration plan.

---

## 1 — Recommended top-level folders

Create these folders at the repository root (shallow, intentional):

```
00-Index/
10-Static/
20-Current-Affairs/
30-Optional/
40-Practice/
assets/
.obsidian/   # Obsidian app files (hide from graph / ignore in git if you want)
```

- `00-Index/` — Maps-of-Content (MOCs), vault README, roadmap.
- `10-Static/` — Atomic topic notes (one file per idea/topic).
- `20-Current-Affairs/` — Date-prefixed CA notes.
- `30-Optional/` — Optional subject notes (shallow per subject).
- `40-Practice/` — Answer-writing, essay drafts, PYQs, prelims MCQs.
- `assets/` — PDFs, images, charts (exclude from graph view).

---

## 2 — Naming conventions (automation-friendly)

- Static topic files: `Subject-Subtopic.md` (e.g., `Polity-Fundamental-Rights.md`)
- Current Affairs files: `YYYY-MM-DD - Source - Short-Title.md` (e.g., `2025-11-18 - The Hindu - Delhi Water Dispute.md`)
- MOC files: `MOC-Polity.md`, `MOC-History.md`
- Templates: `_template-topic.md`, `_template-ca.md`, `_template-moc.md`

Why: predictable names make script-based linking, search, and alias generation reliable.

---

## 3 — Obsidian recommended settings (quick)

1. Settings → Files & Links → **Use markdown links** (or auto-convert wikilinks to MD links).
2. Graph view → Excluded files/folders: add `assets/*` and `.obsidian/*`.
3. Keep `aliases` in frontmatter so `[[WikiLinks]]` resolve regardless of file path.

These settings keep GitHub readable while preserving Obsidian's link magic.

---

## 4 — Maps of Content (MOC)

Create one MOC per major subject in `00-Index/`. MOCs are hub nodes that the graph loves.

Examples to create:

- `00-Index/MOC-GS.md`
- `00-Index/MOC-Polity.md`
- `00-Index/MOC-History.md`
- `00-Index/MOC-Geography.md`
- `00-Index/MOC-Current-Affairs.md`

MOCs contain short summaries and curated `[[links]]` to important notes and revision summaries.

---

## 5 — Frontmatter & Aliases (stable wikilinks)

Use YAML frontmatter on key notes so `[[Friendly Name]]` always resolves even if file name changes.

Example frontmatter:

```yaml
---
aliases:
  - Fundamental Rights
  - FR
tags:
  - gs1
sources:
  - Laxmikanth
---
```

Obsidian will resolve `[[Fundamental Rights]]` to that file even if it lives in `10-Static/`.

---

## 6 — Templates (save these as `_template-*.md` in a templates folder)

### `_template-topic.md`

```md
---
aliases: []
tags: []
sources: []
---

# {{title}}

**Summary (2–3 lines)**

## Key points

-

## Details / Notes

-

## Links

- [[MOC-{{subject}}]]
- [[Related-Topic]]

## Sources

-
```

### `_template-ca.md`

```md
---
tags: [current-affairs]
date: { { date } }
source: { { source } }
---

# {{date}} — {{source}} — {{title}}

## **Summary**

## **Why it matters**

**Linked topics**

- [[Polity-Federalism]]
- [[Economy-Inflation]]

## **Source link / notes**
```

### `_template-moc.md`

```md
---
tags: [moc]
---

# MOC — {{subject}}

Short: One-line purpose.

## Core topics

- [[Subject-Topic-A]]
- [[Subject-Topic-B]]

## Revision notes

- [[Subject-Revision-Summary]]

## Important links / timelines

- [[YYYY-MM-DD - Source - Event]]

## Related MOCs

- [[MOC-GS]]
```

---

## 7 — Example files (drop these directly)

**`00-Index/README.md`**

- Index pointing at MOCs.

**`00-Index/MOC-Polity.md`**

- MOC file with curated links to `Polity-*` notes and recent CA files.

**`10-Static/Polity-Fundamental-Rights.md`**

- A topic file using aliases frontmatter and `[[links]]` to MOCs and related topics.

(Exact example content is saved in templates above.)

---

## 8 — Flattening / Migration steps

**Manual (recommended)**

1. Open the vault in Obsidian.
2. Drag the deep file (e.g., `Geography/Climate/Atmosphere.md`) into `10-Static/` or rename to `10-Static/Geography-Atmosphere.md` using Obsidian's file explorer. Obsidian will update internal links.

**Scripted (use with care)**

- If automation is required, write a script to move files and to add/update aliases in frontmatter. Test on a copy first.

---

## 9 — PowerShell helpers

**Generate folder-only tree (markdown-ish):**

```powershell
Get-ChildItem -Directory | ForEach-Object { "- $_.Name" } > structure.md
```

**Full tree to file (old-school):**

```powershell
tree /A > tree.txt
```

---

## 10 — Git tips

- Add `.obsidian/` to `.gitignore` if you don’t want to track workspace state.
- Commit often with meaningful messages.
- Use branches only if you plan big structural reorgs; otherwise keep it simple.

Suggested initial commit message:

```
chore: initial commit – setup UPSC Obsidian vault with structure + templates
```

---

## 11 — Quick checklist to run now

- [ ] Create folders (root layout above)
- [ ] Add `_template-*.md` in a `00-Index/_templates/` folder
- [ ] Create MOC files in `00-Index/`
- [ ] Create 3–5 seed topic notes in `10-Static/` using the topic template
- [ ] Exclude `assets/` and `.obsidian/` from graph
- [ ] Commit and push to your Git remote

---

Drop this file into your vault root and point your IDE/AI at it. It’s a precise spec — automated tools will understand it and can create the MOCs, templates, and move files accordingly.
