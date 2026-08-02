# Mini CDR — Module 05: Machine Learning – The Data

Module 05 covers two Canvas items: A05 (ChatGPT Research & Interaction)
and L05 (Computational Humor). Kept separate below since they're distinct
deliverables with distinct grades (98% and 95%).

## A05 — ChatGPT Research & Interaction

```
Mini CDR — A05: ChatGPT Research & Interaction
|
├── Problem / Prompt
|   └── Research how ChatGPT works (training stages, applications), then
|       directly interact with it across six questions spanning ML
|       fundamentals, self-critique, code generation, and a hypothetical
|       redesign — and critically analyze the responses for accuracy,
|       human-likeness, and limitations.
|
├── Approach
|   └── Picked six questions to deliberately span categories (a factual
|       ML definition, a self-critical limitations question, a real-world
|       bias/ethics question, a code-generation task, a taxonomy
|       question, and an open-ended hypothetical) instead of six similar
|       factual questions, so the analysis would surface different kinds
|       of behavior.
|
├── What worked
|   ├── Asking the model to critique its own limitations (Q2) and
|   |   redesign itself (Q6) produced more genuinely useful signal than
|   |   any purely factual question — it's where the gap between
|   |   "sounds confident" and "is calibrated" showed up clearest.
|   └── Running the actual Fibonacci code instead of just accepting it as
|       correct caught a real, if minor, gap: no test cases, no
|       complexity note.
|
├── What didn't / had to change
|   └── Nothing needed correcting in the responses themselves (all six
|       were factually accurate), but the first draft of the analysis
|       under-weighted the "uniformly confident tone" observation — that
|       turned out to be the most important finding, so I expanded it.
|
├── What I'd do differently next time
|   └── Add a question specifically designed to trigger a hallucination
|       (something obscure or post-cutoff) instead of only asking
|       questions the model was likely to answer well.
|
└── Key concept takeaway
    └── RLHF is what separates a raw next-word predictor from something
        that reads as "helpful" — but it optimizes for *sounding*
        aligned with human preference, not for the model knowing when
        it's uncertain. Those are different problems, and only one of
        them RLHF actually solves.
```

## L05 — Computational Humor

```
Mini CDR — L05: Computational Humor
|
├── Problem / Prompt
|   └── Research three computational humor systems (purpose, mechanism,
|       strengths/limitations), design a manual joke-generation
|       algorithm, produce a sample joke, and evaluate it with a real
|       human audience.
|
├── Approach
|   ├── Picked systems spanning three different eras/approaches (JAPE's
|   |   rigid hand-built templates, GPT-3's emergent next-token humor,
|   |   Bard/Gemini's RLHF-tuned conversational humor) so the comparison
|   |   would show an actual evolution, not three similar systems.
|   └── Built the joke algorithm as an explicit decision tree (scenario →
|       clear expectation? → twist? → apply incongruity → deliver)
|       instead of writing a joke first and reverse-engineering a
|       process to match.
|
├── What worked
|   ├── Testing the joke on three real people instead of just asserting
|   |   it was funny — the split between Sarah/Jason (banking
|   |   background, rated it higher) and David (understood it, rated it
|   |   lower, read into the metaphor instead) is a real finding, not
|   |   something predictable from the algorithm alone.
|   └── Framing the algorithm as decision points rather than a fixed
|       script made it reusable — the same steps work for a different
|       scenario, not just the banker joke.
|
├── What didn't / had to change
|   └── Nothing had to be revised after audience feedback (the joke
|       worked well enough across all three respondents), but the
|       reflection had to be rewritten once I noticed David's response
|       wasn't really about the joke's mechanics — that observation
|       became the strongest part of the analysis.
|
├── What I'd do differently next time
|   └── Test two different jokes from the same algorithm with the same
|       audience, to see whether the algorithm's success rate is
|       consistent or if I got lucky with this specific scenario/word
|       pair.
|
└── Key concept takeaway
    └── An algorithm can verify a joke's mechanical structure (specific
        setup, a word carrying two valid readings) but can't predict
        whether a given audience's background will make the connection
        feel obvious, forced, or accidentally meaningful — the mechanics
        are computable, the impact isn't.
```
