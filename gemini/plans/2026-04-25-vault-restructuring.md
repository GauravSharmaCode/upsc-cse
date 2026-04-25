# Design Spec: Vault Restructuring & PYQ Analysis Staging
**Date:** 2026-04-25
**Branch:** `feature/PYQ-Analysis`

## 1. Overview
The goal is to organize 'random' root files, enforce naming conventions, update subject MOCs, and stage all pending content (including PYQ analyses and new Polity notes) into a new branch for submission.

## 2. Structural Changes
### 2.1 File Cleanup
- **Delete:**
  - `Untitled.base`
  - `Untitled 1.base`
  - `Untitled 2.base`
- **Move & Rename:**
  - `Alternative Powertrains.md` → `10-Static/Science-Alternative-Powertrains.md`
  - `10-Static/Polity-President of India.md` → `10-Static/Polity-President-of-India.md`

### 2.2 Index & MOC Updates
- **New MOC:** `00-Index/MOC-Science-Technology.md`
- **Updated MOCs:**
  - `00-Index/MOC-GS.md`: Add Science & Technology section.
  - `00-Index/MOC-Polity.md`: Link new Polity notes:
    - `Polity-Constitution-Making`
    - `Polity-Fundamental-Rights`
    - `Polity-Parliament`
    - `Polity-Preamble`
    - `Polity-President-of-India`
  - `00-Index/MOC-Current-Affairs.md`: Link `2026-03-28 - The Hindu - Governor-Power-to-Withhold-Assent.md`.

## 3. Link Consistency
- Update `40-Practice/PYQ-2025/PYQ-2025-Science-Technology.md`:
  - `[[Alternative Powertrains]]` → `[[Science-Alternative-Powertrains]]`

## 4. Git Operations
- Create branch `feature/PYQ-Analysis`.
- Stage all valid tracked and untracked files:
  - `.obsidian/` (config changes)
  - `00-Index/`
  - `10-Static/`
  - `20-Current-Affairs/`
  - `40-Practice/`
  - `assets/`
- Commit with a descriptive message.
- Push to origin.

## 5. Success Criteria
- [ ] No notes or 'base' files remaining in the root directory.
- [ ] All Polity notes follow the hyphenated naming convention.
- [ ] MOC-GS includes Science & Technology.
- [ ] All untracked valid notes are staged and committed.
- [ ] WikiLinks are verified to point to the correct note names.
