# Vault Restructuring & PYQ Analysis Staging Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Clean up the root directory, enforce naming conventions, update MOCs, and stage all content for the `feature/PYQ-Analysis` branch.

**Architecture:** Systematic cleanup followed by index updates to maintain vault integrity.

**Tech Stack:** Git, PowerShell/Bash, Markdown.

---

### Task 1: Root Directory Cleanup

**Files:**
- Delete: `Untitled.base`, `Untitled 1.base`, `Untitled 2.base`
- Move: `Alternative Powertrains.md` → `10-Static/Science-Alternative-Powertrains.md`

- [ ] **Step 1: Delete base files**
Run: `rm "Untitled.base", "Untitled 1.base", "Untitled 2.base"`

- [ ] **Step 2: Move Alternative Powertrains**
Run: `mv "Alternative Powertrains.md" "10-Static/Science-Alternative-Powertrains.md"`

- [ ] **Step 3: Commit cleanup**
Run: `git add . ; git commit -m "chore: cleanup root directory and move science note"`

---

### Task 2: Enforce Naming Conventions

**Files:**
- Rename: `10-Static/Polity-President of India.md` → `10-Static/Polity-President-of-India.md`

- [ ] **Step 1: Rename President of India note**
Run: `mv "10-Static/Polity-President of India.md" "10-Static/Polity-President-of-India.md"`

- [ ] **Step 2: Commit renaming**
Run: `git add . ; git commit -m "style: enforce hyphenation naming convention for Polity notes"`

---

### Task 3: Create Science & Technology MOC

**Files:**
- Create: `00-Index/MOC-Science-Technology.md`
- Modify: `00-Index/MOC-GS.md`

- [ ] **Step 1: Create Science MOC**
Create `00-Index/MOC-Science-Technology.md` with:
```markdown
---
tags: [moc, gs3]
sources: [Standard References]
---

# MOC — Science & Technology

Short: Tracking Science & Tech developments and static concepts.

## Static Notes
- [[Science-Alternative-Powertrains]]

## PYQ Analysis
- [[PYQ-2025-Science-Technology]]
- [[PYQ-2024-Science-Technology]]
```

- [ ] **Step 2: Update GS MOC**
Modify `00-Index/MOC-GS.md` to include:
```markdown
- [[MOC-Science-Technology]]
```

- [ ] **Step 3: Commit MOC changes**
Run: `git add . ; git commit -m "feat: add Science & Technology MOC"`

---

### Task 4: Update Existing MOCs for Untracked Content

**Files:**
- Modify: `00-Index/MOC-Polity.md`
- Modify: `00-Index/MOC-Current-Affairs.md`

- [ ] **Step 1: Update Polity MOC**
Add new links to `00-Index/MOC-Polity.md`:
- `[[Polity-Constitution-Making]]`
- `[[Polity-Fundamental-Rights]]`
- `[[Polity-Parliament]]`
- `[[Polity-Preamble]]`
- `[[Polity-President-of-India]]`

- [ ] **Step 2: Update Current Affairs MOC**
Add link to `2026-03-28 - The Hindu - Governor-Power-to-Withhold-Assent` in `00-Index/MOC-Current-Affairs.md`.

- [ ] **Step 3: Commit MOC updates**
Run: `git add . ; git commit -m "feat: link new Polity and CA notes to MOCs"`

---

### Task 5: Link Integrity & Staging

**Files:**
- Modify: `40-Practice/PYQ-2025/PYQ-2025-Science-Technology.md`

- [ ] **Step 1: Update Science PYQ Link**
Update `[[Alternative Powertrains]]` to `[[Science-Alternative-Powertrains]]` in `40-Practice/PYQ-2025/PYQ-2025-Science-Technology.md`.

- [ ] **Step 2: Stage all valid untracked files**
Run: `git add .obsidian/ 00-Index/ 10-Static/ 20-Current-Affairs/ 40-Practice/ assets/`

- [ ] **Step 3: Final commit and push**
Run: `git commit -m "feat: stage all pending content and restructure vault for PYQ analysis" ; git push origin feature/PYQ-Analysis`
