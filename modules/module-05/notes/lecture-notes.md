# Module 05 — ML Lifecycle / Computational Humor

**Topic Area:** ML Process
**Note:** Backfilled from the completed L05 (Computational Humor) report,
not written live during lecture.

---

## Key Concepts

- **Humor has a mechanical skeleton.** A joke is two valid interpretations
  of the same sentence colliding — an algorithm can verify a setup is
  specific and that a word carries dual meaning, but it can't predict
  whether a given audience's life experience will make the connection land.
- **Template-based vs. emergent humor generation.** JAPE hand-builds
  linguistic schemas over a structured lexicon (rigid, narrow, but
  reliably grammatical). GPT-3 produces humor as an emergent side effect of
  next-token prediction over massive text (flexible, but inconsistent and
  with no real grasp of *why* something is funny). Bard/Gemini sits between
  the two — instruction-tuned with RLHF, conversational, can explain a
  joke's mechanism, still shares LLM caveats.
- **The evaluation gap.** Pattern-matching (does the setup create a clear
  expectation? does the key word support two readings?) is something a
  rule-based system can check. Whether the joke actually lands depends on
  the listener's own background — that part isn't measurable from the joke
  text alone.

## Manual Joke Algorithm (as a tree)

```
Manual Joke Algorithm
|
├── Start: pick an everyday scenario
|   └── "Working as a banker"
|
├── Does the setup create a clear expectation?
|   ├── No → make the setup more specific (name the exact job)
|   └── Yes → continue
|
├── Is there an unexpected twist?
|   ├── No → add an incongruity (borrow a term from that field)
|   └── Yes → continue
|
├── Apply technique: category shift
|   └── "interest" = job term (finance) + feeling (losing interest)
|
└── Deliver setup + punchline
    "I used to be a banker, but I lost interest."
    (technique: incongruity — one word, two valid readings)
```

## Vocabulary

| Term | Definition |
|---|---|
| JAPE | Joke Analysis and Production Engine — hand-built linguistic schemas over a structured lexicon; produces punning Q&A riddles via a fixed template |
| Incongruity (humor theory) | The comedic technique of setting up one expected reading of a word/situation, then resolving with a second, unexpected valid reading |
| RLHF (recap) | Used in Bard/Gemini's instruction-tuning; same mechanism from Module 04, applied here to conversational humor generation |

## Real-World Applications

- Computational humor research feeds directly into conversational AI
  tone/personality tuning — the same "does this land with a general
  audience" evaluation problem shows up in any consumer-facing chatbot.

## Questions I Still Have

- Is there any measurable proxy for "will this land with this specific
  audience" that isn't just... asking a human, the way I had to for this
  assignment?

## Connection to Clay Climate AI / My Work

The evaluation gap is the same lesson as Module 04's RLHF discussion: a
system can verify mechanical correctness (grammar, structure, a template
being followed) but can't verify whether the output actually serves the
person receiving it. That's exactly why the Hermes report pipeline still
needs a human review step before a generated report goes out — mechanically
correct isn't the same as actually useful to the tech reading it.
