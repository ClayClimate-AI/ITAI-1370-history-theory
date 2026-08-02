# Module 03 — Games, Prelude to A.I.

**Topic Area:** Reinforcement Learning / Games
**Note:** Backfilled from four real Canvas items — the InClass Stock News
Sentiment Tracker (added last-minute by the professor, separate from the
formal lab), A03 (AlphaStar limitations report), L03 (Scratch Paddle
Game — confirmed by Joe: this is the real L03 submission, not the Stock
Tracker), and Puzzle 03 (Monty Hall / Bayes' Theorem).

---

## InClass Assignment (Jun 10, 2026) — AI-Based Stock News Sentiment Tracker

Confirmed via the live deployment (l03-josephclay-itai1370.netlify.app,
fetched and read this session) and the local HTML source
(`L03_JosephClay_TuringCollective_ITAI1370.html`).

### Key Concepts
- **Client-side sentiment scoring**, no server/backend — headlines are
  fetched, scored, and displayed entirely in the browser.
- **Weighted keyword scoring + negation detection + intensity modifiers**
  is the actual scoring method — not a trained ML classifier. Sentiment is
  computed as a rule-based score from -100 to +100, not learned from data.
- **Graceful degradation**: a curated-headline fallback exists for when
  CORS policies block live RSS fetching — the tool still functions in a
  sandboxed/restricted environment instead of failing outright.

### Vocabulary
| Term | Definition |
|---|---|
| Sentiment score | A -100 to +100 value classifying text as Positive/Negative/Neutral, here computed via weighted keywords rather than a trained model |
| Negation detection | Catching phrases like "not profitable" so a positive keyword inside a negated phrase doesn't get miscounted as positive |
| CORS proxy | A workaround for browser cross-origin restrictions that would otherwise block client-side fetching of Yahoo Finance RSS feeds |

### Real-World Applications
Rule-based sentiment scoring is a real, still-used alternative to trained
NLP classifiers when explainability matters — every score here can be
traced back to a specific keyword/modifier, unlike a black-box model
output.

## L03 — Scratch Paddle Game

Confirmed via `Ready_For_Submission/L03_TuringCollective_JosephClay_ITAI1370.docx`.
Live at scratch.mit.edu/projects/1331568586.

### Key Concepts
- **Block-based programming makes control flow visible.** Conditional
  statements and forever loops control the Ball, Paddle, and Line sprites
  independently — each sprite gets its own `when 🚩 clicked` trigger so all
  three activate simultaneously at game start, rather than depending on
  execution order.
- **Debugging a shared-state race condition.** The score system broke
  because a competing loop was resetting the score to zero on every
  increment — a concrete, hands-on encounter with the same "two processes
  fighting over shared state" bug class that shows up in real software,
  just visible as draggable blocks instead of text.
- **Collision detection drives game logic.** The Line sprite's sole job is
  detecting ball contact and triggering a full stop + score reset — game
  logic here is really a small event-driven state machine (ball moving →
  paddle hit → score++; ball hits line → stop everything → reset).

### Sprites & Logic (as a tree)

```
Scratch Paddle Game
|
├── Ball (when 🚩 clicked)
|   └── Moves and bounces; increments score on paddle touch
|
├── Paddle (when 🚩 clicked)
|   └── Tracks mouse x position; player-controlled
|
└── Line — Red (when 🚩 clicked)
    └── Detects ball collision → stops all scripts → resets score
```

### Vocabulary
| Term | Definition |
|---|---|
| Block-based programming | Visual programming using draggable logic blocks instead of text syntax — Scratch's paradigm |
| Race condition | Two processes competing over the same shared state (here: two loops both writing to the score variable) producing incorrect results |
| Event-driven trigger | Code that runs in response to an event (`when 🚩 clicked`) rather than top-to-bottom sequential execution |

### Real-World Applications
Block-based environments like Scratch are widely used as the first
programming environment in K-12 CS education specifically because they
make control flow and event-driven logic visible and draggable — the same
concepts (loops, conditionals, triggers, shared state bugs) transfer
directly to text-based languages.

## A03 — AlphaStar Limitations + Puzzle 03 — Monty Hall

### Key Concepts

- **Artificial Narrow Intelligence (ANI)** — AlphaStar beats grandmasters at
  StarCraft II but can't play checkers or tie a shoelace. Mastering one
  closed environment isn't general intelligence; it's a system tuned to a
  specific dataset and rule set.
- **Lifetime adaptation** — humans can change tactics mid-match when
  ambushed. Deep RL agents like AlphaStar can't; their strategy is fixed by
  training across millions of prior games and needs expensive re-training to
  handle anything outside that learned distribution.
- **Fast forward models** — Go's branching factor is small enough for tree
  search to look many moves ahead. StarCraft II's branching factor is orders
  of magnitude larger, so AlphaStar has to rely on heuristics and
  approximations instead of perfect lookahead.
- **Bayes' Theorem in practice (Monty Hall)** — new information (Monty
  deliberately revealing a goat) changes the probability distribution over
  what's left. The reveal isn't random, so it transfers 2/3 probability onto
  the remaining door instead of splitting evenly.

### The Algorithm (Monty Hall, as a tree)

```
Monty Hall Decision
|
├── Initial pick (before any reveal)
|   └── Each door: P = 1/3 (uniform prior)
|
├── Monty reveals a goat (deliberate, not random)
|   ├── Never opens your door
|   ├── Never opens the car door
|   └── This action transfers probability, it doesn't split it evenly
|
└── Decision point
    ├── Stay → P(car) stays frozen at 1/3
    |   (your door was chosen before any information existed)
    └── Switch → P(car) = 2/3
        (the unopened door absorbs the full remaining probability)
```

### Vocabulary

| Term | Definition |
|---|---|
| ANI (Artificial Narrow Intelligence) | AI competent in one closed domain, with no ability to generalize outside it |
| Lifetime adaptation | The ability to change strategy mid-episode in response to novel events, without re-training |
| Branching factor | The number of possible next moves/actions at each decision point — drives how feasible tree search/lookahead is |
| Bayes' Theorem | P(A\|B) = [P(B\|A) × P(A)] / P(B) — how a prior probability updates given new evidence |
| Prior / posterior | Belief before new evidence (prior) vs. belief after incorporating it (posterior) |

### Real-World Applications

- Game-playing AI (AlphaStar, AlphaGo) as the proving ground for RL
  techniques that later generalize to robotics and multi-agent coordination.
- Bayesian updating underlies spam filters, medical diagnosis systems, and
  recommendation engines — same math as Monty Hall, higher stakes.

## Questions I Still Have

- What would it actually take architecturally to give an RL agent real
  lifetime adaptation instead of needing full re-training?
- The Scratch score-reset bug (L03) and AlphaStar's brittleness (A03) are
  both "shared/learned state behaving unexpectedly" bugs at wildly
  different scales — is there a unifying way to think about debugging
  state issues that applies whether the state is a Scratch variable or a
  trained network's weights?

## Connection to Clay Climate AI / My Work

The "lifetime adaptation" limitation is the most directly relevant concept
here — a model trained on historical HVAC service-call patterns is brittle
the same way AlphaStar is: it performs well inside its learned distribution
and needs retraining, not graceful adaptation, when it meets a genuinely
novel failure mode it never saw in training data. The Stock Sentiment
Tracker's rule-based scoring (weighted keywords, not a trained model) is
also directly relevant — it's the same "explainable rules vs. opaque model"
tradeoff I navigate in the Hermes pipeline. And the Scratch race-condition
bug (two loops fighting over the score variable) is a smaller-scale version
of exactly the kind of state bug I've had to hunt down in the Hermes
pipeline when two automation steps both tried to write the same field.
