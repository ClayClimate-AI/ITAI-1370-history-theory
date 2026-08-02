# Module 10 — NLP: Basics — A10 Notes

**Note:** Backfilled from the completed A10 (Manual NLP Pipeline)
submission, not written live during lecture.

---

## Key Concepts

- **Each pipeline stage exists to make the next one possible.** Cleaning
  produces text a tokenizer can split reliably; tokenizing produces units
  a stop-word filter can check; stop-word removal concentrates the list
  on topical words a stemmer can normalize; normalization feeds POS
  tagging and, ultimately, vectorization — the step every downstream ML
  algorithm actually needs, since computers can't do math on raw words.
- **Stop words are structural filler, not noise.** Removing them dropped
  this corpus from 98 to 61 tokens — over a third of ordinary English
  text is function words ("the," "and," "of") carrying grammatical
  structure but no topic-specific meaning.
- **Stemming trades accuracy for speed.** Simple suffix-stripping
  produces real dictionary roots sometimes ("computing" → "comput" is
  close) but non-words other times ("decisive" → "decis," "viability" →
  "viabil"). It also can't handle irregular forms ("came," "won," "built"
  passed through unchanged) — lemmatization would need a reference
  lexicon to correctly reduce "came" to "come."
- **POS tags disambiguate role, not just word identity.** The same token
  ("processing," "learning") can function as a noun or an adjective/verb
  form depending on context — without POS tagging, an NLP system treats
  every occurrence identically and loses that grammatical information.

## The Pipeline (as a tree)

```
A10 — Manual NLP Pipeline (corpus: AlexNet paragraph, from Joe's own A01 essay)
|
├── 1. Corpus selection
|   └── One paragraph, 2012 AlexNet breakthrough — short, topic-relevant
|
├── 2. Cleaning
|   └── Lowercased, stripped punctuation/numbers/hyphens
|
├── 3. Tokenization
|   └── Split on whitespace → 98 total tokens, 75 unique
|
├── 4. Stop word removal
|   └── 22-word stop list applied → 61 total tokens, 58 unique
|       (over 1/3 of the corpus was structural filler)
|
├── 5. Stemming
|   └── Manual suffix-stripping → real roots ("call," "unit") and
|       non-word fragments ("decis," "reorgan," "viabil") side by side;
|       irregular verbs (came/won/built) left unchanged
|
├── 6. POS tagging
|   └── 20+ tokens manually tagged (nouns, verbs, adjectives, proper
|       nouns, gerunds) using pre-stemmed forms for clarity
|
└── 7. Vectorization
    └── Manual Count Vectorization on a 21-word subset →
        21-dimension vector, all counts = 1 except "percent" = 2
```

## Vocabulary

| Term | Definition |
|---|---|
| Stemming | Rule-based suffix-stripping to normalize word forms — fast, but can produce non-dictionary fragments |
| Lemmatization | Dictionary/grammar-based reduction to a word's true root — more accurate than stemming, requires a reference lexicon |
| POS tagging | Labeling each token with its grammatical role (noun, verb, adjective, etc.) |
| Count Vectorization | Converting a token list into a numeric vector by counting occurrences of each vocabulary word |

## Real-World Applications

- Search engines and document similarity (cosine similarity over
  vectorized text) both depend on the exact pipeline built here by hand.
- Any downstream classifier or clustering algorithm requires vectorized
  input — this pipeline is the manual version of what libraries like
  spaCy/NLTK automate.

## Questions I Still Have

- At what corpus size does manual stemming's error rate (non-word
  fragments) actually start costing real accuracy in a downstream task,
  versus just being a cosmetic imperfection?

## Connection to Clay Climate AI / My Work

Using my own A01 essay paragraph as the corpus wasn't just convenient —
it's the same kind of text (technical, domain-specific prose) the Hermes
pipeline has to process from real HVAC service transcripts. Watching stop
words cut the token count by a third by hand is a concrete reminder of
why that preprocessing step matters before anything gets vectorized or
matched downstream.
