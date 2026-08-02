# Module 01 — Welcome to AI / History of AI

**Topic Area:** Foundations / History
**Note:** These notes were backfilled from the completed A01 research paper
(`assignments/A01_AIHistoryResearch_JosephClay_1370.docx`), not written live
during lecture. They're organized as study notes on the module's core
concepts, pulled from work I actually did.

---

## Key Concepts

- **The "AI effect"** — each generation defines intelligence as whatever
  machines *can't* do yet, so the goalposts move as capabilities improve.
  Chess and speech transcription were once "proof" of machine thought; now
  they're routine engineering.
- **Symbolic AI vs. connectionism** — the whole history of the field is a
  tension between two ideas: intelligence as explicit rule-following
  (symbolic logic) vs. intelligence as learned statistical patterns from data
  (neural networks). The second one won, but not until it survived decades of
  being sidelined.
- **AI winters** — funding collapses (1970s, ~1990) that followed periods of
  overpromising. The pattern repeats: hype → unmet expectations → funding
  dries up → a marginalized idea (neural nets) quietly keeps developing until
  conditions change.
- **The Transformer / self-attention (2017)** — replaced sequential
  processing with a mechanism that's both more accurate and parallelizable.
  This is the architecture underneath every modern large language model.

## Important Names / Figures

| Name | Contribution |
|---|---|
| Alan Turing | 1936 universal machine (theory of computation); 1950 Turing Test — reframed "can machines think" as an operational, testable question |
| John McCarthy | Coined "artificial intelligence" at Dartmouth 1956; invented Lisp |
| Marvin Minsky | Symbolic-era theorist; his 1969 critique of the Perceptron slowed neural-network research for years |
| Geoffrey Hinton | Kept neural-network research alive through the years it was out of fashion; his lab produced AlexNet (2012); 2024 Nobel Prize in Physics |

## Vocabulary

| Term | Definition |
|---|---|
| Turing Test | An operational test for machine intelligence: if a human can't reliably tell the machine's responses from a human's, credit the machine with intelligence |
| Expert system | A program that encodes a specialist's knowledge as if-then rules (e.g., MYCIN for infection diagnosis) — powerful in a narrow domain, brittle outside it |
| Perceptron | Rosenblatt's 1958 trainable neural network — the earliest ancestor of today's deep learning |
| Backpropagation | The algorithm (popularized 1980s) that made training multi-layer neural networks practical |
| AlexNet | The 2012 deep neural network that won ImageNet by a margin so large it was initially suspected to be an error — the moment deep learning became mainstream |
| Transformer / self-attention | 2017 architecture ("Attention Is All You Need") that underlies GPT, Claude, and other modern LLMs |

## Real-World Applications

- Expert systems in medicine (MYCIN-style diagnosis) and finance.
- Facial-analysis and hiring-screening systems — and their documented bias
  (Buolamwini & Gebru, 2018, found error rates as high as 1-in-3 for
  darker-skinned women vs. near-perfect for lighter-skinned men).
- Modern LLMs performing translation, summarization, and code generation —
  capabilities that emerged at scale rather than being explicitly programmed.

## Questions I Still Have

- If bias keeps showing up whenever a system learns from historical data,
  is "fix the training data" actually a solvable problem at scale, or is it
  a permanent tax on every ML system built on real-world data?
- Where's the actual line between "emergent capability" and "the model was
  just trained on enough examples of that task to fake it"?

## Connection to Clay Climate AI / My Work

The symbolic-vs-learned tension shows up directly in how I built the Hermes
voice-to-report pipeline: early automation logic was closer to symbolic
rules (if field X is missing, flag it), while the parts that actually work
well now lean on an LLM's learned pattern recognition to interpret messy,
real-world technician speech. The history in this module is basically the
argument for why I didn't try to hand-code every edge case.
