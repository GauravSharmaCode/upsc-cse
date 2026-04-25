# GEMINI.md — UPSC CSE Vault Instructions for AI Agents

This file is the single source of truth for any AI agent working on this vault.
Read this before doing anything else.

---

## Who This Vault Belongs To

- **Name**: Gaurav Sharma
- **Target Exam**: UPSC CSE (Prelims → Mains)
- **Current Focus**: **Prelims** — fact accuracy, keyword recall, and conceptual clarity.
- **Mains Approach**: Basics only — structure and key arguments. No deep Mains answer-writing work yet.
- **Primary Study Sources**: Laxmikanth (Polity), NCERT Geography Class 11, standard GS references.

---

## Vault Directory Structure

```
00-Index/          → MOCs (Maps of Content) and templates
10-Static/         → Atomic topic notes (evergreen, source-based)
20-Current-Affairs/→ Date-prefixed news/CA notes
30-Optional/       → Optional subject (not active yet)
40-Practice/       → PYQs, answer writing
assets/            → PDFs, images (excluded from graph)
.ai/               → AI instructions (this file lives here conceptually)
```

---

## What's Done So Far

### 10-Static/ (completed notes)
- `Geography-Atmosphere.md` — Complete
- `Geography-Climate.md` — Shell (needs content)
- `Geography-Insolation.md` — Shell (needs content)
- `Polity-Historical-Background.md` — Complete (British Acts 1773–1947)

### 20-Current-Affairs/
- Empty. Not started yet.

### 40-Practice/
- Empty. Not started yet.

---

## Naming Conventions (strict)

- Static notes: `Subject-Subtopic.md` → e.g., `Polity-Fundamental-Rights.md`
- Current Affairs: `YYYY-MM-DD - Source - Short-Title.md`
- MOCs: `MOC-Subject.md`

---

## Frontmatter (required on every note)

```yaml
---
aliases: [Common Name, Acronym]
tags: [gs1, polity]   # gs1/gs2/gs3/gs4 based on paper
sources: [Laxmikanth, NCERT Class 11]
---
```

Tag reference:
- `gs1` → History, Geography, Society
- `gs2` → Polity, Governance, IR
- `gs3` → Economy, Environment, Science
- `gs4` → Ethics (not active)

---

## Note Quality Standard (Prelims-First)

Every completed static note must have:
1. **Summary** — 2–3 lines, plain language
2. **Key Facts** — bullet points; what Prelims MCQs can be formed from
3. **Details/Notes** — structured explanation with sub-headings
4. **Links** — back to MOC + at least one related note
5. **Sources** — where this came from

For Polity notes specifically:
- Include the relevant **Article number** wherever applicable
- Mention the **landmark SC case** if relevant
- Note if a provision was borrowed from another Constitution and which one

For Geography notes specifically:
- Tie to NCERT chapter
- Include diagrams/data references where the fact is numerical (lapse rate, layer heights, etc.)

---

## AI Agent Rules

When creating or editing notes in this vault:

1. **Prelims-first framing** — prioritize factual precision over narrative depth. Every sentence should be something that could be tested in a 1-mark MCQ.

2. **No unnecessary Mains elaboration** — don't write long analytical paragraphs unless explicitly asked. Keep notes dense and scannable.

3. **Always check existing files before creating new ones** — list `10-Static/` first. Don't duplicate.

4. **Fill shells before creating new notes** — if `Geography-Climate.md` is a shell, fill it before making `Geography-Monsoon.md`.

5. **WikiLink aggressively but accurately** — link to notes that exist or are likely to exist. Use `[[Note-Name]]` format. Don't invent links to non-existent notes without flagging them.

6. **Flag missing notes** — if a WikiLink points to something that doesn't exist yet, note it as `[[Note-Name]] ← TO CREATE`.

7. **Callout blocks for exam tips** — use `> [!TIP]` for memory tricks, `> [!NOTE]` for common exam traps, `> [!WARNING]` for frequently confused concepts.

8. **Don't touch `30-Optional/` or `40-Practice/`** — these are inactive. Don't add content unless explicitly asked.

---

## Current Priorities (updated 2026-03-28)

1. Create Polity notes: `Polity-Preamble.md`, `Polity-Union-Territories.md`, `Polity-Citizenship.md`.
2. Expand Geography: Create `Geography-Monsoon.md` and `Geography-Ocean-Currents.md`.
3. Practice: Start mapping PYQ 2025 questions in the newly created notes.
4. CA: Maintain daily note creation in `20-Current-Affairs/`.

---

## What Good Help Looks Like

- Reviewing a note: point out what's missing for Prelims, what's redundant, what needs a WikiLink
- Creating a note: follow the template, stay factual, link to MOC and related notes
- Filling a shell: add substance using NCERT/Laxmikanth-level facts, not deep analysis
- Suggesting next notes: based on what's missing in `10-Static/` relative to the Prelims syllabus
