# UPSC CSE Prep – Knowledge Vault

> A structured, interlinked, version-controlled vault for UPSC CSE preparation. Built using **Obsidian + Markdown + Git**, designed for long-term revision, deep linking, and multi-source knowledge integration.

---

## Overview

This repository functions as a personal **UPSC knowledge system**, containing:

- **Static Notes** from NCERTs, reference books, and standard sources
- **Current Affairs** with daily, weekly, and topic-wise breakdowns
- **Interlinked Concepts** using Obsidian WikiLinks
- **MOC Pages (Maps of Content)** for hierarchical navigation
- **Templates** to standardize note-taking
- **Practice** folders for PYQs, answer writing, and mock work

The goal is simple: **Combine theory, GS, and current affairs into one cohesive linked knowledge base.**

---

### Why this structure works

- Shallow hierarchy keeps graph clean
- MOCs centralized in **00-Index**
- Static notes isolated from Current Affairs
- Templates grouped for automation
- Assets kept out of graph clutter
- Git-friendly and future-proof
- Easy for IDE or AI agents to operate on

---

## How to Use the Vault

### On Desktop (Windows/Linux/macOS)

1. Open vault in Obsidian
2. Start navigating from `00-Index/`
3. Use templates for creating consistent notes
4. Link everything using `[[WikiLinks]]`
5. Keep Current Affairs in `20-Current-Affairs/`
6. Use `10-Static/` for evergreen notes

Commit routinely:

```
git add .
git commit -m "Updated notes"
git push
```

### On Android

- Great for reading and light edits
- Sync via Obsidian Git plugin or GitJournal
- Avoid heavy reorganizing
- Perfect for adding CA notes

---

## Graph Map Philosophy

Goal is **clusters, not chaos**.

- MOCs form top-level hubs
- Static notes form dense GS clusters
- CA links back to fundamentals
- Practice connects across subjects

This creates a concept web ideal for Mains-oriented revision.

---

## Templates Included

Located in: `00-Index/_templates/`

### `_template-topic.md`

For static GS notes.

### `_template-ca.md`

For Current Affairs.

### `_template-moc.md`

For Maps of Content.

---

## Automation & AI Integration

The `.ai/rules.md` file supports:

- Auto-generating folder trees
- Naming consistency
- Template insertion
- Auto-linking related notes
- Running summarisation tools

Your vault is fully AI-ready.

---

## Contributing

1. Fork repo
2. Create branch
3. Commit
4. Open PR

---

## License

MIT License
