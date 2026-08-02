# Worked Example — Forward Pass + Backprop (from A07)

Not literal code — this is the network's math worked by hand for one
training example (RTU-04), pulled from the A07 deck, documented here as a
reusable reference for the mechanics of forward propagation and gradient-
based learning.

## Network architecture

```
4 input features → Hidden Layer 1 (4 neurons) → Hidden Layer 2 (3 neurons) → 2 output classes
```

## Input (RTU-04, normalized before entry)

| Feature | Raw value | Signal |
|---|---|---|
| x1 — Unit Age | 15 yrs | VERY HIGH — pushes toward failure |
| x2 — Days Since Last Service | 30 days | LOW — freshly maintained, protective |
| x3 — Avg Ambient Temp | 95°F | ELEVATED — Houston summer load |
| x4 — Fault Codes (last 90d) | 1 | LOW — minor signal only |

## Forward pass

Each hidden neuron: `z = Σ(wᵢ·xᵢ) + b`, then ReLU: `f(z) = max(0, z)`.

Dominant route for this input: `age(15) → h1.1 → h2.1 ("Wear & Neglect") →
WILL FAIL`, since age carried the largest weights going in.

Output (softmax over the two classes):

```
P(WILL FAIL)     = 0.74
P(WILL NOT FAIL) = 0.26
```

**Prediction: WILL FAIL within 30 days (74% confidence)** — driven almost
entirely by Unit Age through the h1.1 → h2.1 path.

## Reality check

Actual outcome: **DID NOT FAIL**. Error = 0.74.

## Backpropagation (gradient descent: `w ← w − η·∂E/∂w`)

| Connection | Direction | Why |
|---|---|---|
| Age → h1.1 | WEAKENED | Was "the loudest voice" — drove a confident wrong answer, so gradient assigns it the largest share of blame |
| Days-Since-Service → h1.2 | STRENGTHENED | The true protective signal the network under-weighted |
| h2.1 "Wear & Neglect" → WILL FAIL | MODERATED | Stays useful, but its vote toward failure is tempered so age alone can't dominate |

**After learning:** re-running RTU-04 yields `P(fail) ≈ 0.41` → prediction
flips to WILL NOT FAIL. The network learned the interaction "old AND
recently-serviced ≠ old AND neglected" — something no single weight could
express before the correction.
