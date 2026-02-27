# Agent Knowledge Base — How to Use

Each agent has a **knowledge folder** where you can add links, notes, and documents. When you ask that agent a question, they’ll use this content to give you better answers.

---

## Where to Add Content

| Agent | Folder |
|-------|--------|
| **Professor** | `agents/professor/knowledge/` |
| **Neo** | `agents/neo/knowledge/` |
| **Bruce** | `agents/bruce/knowledge/` |
| **Cena** | `agents/cena/knowledge/` |
| **Luffy** | `agents/luffy/knowledge/` |

---

## How to Add Content (No Technical Skill Required)

### Option 1: Edit the index file (easiest)

1. In Cursor, go to **Explorer** (left sidebar).
2. Open the agent folder (e.g. `agents` → `neo` → `knowledge`).
3. Open `index.md`.
4. Add links or notes using the format shown in the file.

**Links:** Copy-paste URLs into the Links table with a short description.  
**Notes:** Type your thoughts, rules, or principles in the Notes section.

### Option 2: Add markdown files

1. Create a new file in the agent’s `knowledge` folder (e.g. `agents/neo/knowledge/coding-tips.md`).
2. Write in plain text or markdown.
3. Add the filename to the index so the agent knows it’s there.

### Option 3: Book or article summaries

Instead of uploading full PDFs:

1. Create a new `.md` file in the agent’s knowledge folder.
2. Add a short summary, key points, or quotes.
3. This is usually more useful than raw documents.

---

## What to Add for Each Agent

| Agent | Good content to add |
|-------|---------------------|
| **Professor** | Decision frameworks, principles you want applied |
| **Neo** | Coding tutorials, docs, technical references |
| **Bruce** | Budget templates, financial articles, risk rules |
| **Cena** | Health resources, habit frameworks, capacity notes |
| **Luffy** | Experiments to try, beliefs to question, exploration ideas |

---

## Quick Start

Start with **one agent** — e.g. Neo if you’re learning to code. Add 2–3 links or a short note to their `index.md`, then ask that agent a question and see if they use it.
