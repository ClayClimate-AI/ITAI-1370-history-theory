# Mini CDR — Module 10: NLP – Basics

## A10 — Manual NLP Pipeline

```
Mini CDR — A10: Manual NLP Pipeline
|
├── Problem / Prompt
|   └── Manually implement a full NLP pipeline (clean → tokenize → stop
|       words → stem → POS tag 20+ tokens → vectorize) on a self-selected
|       corpus, without automated NLP libraries.
|
├── Approach
|   └── Chose a corpus I actually knew well — the AlexNet paragraph from
|       my own A01 essay — so I could sanity-check every pipeline output
|       against text I'd already thought carefully about, instead of a
|       corpus with unfamiliar edge cases.
|
├── What worked
|   ├── Leaving stemming's non-word fragments ("decis," "viabil") in the
|   |   final report instead of cleaning them up — an honest result
|   |   teaches the actual speed/accuracy tradeoff better than a tidy one.
|   └── Reporting token counts at each stage (98 → 75 unique → 61 after
|       stop words) made the pipeline's effect measurable, not just
|       described.
|
├── What didn't / had to change
|   └── n/a — manual step-by-step exercise, no revision needed once each
|       stage was worked through correctly.
|
├── What I'd do differently next time
|   └── Run the same pipeline on a second, longer corpus to see whether
|       the ~1/3 stop-word reduction rate holds, or was specific to this
|       particular paragraph's structure.
|
└── Key concept takeaway
    └── Every stage of the pipeline exists to make the next one possible
        — cleaning enables tokenizing, tokenizing enables stop-word
        filtering, filtering enables stemming/POS tagging, and all of it
        exists to produce the one thing a model can actually use:
        a numeric vector.
```

## Lab 10 — IBM Watson Chatbot (Lendyr Demo)

```
Mini CDR — Lab 10: IBM Watson Chatbot (Lendyr Demo)
|
├── Problem / Prompt
|   └── Research Watson Assistant, explore the Lendyr Demo, and analyze
|       its UI/UX — interface design, ease of use, response handling,
|       including unexpected/off-script questions.
|
├── Approach
|   └── Explored both the customer-facing Lendyr chat AND the underlying
|       trial builder (action setup, integrations catalog, phone/voice
|       config) to assess the platform from both the user's and the
|       business's side, not just the polished demo surface.
|
├── What worked
|   └── Deliberately testing an off-script path ("Modify in progress
|       application") instead of only following the happy path — that's
|       what surfaced the real limitation (agent-offline dead end) rather
|       than a purely positive review of the scripted demo flow.
|
├── What didn't / had to change
|   └── n/a — exploratory assignment, no revision needed.
|
├── What I'd do differently next time
|   └── Test whether Watson Assistant's Search feature (shown in IBM's
|       own tutorial) could have actually caught the dead-end request if
|       the demo had been configured with a knowledge base behind it.
|
└── Key concept takeaway
    └── Watson Assistant is a construction kit, not a ready-made
        assistant — its intelligence is entirely a function of what a
        business explicitly builds. That's real enterprise flexibility,
        but it also means every unbuilt path is a hard dead end, not a
        graceful fallback.
```

