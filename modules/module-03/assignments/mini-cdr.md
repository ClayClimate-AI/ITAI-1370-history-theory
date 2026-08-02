# Mini CDR — Module 03: Games, Prelude to A.I.

## L03 — Scratch Paddle Game

```
Mini CDR — L03: Scratch Paddle Game
|
├── Problem / Prompt
|   └── Build a playable paddle-and-ball game in Scratch (block-based
|       programming), following the professor's tutorial as a starting
|       point for the block/sprite paradigm.
|
├── Approach
|   └── Built three independently-triggered sprites (Ball, Paddle, Line),
|       each with its own `when 🚩 clicked` script, then layered
|       conditional logic and forever loops for movement, paddle tracking,
|       and collision detection on top.
|
├── What worked
|   └── Giving each sprite its own independent trigger instead of one
|       master controller sprite — solved the "everything needs to start
|       at once" requirement cleanly, without an orchestration layer.
|
├── What didn't / had to change
|   └── The score system initially reset to zero on every increment — a
|       competing loop was fighting over the same score variable. Had to
|       trace which scripts were touching score and consolidate to one
|       source of truth.
|
├── What I'd do differently next time
|   └── Add a difficulty ramp (ball speed increasing over time) — right
|       now the game's difficulty is static regardless of how long the
|       player survives.
|
└── Key concept takeaway
    └── Multiple independent, event-triggered scripts touching the same
        shared state (the score variable) is a real coordination hazard —
        visible and debuggable here in a way it often isn't in larger,
        text-based systems.
```

## InClass Assignment — AI-Based Stock News Sentiment Tracker

```
Mini CDR — InClass: AI-Based Stock News Sentiment Tracker
|
├── Problem / Prompt
|   └── Build a tool that fetches real financial news headlines and scores
|       sentiment per stock ticker, with the scoring method explainable
|       rather than a black-box model.
|
├── Approach
|   └── Client-side only: crawl Yahoo Finance RSS per ticker (MSFT, GOOGL,
|       AAPL, TSLA, META), score each headline with weighted keywords +
|       negation detection + intensity modifiers, fall back to curated
|       headlines when CORS blocks live fetching.
|
├── What worked
|   ├── The CORS-proxy + curated-fallback combination means the tool
|   |   still demos correctly even in a sandboxed environment where live
|   |   fetching is blocked — it degrades gracefully instead of breaking.
|   └── Negation detection catches the exact failure mode naive keyword
|       scoring has (e.g. "not profitable" scoring as positive without it).
|
├── What didn't / had to change
|   └── n/a for this pass — documented after the fact from the live
|       deployment and source, not from a build log.
|
├── What I'd do differently next time
|   └── Compare the rule-based score against a real trained sentiment
|       model on the same headlines to quantify what the explainability
|       tradeoff actually costs in accuracy.
|
└── Key concept takeaway
    └── Sentiment scoring doesn't require a trained model — weighted
        keywords, negation handling, and intensity modifiers can get you
        an auditable, explainable classifier that trades some accuracy
        for the ability to show your work on every single score.
```

## A03 (AlphaStar) + Puzzle 03 (Monty Hall)

```
Mini CDR — A03: AlphaStar Limits + Puzzle 03: Monty Hall
|
├── Problem / Prompt
|   ├── A03 — analyze what a superhuman game-playing AI (AlphaStar) still
|   |   *cannot* do, and why.
|   └── P03 — solve the Monty Hall problem and justify the answer using
|       Bayes' Theorem, not just intuition.
|
├── Approach
|   ├── A03 — organized the analysis around four concrete failure modes
|   |   (general intelligence, lifetime adaptation, forward-model
|   |   planning, human-like believability) instead of a vague "AI has
|   |   limits" essay.
|   └── P03 — built an interactive simulator to run the Monty Hall
|       scenario multiple times and watch the probabilities converge,
|       rather than just trusting the formula.
|
├── What worked
|   ├── Grounding each AlphaStar limitation in a specific mechanism (e.g.,
|   |   branching factor vs. Go's, "inner loop" training vs. real-time
|   |   adaptation) instead of restating "it's narrow AI" four ways.
|   └── Running the Monty Hall simulator repeatedly made the 1/3 vs 2/3
|       split concrete — a single playthrough can still "prove" the wrong
|       strategy by luck (Figure 3 shows a Stay win), which is itself a
|       lesson about small-sample intuition vs. the actual long-run math.
|
├── What didn't / had to change
|   └── Early draft of the Monty Hall write-up jumped straight to
|       "switch is better" without showing why the reveal isn't neutral
|       information — had to add the explicit P(B|A) breakdown to make
|       the proof airtight instead of just asserted.
|
├── What I'd do differently next time
|   └── Run the simulator enough times to report an actual empirical win
|       rate next to the theoretical 66.7%, instead of relying on the
|       formula alone.
|
└── Key concept takeaway
    └── Mastery inside a fixed, fully-specified environment (a video game
        with a win condition, a puzzle with a formula) doesn't transfer
        to open-ended, partially-known environments — true for both
        AlphaStar and for naive probability intuition.
```
