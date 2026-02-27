# Books Module Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Add a bilingual Books module to homepage with two sub-sections (Monographs/Translations) and item-level one-sentence descriptions.

**Architecture:** Reuse existing card/list styling (`card`, `item-list`, `item-note`) used by Publications and Packages. Add two new card sections (zh/en) in `index.md`, each with `h3` sub-headings and linked book entries.

**Tech Stack:** Jekyll Markdown page (`index.md`) with inline HTML/CSS.

---

### Task 1: Insert Chinese Books section

**Files:**
- Modify: `index.md`

1. Add `<section class="card" data-lang="zh">` titled `书籍`.
2. Add two sub-sections: `专著` and `译著`.
3. For each book, add linked title and one-sentence Chinese intro using `<p class="item-note">`.

### Task 2: Insert English Books section

**Files:**
- Modify: `index.md`

1. Add `<section class="card" data-lang="en">` titled `Book`.
2. Add two sub-sections: `Monographs` and `Translations`.
3. For each book, add linked title and one-sentence English intro using `<p class="item-note">`.

### Task 3: Keep style consistency

**Files:**
- Modify: `index.md`

1. Reuse existing `.item-list` and `.item-note` classes.
2. If needed, add minimal `h3` style matching current typography.

### Task 4: Verify structure

**Files:**
- Modify: `index.md`

1. Check both language sections are wrapped by `data-lang`.
2. Ensure all four links appear in both zh/en sections.
3. Confirm section placement before Links & Contact.
