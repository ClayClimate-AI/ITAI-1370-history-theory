# Module 02 — Introduction to A.I.: The Big Issues

**Topic Area:** History / Foundational Figures
**Note:** Backfilled from three real Canvas items — A02 (Google & AI
Patents), L02 (Key People & Foundational Work spreadsheet), and Puzzle 02
(Google's Hat Puzzle). L03 (previously documented here by mistake) has
been moved to Module 03, where it actually belongs on Canvas — it's
unrelated (the AI Stock Sentiment Tracker, not hat-puzzle content).

---

## A02 — Why Google Was Created / AI Patents (2014–2023)

### Key Concepts
- **PageRank's founding insight**: pre-Google search engines (AltaVista,
  Yahoo) ranked pages by raw keyword frequency, which was trivially
  gameable and often irrelevant. Google's bet was ranking by link
  structure instead — Larry Page's stated goal was a search engine that
  "would understand exactly what you mean and give back exactly what you
  want."
- **The GenAI patent surge maps directly onto four dated milestones**:
  2017 Transformer ("Attention Is All You Need") → 800%+ surge in GenAI
  patent filings; 2020 GPT-3 → accelerated corporate filings; 2022 ChatGPT
  (100M users in 2 months, fastest product adoption in history) → new
  R&D/IP wave; 2023 → over 25% of all GenAI patents ever filed were
  published in that single year, with China leading globally and the U.S.
  second.

### Vocabulary
| Term | Definition |
|---|---|
| PageRank | Google's founding algorithm — ranks pages by link structure/authority instead of raw keyword frequency |
| Patent family | A patent landscape metric counting related patent filings across jurisdictions, used by WIPO to track GenAI IP growth |

### Real-World Applications
Patent filing volume as a leading indicator of where AI R&D investment is
actually concentrated — the data shows the shift from research paper
(2017 Transformer) to product (2022 ChatGPT) to IP land-grab (2023) in
under six years.

## L02 — Key People & Foundational Work in AI History

An 11-person research spreadsheet, each row covering: best date of work,
institution, key papers, funding source, final product, today's derived
capability, where the work continues today, and rough field size.

### Key Figures Documented

| Person | Landmark work | Direct line to today |
|---|---|---|
| Alan Turing (1912–1954) | 1936 Turing Machine; 1950 Turing Test | Foundation of every modern computer and AI system; LLM eval benchmarks descend from the Turing Test |
| John McCarthy (1927–2011) | 1956 Dartmouth Conference; 1958 Lisp | Coined "Artificial Intelligence"; Lisp descendants still used in symbolic AI/knowledge graphs |
| Marvin Minsky (1927–2016) | 1951 SNARC neural net; 1969 Perceptrons critique | Society of Mind theory influences modern multi-agent AI architectures |
| Newell & Simon (1927–1992 / 1916–2001) | 1955–56 Logic Theorist; 1957 General Problem Solver | GPS influenced modern AI planning; Simon's Nobel (Economics, 1978) tied to bounded rationality |
| Claude Shannon (1916–2001) — ★ namesake of Claude AI | 1948 Information Theory | Every digital transmission uses Shannon's theorems; parity bits in all storage/networking |
| Frank Rosenblatt (1928–1971) | 1957–58 Perceptron (first hardware neural net) | Direct ancestor of every deep learning layer in use today |
| Geoffrey Hinton (b. 1947) | 1986 Backpropagation; 2012 AlexNet | Foundation of all modern AI: GPT-4, Gemini, Claude, Stable Diffusion |
| Yann LeCun (b. 1960) | 1989–98 CNNs / LeNet | CNNs power all image recognition — Face ID, medical imaging, autonomous vehicles |
| Yoshua Bengio (b. 1964) | 2003 Neural Language Model; 2014 Attention Mechanism | Attention mechanism is the core of every LLM in use today |
| Vaswani et al. (Google Brain, 2017) | Transformer architecture ("Attention Is All You Need") | Powers every modern LLM: GPT-4, Gemini, Claude, LLaMA, BERT |
| Arthur Samuel (1901–1990) | 1952–59 Machine learning / checkers program | Coined the term "machine learning"; self-play lineage runs through AlphaGo |

### Key Concepts
- **Funding sources are almost entirely military/government/corporate
  R&D**, not individual grants — DARPA, ONR, NSF, and internal corporate
  R&D budgets (Bell Labs, IBM, Google) show up across nearly every row.
  Foundational AI research has never been separable from defense and
  corporate funding.
- **Every landmark traces a direct, unbroken line to a system in use
  today** — this spreadsheet format (Then → Now) is itself an argument
  that AI history isn't a sequence of disconnected breakthroughs, it's
  one continuous lineage.

## Puzzle 02 — Google's Hat Puzzle

See the full write-up already in this module: 100 prisoners, parity
encoding, one shared bit guaranteeing 99% survival. (Full tree diagram and
AI-concept mapping already documented — unchanged by this reorganization.)

## Questions I Still Have

- The patent-surge data (A02) and the funding-lineage data (L02) tell the
  same story from two different angles — corporate R&D money chasing
  research breakthroughs. Is there a year-by-year way to show the funding
  driving the patents, rather than just correlating two separate timelines?

## Connection to Clay Climate AI / My Work

The L02 "Final Product → Today's Capability → Where Today" structure is
close to how I should be documenting Clay Climate AI's own build
decisions — not just what was built, but which prior technique it's
actually descended from and where that lineage is headed next.
