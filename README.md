<div align="center">

# 🤖 ITAI-1370 — Artificial Intelligence History, Theory & Platforms

![HCC](https://img.shields.io/badge/HCC-AI_%26_Robotic_Design-gold?style=flat-square)
![Summer 2026](https://img.shields.io/badge/Summer_2026-Jun_1_–_Aug_9-blue?style=flat-square)
![Credits](https://img.shields.io/badge/Credits-3-purple?style=flat-square)
![Status](https://img.shields.io/badge/Status-In_Progress-brightgreen?style=flat-square)
![Modules](https://img.shields.io/badge/Modules-16-orange?style=flat-square)
![GitHub](https://img.shields.io/badge/GitHub-ClayClimate--AI-black?style=flat-square&logo=github)

<br/>

> **Joseph Clay** · Houston Community College · AI & Robotic Design AAS/BAT  
> *Documenting the full journey — not just for a grade, but as evidence of who I'm becoming.*

</div>

---

## 📋 Table of Contents

- [About This Repository](#about-this-repository)
- [Course At A Glance](#course-at-a-glance)
- [Grading Breakdown](#grading-breakdown)
- [Repository Structure](#repository-structure)
- [Module Map — All 16 Modules](#module-map--all-16-modules)
- [Terminal Setup — Run This First](#terminal-setup--run-this-first)
- [How I Use This Repo](#how-i-use-this-repo)
- [Portfolio Final Exam](#portfolio-final-exam)
- [Midterm AI Glossary](#midterm-ai-glossary)
- [Skills Built Simultaneously](#skills-built-simultaneously)
- [Author](#author)

---

## 🧠 About This Repository

This repo documents **ITAI-1370: Artificial Intelligence History, Theory & Platforms** at Houston Community College — 16 modules spanning the full arc of AI: from symbolic logic and the 1956 Dartmouth Conference through deep learning, foundation models, robotics, generative AI, and responsible AI governance.

Every assignment lives here. Every reflection gets committed. Every lab that can be executed as code, gets coded.

This is **not** just homework storage. It is a living portfolio artifact — structured evidence of a learning journey that runs in parallel with building real applied developer and AI engineering skills. Future employers who open this repo will see module-by-module documentation, Python experiments, reflections, and a deployed portfolio — not a folder of Word docs.

---

## 📌 Course At A Glance

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

## 📊 Grading Breakdown

| Component | Weight | Due | Description |
|---|---|---|---|
| **Weekly Assignments** | 40% | Each module | Group tasks — written docs, PPT, or multimedia |
| **Midterm — AI Glossary** | 35% | Mid-semester | Group glossary of AI terms w/ definitions |
| **Final Exam — Portfolio** | 25% | **Aug 8** | 100-pt PowerPoint portfolio of full course journey |

> **Late Policy:** 10% deducted per day · Not graded after 5 days late · No extensions past last class day

**Grade Scale:** A (90+) · B (80-89) · C (70-79) · D (60-69) · F (59 and below)

---

## 🗂️ Repository Structure

```
ITAI-1370/
│
├── README.md                          ← You are here
├── syllabus.pdf                       ← Official HCC course syllabus
│
├── modules/                           ← One folder per module (16 total)
│   ├── module-01/                     ← Welcome to AI
│   │   ├── notes/                     ← Lecture notes, key concepts (Markdown)
│   │   ├── assignments/               ← Assignment prompts + your submissions
│   │   ├── code/                      ← Python scripts, visualizations, labs
│   │   ├── reflections/               ← Challenges faced, lessons learned
│   │   └── resources/                 ← Module-specific PDFs, links, reading
│   ├── module-02/ ... module-16/      ← Same structure for every module
│
├── portfolio/                         ← Final Exam deliverable (due Aug 8, 100 pts)
│   ├── slides/                        ← portfolio_draft.pptx + portfolio_final.pdf
│   ├── assets/
│   │   ├── images/                    ← Screenshots, diagrams, visual aids
│   │   ├── charts/                    ← Data visualizations per module
│   │   └── qr-codes/                  ← QR codes linking to GitHub projects
│   └── drafts/                        ← In-progress slide versions
│
├── midterm-glossary/                  ← Midterm (35% of grade)
│   ├── terms/                         ← Individual term definition files
│   ├── references/                    ← Source citations
│   └── submissions/                   ← Final submitted versions
│
├── resources/
│   └── reading-materials/             ← Course-wide PDFs and reference papers
│
└── _templates/                        ← Reusable templates (notes, reflection, etc.)
```

---

## 🗺️ Module Map — All 16 Modules

| # | Module Title | Topic Area | Key Assignment | Code Lab Opportunity |
|---|---|---|---|---|
| 01 | Welcome to AI | Foundations | AI in My Daily Life | Map AI ecosystem in Python dict |
| 02 | History of AI | History | Timeline Creation | matplotlib timeline viz |
| 03 | AI Plays Games | Reinforcement Learning | Design AI Game Challenge | Simple reward function script |
| 04 | Machine Learning | Core ML | "Be the Algorithm" | sklearn classification demo |
| 05 | ML Lifecycle | ML Process | AI Product Pitch | Data pipeline pseudocode |
| 06 | Neural Networks | Deep Learning Intro | Human Neural Network Sim | Neuron weight diagram |
| 07 | Deep Learning & Foundation Models | Transformers/GPT | Foundation Model Exploration | API comparison script |
| 08 | Computer Vision | CV | Visual AI Ethics Debate | OpenCV image detection |
| 09 | NLP | Language AI | Lost in Translation | NLTK tokenizer demo |
| 10 | Autonomous Agents | Agents | Design an AI Assistant | Decision tree logic |
| 11 | Generative AI | GANs/Diffusion | AI Art Exhibition | Prompt comparison log |
| 12 | Robotics | Physical AI | Robot Ethics Scenarios | Sensor logic pseudocode |
| 13 | Ethics & Regulation | Responsible AI | AI Ethics Board Sim | Bias analysis script |
| 14 | What's Next | Emerging AI | Future AI Symposium | Trend research + summary |
| 15 | Final Review | Synthesis | AI Knowledge Showcase | Mind map generator |
| 16 | Final Exam / Portfolio | Capstone | **Portfolio Submission** | Full repo = the deliverable |

---

## ⚙️ Terminal Setup — Run This First

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
git remote add origin https://github.com/ClayClimate-AI/ITAI-1370.git
git branch -M main
git push -u origin main
```

### Step 5 — Verify your tree looks right

```bash
find . -type d | sort
```

---

## 📝 How I Use This Repo

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

---

## 🎓 Portfolio Final Exam

**Due: August 8, 2026 · 100 points · 25% of grade**

The final portfolio is a PowerPoint presentation documenting your full course journey. Per the official instructions:

| Slide | Content |
|---|---|
| Slide 1 | Title — Full name, course name |
| Slide 2 | Table of Contents |
| Slide 3 | Introduction — course overview, personal learning goals |
| Slides 4–N | Module-by-module record (see below) |
| Slides N+ | Graphs, tables & images (integrated per module) |
| Slides N+ | Article & video links with relevance notes |
| Slides N+ | GitHub / project integration with QR codes |
| Slide N | Conclusion & future objectives |
| Slide N | Bibliography |

### Per-module slide block (4–5 slides each):

```
1. Module Title Slide    — module name and number
2. Summary Slide         — what the module covered (2–4 sentences)
3. Key Points Slide      — main learnings in bullet format
4. Activities & Results  — assignments, projects, charts, visual output
5. Reflection Slide      — challenges, solutions, key takeaways
```

> Portfolio assets live in `portfolio/assets/` · Working file in `portfolio/slides/portfolio_draft.pptx` · Final export as `portfolio/slides/portfolio_final.pdf`

**Pre-submission checklist:**
- [ ] All 16 modules documented with all slide types
- [ ] Charts, tables, and images have captions
- [ ] Article/video links annotated with relevance notes
- [ ] GitHub project slides include QR codes
- [ ] Conclusion includes future objectives in AI
- [ ] Bibliography uses consistent citation style
- [ ] Final file exported as PDF
- [ ] Slide count within 30–40 range

---

## 📚 Midterm AI Glossary

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

## 🛠️ Skills Built Simultaneously

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

## 👤 Author

**Joseph Clay**  
AI & Robotic Design AAS/BAT Candidate — Houston Community College, 2026  
EPA 608 Universal · TDLR HVAC Technician #148984 · OSHA 10  
Full Stack Developer · Python · React · JavaScript · Java  

🌐 [josephclay.dev](https://josephclay.dev)  
💻 [github.com/ClayClimate-AI](https://github.com/ClayClimate-AI)  
📧 Available via HCC student email

---

> *"Forget the former things; do not dwell on the past. See, I am doing a new thing."*  
> — Isaiah 43:18–19

