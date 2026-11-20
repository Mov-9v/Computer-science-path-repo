# Summary & Formatting Rules (قواعد تنسيق وبناء الملخصات)

This document defines the standard rules for building, organizing, and formatting all study-guide chapters in this repository.

## 1. Repository & Folder Structure
- **Root (`Computer science path repo/`):**
  - `Subjects , books and notes/` — Study materials, books, and Markdown chapters organized by subject/book.
  - `Exams and Projects/` — Practice exams, quizzes, and coding projects.
- **Book/Subject Folder (`Subjects , books and notes/C++ Reference Guide/`):**
  - **Chapter Files:** Named `Chapter XX - <Chapter Title>.md` (e.g., `Chapter 01 - Computing Foundations & C++ Build Pipeline.md`).
  - **Assets Folder:** `assets/` next to the chapter files, containing only diagrams, flowcharts, cover art, and illustrations.
  - **No Unused Assets:** Code or text-only screenshots must be transcribed into Markdown/code blocks and removed from `assets/`.

## 2. Text Review, Phrasing & Restructuring
- **Active Editing & Rewriting Authority:** Always review raw input text and you have full authority to refine, polish, and rewrite phrasing (into clean, formal engineering Arabic/English matching the rest of the guide) rather than pasting colloquial or rough text verbatim:
  - Convert inline enumerations and `Term: description` definitions into clean bulleted (`-`) or numbered (`1.`) lists.
  - Convert standalone sub-topic lines into `####` subheadings.
  - Group related points under clear subheadings and tables, and remove any conversational/chat filler or duplicated blocks.
- **Bold Technical Terms:** Highlight key concepts, definitions, and bilingual technical terms (e.g., `**المترجم (Compiler)**`, `**الذاكرة العشوائية (RAM)**`) in **bold**.
- **No Full-Paragraph Bold:** Do not wrap entire multi-line prose paragraphs in `**...**`.

## 3. Colored Headings & Typography
- Use `#` for chapter titles, `##` for major sections, `###` for subsections, and `####` for subtopics.
- **Heading Colors:** Apply consistent accent colors to headings using inline HTML `<span>` (rendered in local Markdown viewers/IDEs while keeping GitHub anchor links functional):
  - `#` (Chapter Title): `#1B4F72` (Deep Navy)
  - `##` (Major Section): `#2874A6` (Steel Blue)
  - `###` (Subsection): `#117864` (Teal)
  - `####` (Subtopic): `#6C3483` (Muted Purple)
- **Notes & Callouts:** Format notes as blockquotes (`> **Note:** ...` or `> **ملاحظة:** ...`).
- **Tables:** Use standard GitHub-Flavored Markdown tables (`| col1 | col2 |`).

## 4. Header & Table of Contents
- Every chapter starts with a clean title/cover (if available) followed immediately by a well-organized `## Table of Contents` section with hierarchical indentation and working GitHub-compatible anchor links (`[Section Title](#section-title)`).

## 5. Page System (نظام الصفحات)
- Organize content into balanced pages separated by a horizontal rule (`---`) and a plain-text page marker (`**Page X**`).
- **Target Page Size:** Roughly **40–60 lines** per page (splitting only between complete paragraphs, lists, tables, or code blocks — never mid-table or mid-code-block).
- **Avoid Tiny Pages:** Merge small fragments so no content page is overly short (except Cover and Table of Contents).

## 6. Strict No-Emoji Policy
- Do **not** use emojis anywhere in headings, page markers, callouts, lists, or tables.

## 7. Images & Centering
- Keep only genuine diagrams, architecture charts, and illustrations in `assets/`.
- **Center Alignment:** Every image must be centered using HTML `<p align="center">`:
  ```html
  <p align="center">
    <img src="assets/image_name.png" alt="Descriptive alt text" />
  </p>
  ```

## 8. Code & Algorithms
- Never leave code snippets or algorithm listings as screenshots.
- Transcribe all C++ code into fenced `cpp` code blocks (` ```cpp ... ``` `).
- Transcribe algorithm examples into structured Markdown (Problem Analysis + numbered Algorithm steps with inline code `` `...` ``).
