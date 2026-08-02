# Module 06 — Neural Networks / Knowledge Graph

**Topic Area:** Deep Learning Intro
**Note:** Backfilled from the completed A06 (Machine Learning Knowledge
Graph, built in Whimsical) report, not written live during lecture.

---

## Key Concepts

- **The ML landscape is an ecosystem, not a checklist.** Before this
  exercise, the roadmap topics felt like a sequence to learn in order.
  Mapping them as a graph showed they're not sequential — several run
  through every other branch simultaneously.
- **Infrastructure vs. technique.** Tools and Frameworks (Cloud Platforms,
  Version Control) aren't a stage you pass through — they're infrastructure
  every Learning Approach depends on, at every stage.
- **Python as connective tissue.** Python isn't just a Foundations skill —
  it's also a direct prerequisite for the entire Tools layer (Jupyter,
  Pandas, PyTorch), so it runs across two branches, not one.

## Knowledge Graph Structure (as a tree)

```
Machine Learning
|
├── Foundations
|   ├── Linear Algebra
|   ├── Calculus and Statistics
|   ├── Probability
|   └── Python Programming ──┐ (cross-branch dependency, see below)
|
├── Learning Approaches
|   ├── Supervised Learning ──→ informs Decision Models (Techniques)
|   ├── Unsupervised Learning ──→ informs Clustering (Techniques)
|   ├── Reinforcement Learning ──→ connects to Neural Networks + Applications
|   └── Self-Supervised Learning
|
├── Techniques
|   ├── Neural Networks ──→ primary engine for Computer Vision + NLP
|   ├── Decision Models
|   └── Clustering
|
├── Tools and Frameworks
|   ├── PyTorch and TensorFlow
|   ├── Jupyter Notebooks ←── depends on Python (Foundations)
|   ├── Version Control (Git) ──→ supports ALL four Learning Approaches
|   ├── Pandas ←── depends on Python (Foundations)
|   └── Cloud Platforms ──→ supports ALL four Learning Approaches
|
└── Applications
    ├── Natural Language Processing (NLP) ←── powered by Neural Networks
    ├── Computer Vision ←── powered by Neural Networks
    └── Recommendation Systems
```

## Vocabulary

| Term | Definition |
|---|---|
| Knowledge graph | A visual map of a domain's concepts as nodes, with edges representing dependency/relationship — used here to make cross-cutting dependencies visible instead of implicit |
| Cross-cutting dependency | A relationship between concepts in *different* primary branches (e.g., Python in Foundations feeding directly into Tools) rather than within one branch |

## Real-World Applications

- Whimsical / mind-mapping tools for scoping any complex technical domain
  before starting to learn it, not just ML specifically.
- The same "infrastructure vs. technique" distinction applies to any tech
  stack — recognizing which pieces are always-on dependencies changes what
  you prioritize learning first.

## Questions I Still Have

- How would this graph need to change to represent *time* — i.e., which
  nodes were foundational 10 years ago vs. which are recent additions to the
  roadmap (e.g., self-supervised learning is much newer than supervised/
  unsupervised)?

## Connection to Clay Climate AI / My Work

Recognizing Tools and Frameworks (Cloud Platforms, Version Control) as
infrastructure rather than a learning stage matches exactly how Clay
Climate AI is structured — Make.com and now the self-hosted Hermes stack
aren't a phase I "finished," they're the substrate every feature (voice
transcription, report generation, cost logic) runs on top of continuously.
