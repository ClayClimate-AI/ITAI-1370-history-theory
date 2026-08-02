<div align="center">

# ITAI-1370 — Artificial Intelligence History, Theory & Platforms

![HCC](https://img.shields.io/badge/HCC-AI_%26_Robotic_Design-gold?style=flat-square)
![Summer 2026](https://img.shields.io/badge/Summer_2026-Jun_1_–_Aug_9-blue?style=flat-square)
![Credits](https://img.shields.io/badge/Credits-3-purple?style=flat-square)
![Status](https://img.shields.io/badge/Status-In_Progress-brightgreen?style=flat-square)
![Modules](https://img.shields.io/badge/Modules-16-orange?style=flat-square)
[![GitHub](https://img.shields.io/badge/GitHub-ClayClimate--AI-black?style=flat-square&logo=github)](https://github.com/ClayClimate-AI)

<br/>

> **Joseph Clay** · Houston Community College · AI & Robotic Design AAS/BAT  
> *Documenting the full journey — not just for a grade, but as evidence of who I'm becoming.*

</div>

---

## Table of Contents

- [About This Repository](#about-this-repository)
- [Current Status](#current-status)
- [Course At A Glance](#course-at-a-glance)
- [Grading Breakdown](#grading-breakdown)
- [Repository Structure](#repository-structure)
- [Module Map — Real Canvas Structure](#module-map--real-canvas-structure)
- [Terminal Setup — Run This First](#terminal-setup--run-this-first)
- [How I Use This Repo](#how-i-use-this-repo)
- [Portfolio Final Exam](#portfolio-final-exam)
- [Midterm AI Glossary](#midterm-ai-glossary)
- [Skills Built Simultaneously](#skills-built-simultaneously)
- [Author](#author)

---

## About This Repository

This repo documents **ITAI-1370: Artificial Intelligence History, Theory & Platforms** at Houston Community College — 16 modules spanning the full arc of AI: from symbolic logic and the 1956 Dartmouth Conference through deep learning, foundation models, robotics, generative AI, and responsible AI governance.

Every assignment lives here. Every reflection gets committed. Every lab that can be executed as code, gets coded.

This is **not** just homework storage. It is a living portfolio artifact — structured evidence of a learning journey that runs in parallel with building real applied developer and AI engineering skills. Future employers who open this repo will see module-by-module documentation, Python experiments, reflections, and a deployed portfolio — not a folder of Word docs.

Every module also carries a **mini CDR** (a scaled-down Critical Design
Review) and a **prompt-history record** — the part of the work that shows
*how* the thinking happened, not just what got turned in. See
[How I Use This Repo](#how-i-use-this-repo) for the full convention.

---

## Current Status

*Last updated: August 2, 2026*

| Module | Real Canvas items | Status |
|---|---|---|
| 01 — Introduction to A.I.: Course Setup | A01, L01 | ✅ Complete — 100%, 100% |
| 02 — Introduction to A.I.: The Big Issues | A02, L02, Puzzle 02 | ✅ Complete — 98%, 98%, 99/100 |
| 03 — Games, Prelude to A.I. | InClass Stock Tracker, A03, L03, Puzzle 03 | ✅ Complete — 98/100, 98/100, 98%, 99/100 |
| 04 — Games Change Everything | A04, L04 | ✅ Complete — 98%, 98% |
| 05 — Machine Learning: The Data | A05, L05 | ✅ Complete — 98%, 95% |
| 06 — Machine Learning: The Pipeline | A06 | ✅ Complete — 95% |
| 07 — Deep Learning: Neural Networks | A07, L07 | ✅ Complete — 94%, 94% |
| 08 — Deep Learning: Big Data and Architectures | A08, L08 | ✅ Complete — 94%, 95% |
| 09 — Computer Vision: Image Processing | L09 | ✅ Complete — submitted (image evidence gap disclosed in-document) |
| 10 — NLP: Basics | A10, Lab 10 (IBM Watson) | ✅ Complete — submitted late, ungraded |
| 11 — NLP: LLMs | A11, L11 | ✅ Complete — submitted late, ungraded |
| 12 — AI Agents | A12 | ✅ Complete — submitted late, ungraded |
| 13 — Robotics: Grand Tour | A13 | ✅ Complete — submitted late, ungraded |
| 14–16 | Nothing assigned yet on Canvas | n/a |
| Midterm — AI Glossary | — | ✅ Complete — 94% |
| Final Portfolio | — | ✅ Complete — 11-page PDF, all 13 modules + Bonus (Hermes Agent) + Conclusion + Future Objectives — ready to submit, due Aug 8 |
| Per-module `resources/` | — | ⬜ Pending — source materials currently live in `Class Notes/`, awaiting a sort pass |

> Modules 01–07 were backfilled retroactively — the notes/reflections/mini-CDRs
> were written after the assignments were already submitted, not during
> lecture. Each file says so explicitly. Modules 08–13 mix backfilled
> documentation with real, live collaboration as each assignment was built.
>
> The module numbering above reflects Canvas's real Modules page, not the
> topic list this README originally shipped with — a handful of
> assignments were filed under the wrong module number early on (e.g. A05
> briefly lived under Module 04) and have since been corrected.

---

## Course At A Glance

| Field | Detail |
|---|---|
| **Course** | ITAI-1370 · Section 29 · S10 2026 |
| **Instructor** | Anna Devarakonda · annapurna.rachapudi@hccs.edu |
| **Location** | WLOP Campus · Room 155 |
| **Schedule** | Mondays & Wednesdays · 6:00 PM – 8:50 PM |
| **Dates** | June 1, 2026 → August 9, 2026 |
| **Program** | AI & Robotic Design AAS/BAT · Houston Community College |
| **Canvas** | eagleonline.hccs.edu · Course ID 332486 |

---

## Grading Breakdown

| Component | Weight | Due | Description |
|---|---|---|---|
| **Weekly Assignments** | 40% | Each module | Group tasks — written docs, PPT, or multimedia |
| **Midterm — AI Glossary** | 35% | Mid-semester | Group glossary of AI terms w/ definitions |
| **Final Exam — Portfolio** | 25% | **Aug 8** | 100-pt PowerPoint portfolio of full course journey |

> **Late Policy:** 10% deducted per day · Not graded after 5 days late · No extensions past last class day

**Grade Scale:** A (90+) · B (80-89) · C (70-79) · D (60-69) · F (59 and below)

---

## Repository Structure

```
ITAI-1370/
│
├── README.md                          ← You are here
├── MASTER-TRACKER.md                  ← Wave-by-wave assignment tracker (living doc)
│
├── modules/                           ← One folder per module (16 total)
│   ├── module-01/                     ← Welcome to AI
│   │   ├── notes/                     ← Lecture notes, key concepts (Markdown)
│   │   ├── assignments/               ← Assignment prompts + submissions
│   │   │   ├── mini-cdr.md            ← Scaled-down Critical Design Review
│   │   │   └── prompt-history.md      ← Real AI-collaboration log (or a
│   │   │                                 prompt-history-note.md for modules
│   │   │                                 backfilled before this convention started)
│   │   ├── code/                      ← Scripts, snippets, worked examples
│   │   ├── reflections/               ← Challenges faced, lessons learned
│   │   └── resources/                 ← Module-specific PDFs, links, reading
│   ├── module-02/ ... module-16/      ← Same structure for every module
│
├── portfolio/                         ← Final Exam deliverable (due Aug 8, 100 pts)
│   ├── FE_JosephClay_ITAI1370.pdf     ← Final submission (11-page designed PDF)
│   ├── FE_JosephClay_ITAI1370_source.md ← Source content, module-by-module
│   ├── Hermes_Agent_bonus_challenge.pdf ← Source deck for the Bonus section
│   └── Final-Exam-Portfolio-requirements.md ← Real Canvas requirements, verbatim
│
├── midterm-glossary/                  ← Midterm (35% of grade)
│   ├── terms/                         ← Individual term definition files
│   ├── references/                    ← Source citations
│   └── submissions/                   ← Final submitted versions
│
├── resources/
│   ├── reading-materials/             ← Course-wide PDFs and reference papers
│   └── ai-collaboration-vocabulary.md ← Verification loops, prompt contracts,
│                                          reverse prompting, context management
│
└── _templates/                        ← Reusable templates
    ├── notes-template.md
    ├── reflection-template.md
    ├── glossary-term.md
    ├── mini-cdr-template.md
    └── prompt-history-template.md
```

---

## Module Map — Real Canvas Structure

Pulled directly from the course's Canvas Modules page (verified Aug 1,
2026) — this replaces an earlier version of this table that was a guessed
template and didn't match reality past Module 07.

| # | Real Module Title | Canvas Items | Notes |
|---|---|---|---|
| 01 | Introduction to A.I. – Course Setup | A01, L01 | |
| 02 | Introduction to A.I. – The Big Issues | A02, L02, Puzzle 02 | |
| 03 | Games, Prelude to A.I. | InClass Stock Tracker, A03, L03, Puzzle 03 | L03 = Scratch Paddle Game (Stock Tracker was a separate last-minute in-class add) |
| 04 | Games Change Everything | A04, L04 | |
| 05 | Machine Learning – The Data | A05, L05 | |
| 06 | Machine Learning – The Pipeline | A06 | No lab this module |
| 07 | Deep Learning – Neural Networks | A07, L07 | |
| 08 | Deep Learning – Big Data and Architectures | A08, L08 | GANs / Fact-or-Fiction |
| 09 | Computer Vision – Image Processing | L09 | No A09 on Canvas |
| 10 | NLP – Basics | A10, Lab 10 | Lab 10 = IBM Watson Chatbot |
| 11 | NLP – LLMs | A11, L11 | A11 = AI assistants vs. the movie *Her* |
| 12 | AI Agents | A12 | No lab this module |
| 13 | Robotics – Grand Tour | A13 | Robotic design & ethical analysis |
| 14 | Robotics – Hard and Soft Issues | — | Nothing assigned yet |
| 15 | Responsible AI | — | Placeholders only, not yet populated |
| 16 | Platforms and Security – Cognitive Issues | — | Placeholders only, not yet populated |
| *(separate)* | Mid Term Glossary / Final Exam Portfolio | Midterm Glossary, Final Exam Portfolio | `midterm-glossary/`, `portfolio/` |

---

## Terminal Setup — Run This First

Open your terminal in Cursor (`Ctrl + backtick`) and run these commands to initialize the full directory tree and set up git tracking from day one.

### Step 1 — Navigate to your projects folder

```bash
cd ~/Documents
# or wherever you keep your code projects
```

### Step 2 — Create the full directory tree in one command block

```bash
BASE="ITAI-1370"

for i in 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16; do
  mkdir -p "$BASE/modules/module-$i/notes"
  mkdir -p "$BASE/modules/module-$i/assignments"
  mkdir -p "$BASE/modules/module-$i/code"
  mkdir -p "$BASE/modules/module-$i/reflections"
  mkdir -p "$BASE/modules/module-$i/resources"
done

mkdir -p "$BASE/portfolio/slides"
mkdir -p "$BASE/portfolio/assets/images"
mkdir -p "$BASE/portfolio/assets/charts"
mkdir -p "$BASE/portfolio/assets/qr-codes"
mkdir -p "$BASE/portfolio/drafts"
mkdir -p "$BASE/midterm-glossary/terms"
mkdir -p "$BASE/midterm-glossary/references"
mkdir -p "$BASE/midterm-glossary/submissions"
mkdir -p "$BASE/resources/reading-materials"
mkdir -p "$BASE/_templates"

echo "✅ ITAI-1370 directory tree created"
```

### Step 3 — Initialize git and create your first commit

```bash
cd ITAI-1370
git init
git add README.md
git commit -m "init: ITAI-1370 course repo — Joseph Clay, HCC Summer 2026"
```

### Step 4 — Connect to GitHub

```bash
# Create the repo at github.com/ClayClimate-AI first, then:
git remote add origin https://github.com/ClayClimate-AI/ITAI-1370-history-theory.git
git branch -M main
git push -u origin main
```

### Step 5 — Verify your tree looks right

```bash
find . -type d | sort
```

---

## How I Use This Repo

### Every module, same workflow:

```bash
# Navigate to the module
cd modules/module-01

# 1. After lecture — write your notes
code notes/lecture-notes.md

# 2. Download assignment prompt from Canvas, drop it in:
# assignments/prompt.pdf

# 3. Write your submission
code assignments/submission.md

# 4. If there's a code lab, build it
code code/lab.py

# 5. Write your reflection after completing the module
code reflections/reflection.md

# 6. Commit everything
git add .
git commit -m "module-01: completed notes, assignment, and lab"
git push
```

### Module notes template (save as `_templates/notes-template.md`):

```markdown
# Module [NUMBER] — [TITLE]

**Date:** [Date]  
**Topic Area:** [e.g., History / Machine Learning / NLP]

---

## Key Concepts
- 

## Important Names / Figures
- 

## Vocabulary
| Term | Definition |
|------|-----------|
|  |  |

## Real-World Applications
- 

## Questions I Still Have
- 

## Connection to Clay Climate AI / My Work
- 
```

### Reflection template (save as `_templates/reflection-template.md`):

```markdown
# Reflection — Module [NUMBER]

**What challenged me this module:**

**What clicked that didn't before:**

**How I'd explain this concept to someone who knows nothing about AI:**

**One thing I want to go deeper on:**

**How this connects to the broader AI landscape:**
```

### Mini CDRs and prompt history — why they're here

Notes and reflections show what I learned. They don't show *how* I got there —
and "did you actually learn this, or did AI just hand it to you" is a fair
question for any of this work. Two more artifacts exist per module to answer
that directly:

- **`assignments/mini-cdr.md`** — a scaled-down Critical Design Review per
  assignment: the problem, the approach, what worked, what I'd change, and
  the one concept I could explain cold in an interview.
- **`assignments/prompt-history-note.md`** (or a full `prompt-history.md`
  going forward) — a record of the actual collaboration with AI tools:
  planning prompts, push-back, debugging, revisions.

Mini CDRs are written as ASCII tree diagrams, not prose paragraphs — the
same box-drawing format used throughout this repo for anything
hierarchical — so the structure is visible at a glance instead of buried in
a wall of text:

```
Mini CDR — Module [NUMBER]: [ASSIGNMENT NAME]
|
├── Problem / Prompt
├── Approach
├── What worked
├── What didn't / had to change
├── What I'd do differently next time
└── Key concept takeaway
```

Modules 01–07 didn't have contemporaneous prompt logs — that habit started
partway through the course, so those modules carry a short honest note
instead of a fabricated transcript. Modules 08–10 are documentation gaps
(real, graded work with no local content yet — see each module's
`gap-note.md`). Starting module 11, prompt history is logged live using
`_templates/prompt-history-template.md`. Mini CDRs use
`_templates/mini-cdr-template.md`.

The vocabulary behind both — verification loops, prompt contracts, reverse
prompting, context management — is written up in
`resources/ai-collaboration-vocabulary.md`, in interview-ready language.

---

## Portfolio Final Exam

**Due: August 8, 2026 · 100 points · 25% of grade · Individual · 1 attempt**

Per the real Canvas assignment text (`portfolio/Final-Exam-Portfolio-requirements.md`,
copied verbatim): for each module, record activities and results — what
was learned — with tables, graphs, and images as appropriate, links to
valuable articles/videos, and citations for any intellectual property
used. Convert the completed file to a PDF for submission.

**What was actually built:** a single, professionally designed 11-page
PDF (`portfolio/FE_JosephClay_ITAI1370.pdf`) — a cover page, a course
grade-snapshot/table-of-contents page, an activities-and-what-I-learned
card for each of the 13 active modules with real grades, the Midterm, a
Bonus section on the Hermes Agent extra-credit challenge, the Modules
14–16 status note, a Conclusion tying the semester's throughline
together, and a Future Objectives section in Joe's own words. Source
content lives in `portfolio/FE_JosephClay_ITAI1370_source.md`.

**Pre-submission checklist:**
- [x] All 13 active modules documented with real activities, results, and grades
- [x] Tables (grade pills) and images/diagrams referenced where they exist
- [x] Honest gaps disclosed directly (e.g. Module 09's missing image evidence)
- [x] Conclusion includes future objectives in AI, in my own words
- [x] Bonus/extra-credit work (Hermes Agent) included and tied to the semester throughline
- [x] Final file exported as PDF
- [ ] Submitted to Canvas under the confirmed filename `FE JosephClay ITAI 1371 2023`

---

## Midterm AI Glossary

**Weight: 35% of total grade · Group project**

The midterm requires building a collaborative glossary of AI-related terms — precise definitions that demonstrate you understand the nuances between similar concepts (e.g., machine learning vs deep learning vs AI).

### Glossary term template (save as `_templates/glossary-term.md`):

```markdown
## [Term]

**Category:** [e.g., Machine Learning / NLP / Computer Vision]  
**Definition:** [Your definition in plain, precise language]  
**Example:** [Real-world use case]  
**Related Terms:** [2–3 connected terms]  
**Source:** [Citation]
```

> Term files live in `midterm-glossary/terms/` · Final submission in `midterm-glossary/submissions/`

---

## Skills Built Simultaneously

Every module you complete in this repo also trains a parallel set of real developer skills — without any extra effort.

| Academic Activity | Developer Skill Being Built |
|---|---|
| Writing `notes.md` after lecture | Markdown fluency (used in every GitHub README, PR, and technical doc) |
| Organizing 16 module folders | File system and codebase thinking |
| `git commit` after every assignment | Git version control — muscle memory |
| Building code labs in `code/` | Python reps tied directly to AI concepts being studied |
| Writing `reflections/` | Technical writing — documenting your thought process like an engineer |
| Creating portfolio slides | Presentation and communication skills for technical audiences |
| Building QR-linked GitHub projects | Public portfolio building — what hiring managers actually look at |
| Using Cursor agent for code labs | Real IDE workflow with AI-assisted development |

> By module 8, none of this feels deliberate. It's just how you work.

---

## Author

**Joseph Clay**  
AI & Robotic Design AAS/BAT Candidate — Houston Community College, 2026  
EPA 608 Universal · TDLR HVAC Technician #148984 · OSHA 10  
Full Stack Developer · Python · React · JavaScript · Java  

💻 [github.com/ClayClimate-AI](https://github.com/ClayClimate-AI)  
📧 Available via HCC student email

---

> *"Forget the former things; do not dwell on the past. See, I am doing a new thing."*  
> — Isaiah 43:18–19

