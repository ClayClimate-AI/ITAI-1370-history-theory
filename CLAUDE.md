# CLAUDE.md — ITAI-1370 Course Repository Context

> This file is read automatically by Claude in Cursor, Claude Code, and any
> Claude-powered IDE session. It provides persistent project context so every
> session starts informed — no re-explaining needed.

---

## Who I Am

**Joseph Clay** — AI & Robotic Design AAS/BAT student at Houston Community
College, Summer 2026. I am 37, based in Humble, TX. I have a combined
background in commercial HVAC/refrigeration (EPA 608 Universal, TDLR
#148984), GLP/cGMP biotech cleanroom work, and self-taught software
development (JavaScript, Python, React, Java). I am the founder of
Clay Climate AI, an AI-powered voice-to-report automation service for HVAC
companies built on Make.com, AssemblyAI, and the Claude API.

I learn best when explanations are direct, specific, and treat me as
intelligent. Do not talk down to me. Do not pad responses with generic
encouragement. Give me the real path forward.

---

## This Repository

**Course:** ITAI-1370 — Artificial Intelligence History, Theory & Platforms  
**School:** Houston Community College · WLOP Campus · Room 155  
**Schedule:** Mondays & Wednesdays · 6:00 PM – 8:50 PM  
**Dates:** June 1 – August 9, 2026  
**Instructor:** Anna Devarakonda · annapurna.rachapudi@hccs.edu  
**GitHub Org:** ClayClimate-AI  

This repo documents my full learning journey through 16 modules. Every
module has the same internal structure: notes, assignments, code, reflections,
and resources. The goal is dual — complete the course requirements AND build
real developer skills simultaneously through consistent commits, Python labs,
and structured documentation.

---

## Grading Structure

| Component | Weight | Due |
|---|---|---|
| Weekly Assignments | 40% | Each module |
| Midterm — AI Glossary | 35% | Mid-semester |
| Final Portfolio (PowerPoint) | 25% | August 8, 2026 |

**Late policy:** 10% per day · Not graded after 5 days late

---

## Repository Structure

```
ITAI-1370/
├── CLAUDE.md                    ← you are here
├── README.md                    ← full course documentation
├── syllabus.pdf                 ← official HCC syllabus
├── modules/
│   ├── module-01/               ← Welcome to AI
│   │   ├── notes/               ← lecture notes in Markdown
│   │   ├── assignments/         ← prompts + submissions
│   │   ├── code/                ← Python scripts and labs
│   │   ├── reflections/         ← personal takeaways
│   │   └── resources/           ← module-specific PDFs
│   └── module-02/ ... module-16/
├── portfolio/                   ← Final Exam (Aug 8, 100 pts)
│   ├── slides/
│   └── assets/
├── midterm-glossary/            ← 35% of grade
└── _templates/                  ← reusable note/reflection starters
```

---

## All 16 Modules — Quick Reference

| # | Title | Key Concept |
|---|---|---|
| 01 | Welcome to AI | Definitions, everyday AI, course structure |
| 02 | History of AI | Turing, Dartmouth 1956, AI winters, deep learning revolution |
| 03 | AI Plays Games | Reinforcement learning, Deep Blue, AlphaGo |
| 04 | Machine Learning | Supervised/unsupervised/RL, training data, bias |
| 05 | ML Lifecycle | Problem → data → train → deploy → monitor |
| 06 | Neural Networks | Neurons, weights, backpropagation, overfitting |
| 07 | Deep Learning & Foundation Models | CNNs, RNNs, Transformers, GPT, Claude, Gemini |
| 08 | Computer Vision | Image recognition, facial recognition, deepfakes |
| 09 | NLP | Tokens, embeddings, transformers, chatbots, translation |
| 10 | Autonomous Agents | Perception → decision → action, multi-agent systems |
| 11 | Generative AI | GANs, diffusion models, DALL-E, prompt engineering |
| 12 | Robotics | Sensor fusion, Boston Dynamics, surgical robots |
| 13 | Ethics & Regulation | Bias, EU AI Act, accountability, misinformation |
| 14 | What's Next | Multimodal AI, AGI, agentic systems, AI in science |
| 15 | Final Review | Synthesis, peer feedback, exam prep |
| 16 | Final Exam / Portfolio | Full course portfolio submission |

---

## How I Work In This Repo

### Standard module workflow
1. After lecture → write `modules/module-XX/notes/lecture-notes.md`
2. Download assignment from Canvas → save to `assignments/prompt.pdf`
3. Write submission → `assignments/submission.md`
4. Build code lab if applicable → `code/lab.py`
5. Write reflection → `reflections/reflection.md`
6. Commit with a meaningful message:
   `git commit -m "module-02: notes on Turing, Dartmouth, AI winters"`

### When I ask for help with code labs
- I am working in **Cursor IDE** with Python
- Default to Python 3.x unless I specify otherwise
- Keep code clean, commented, and runnable as-is
- If a lab connects to an AI concept from the module, name that connection
  explicitly — I want to understand the why, not just the how

### When I ask for help with written assignments
- Treat me as the author — help me structure and strengthen MY thinking,
  do not write it for me
- Use plain language first, then introduce technical vocabulary
- Flag any claims that need a citation

### When I ask for help with the portfolio
- Portfolio is a PowerPoint (PPTX) due August 8
- Per-module structure: Title → Summary → Key Points → Activities → Reflection
- Max 30–40 slides total
- Final export as PDF for submission
- Assets live in `portfolio/assets/`

---

## My Coding Context

- **Languages:** Python (primary for this course), JavaScript, React, Java
- **IDE:** Cursor with agent mode
- **Python level:** Completed ISYS 214 at Regent University (A grade, Fall 2024)
  Comfortable with: functions, loops, f-strings, file I/O, basic OOP
  Currently building: Clay Climate AI automation scripts
- **Git comfort level:** Comfortable with add/commit/push — branching is a
  growth area I am actively practicing
- **Style preference:** Clean, readable, well-commented code over clever
  one-liners. I want to understand every line.

---

## Related Repos In This Org

| Repo | Purpose |
|---|---|
| `AI--Glossary` | ITAI-1370 midterm project — living AI term reference |
| `Python_Udemy_Projects` | Python skill-building alongside coursework |
| `docs` | Clay Climate AI product documentation |

---

## What Not To Do When Helping Me

- Do not re-explain things I already know — check this file first
- Do not suggest I use a different language unless Python genuinely won't work
- Do not give me watered-down answers — I can handle complexity
- Do not add filler encouragement — direct feedback is more useful to me
- Do not ignore the module context — if I'm working in module-07, that means
  we're in deep learning and foundation models territory; connect the dots

---

## Personal Note

This course is part of a larger arc. I am building toward a career in applied
AI — specifically at the intersection of building automation systems, HVAC,
and AI-driven tooling. Clay Climate AI is the live product that runs on this
foundation. Every module I complete and every commit I push is evidence of
that trajectory. When in doubt about relevance, connect it to that bigger picture.

