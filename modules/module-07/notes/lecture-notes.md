# Module 07 — Deep Learning – Neural Networks

**Topic Area:** Neural Network fundamentals (real Canvas module title)
**Note:** Backfilled from two real Canvas items — A07 ("Predicting HVAC
Failures with a Neural Network") and L07 (TensorFlow Playground technical
report — the real submission, not the requirements template that was
previously the only file in this module). Not written live during lecture.

---

## L07 — TensorFlow Playground

Real 5-task technical report, confirmed via
`assignments/Ready_For_Submission/L07_TuringCollective_JosephClay_ITAI1370.docx`.

### Key Concepts (from the actual experiments run)

- **Activation function shapes the decision boundary, not just the loss.**
  ReLU (piecewise-linear) produced sharp, polygonal boundaries and drove
  training loss to 0.000; sigmoid produced smooth, rounded boundaries and
  converged slightly less tightly (0.016 vs 0.012 test loss). Both solved
  the problem — the difference only becomes disqualifying in deeper
  networks, where sigmoid's flat tails cause vanishing gradients.
- **Capacity must match the pattern.** 2 hidden neurons on a circular
  dataset underfit to a nearly straight line (test loss 0.308); 8 neurons
  cut that to 0.009 — a 30× improvement from capacity alone, no other
  change.
- **Learning rate is a speed/stability tradeoff, not "bigger is better."**
  A 100× increase in learning rate (0.03 → 3) converged faster *and*
  better on this clean, simple dataset (0.006 vs 0.020) — but the report
  explicitly flags this as reading "this easy problem tolerated an
  aggressive rate," not evidence that aggressive rates generalize as a
  good idea on harder data.
- **Noisy data caps achievable accuracy regardless of model quality.**
  Noise 0 → test loss 0.007; Noise 30 → test loss 0.170, a 24× jump, as
  the network started chasing mislabeled outliers (memorizing noise
  instead of the true pattern).
- **Dataset complexity determines required network capacity.** The same
  4-neuron network went from perfect (Gaussian blobs, 0.000 loss) to
  unusable (Spiral, 0.485 loss) with zero architecture changes — XOR
  (0.178) is the textbook case: famously unsolvable by a single-layer
  perceptron (Minsky & Papert, 1969), only partially solved even here.

### Results Table (all 5 tasks)

| Task | Configuration A | Configuration B | Result |
|---|---|---|---|
| 1. Activation | ReLU: loss 0.012, sharp boundary | Sigmoid: loss 0.016, smooth boundary | Both work; ReLU tighter |
| 2. Neuron count | 2 neurons: loss 0.308 (underfit) | 8 neurons: loss 0.009 | 30× improvement from capacity |
| 3. Learning rate | 0.03: loss 0.020, gradual | 3 (100× higher): loss 0.006, near-instant | Risky but won on this easy data |
| 4. Noise | Noise 0: loss 0.007 | Noise 30: loss 0.170 | 24× worse from noise alone |
| 5. Dataset | Gaussian: 0.000 (perfect) | XOR: 0.178 / Spiral: 0.485 (fails) | Capacity must match data complexity |

### Vocabulary (L07-specific)

| Term | Definition |
|---|---|
| Decision boundary | The learned line/curve separating predicted classes — its shape (sharp vs. smooth, tight vs. warped) is diagnostic evidence of what the network learned |
| Underfitting | Too little model capacity for the pattern — visible here as a 2-neuron network collapsing to a near-straight line on curved data |
| XOR problem | The classic non-linearly-separable pattern (Minsky & Papert, 1969) that a single-layer perceptron provably cannot solve |

## A07 — Predicting HVAC Failures with a Neural Network

### Key Concepts

- **Depth builds abstraction.** Hidden Layer 1 detects simple feature
  combinations (age is high, service is recent); Hidden Layer 2 composes
  those into higher-level "risk concepts" (wear & neglect, thermal stress,
  early warning). A single linear model can't capture an interaction like
  "old AND neglected" — depth is what makes that possible.
- **ReLU over sigmoid is a design decision, not a default.** ReLU avoids
  saturating gradients on positive inputs, which keeps error signals strong
  during training in deeper stacks (Nair & Hinton, 2010).
- **A confident wrong answer is still useful.** The network predicted 74%
  WILL FAIL on RTU-04 and was wrong — that miss is exactly the signal
  backprop needs; the error becomes proportional weight updates, not wasted
  effort.
- **Backprop assigns blame proportionally.** The connection that was "the
  loudest voice" driving the wrong answer (Age → h1.1) gets weakened the
  most; the under-weighted true signal (Days-Since-Service → h1.2) gets
  strengthened. This isn't intuition — it's the gradient of the error with
  respect to each weight.
- **Representation quality bounds model quality.** The four input features
  were chosen for domain relevance (each has a known mechanical failure
  pathway) and availability (already captured on routine service calls) —
  the network can only ever learn patterns present in the features it's
  given.

### The Forward Pass → Learning Loop (as a tree)

```
RTU-04 Case Study
|
├── Input Layer (normalized 0-1)
|   ├── x1 Unit Age = 15 yrs        → VERY HIGH risk signal
|   ├── x2 Days Since Service = 30  → LOW risk (protective)
|   ├── x3 Avg Ambient Temp = 95°F  → ELEVATED
|   └── x4 Fault Codes (90d) = 1    → LOW
|
├── Forward propagation
|   ├── Hidden Layer 1 (4 neurons): z = Σ(wᵢ·xᵢ) + b, then ReLU
|   |   └── h1.1 weights Unit Age heavily (dominant this pass)
|   ├── Hidden Layer 2 (3 neurons): composes h1 outputs into concepts
|   |   └── h2.1 "Wear & Neglect" — dominant route: age(15) → h1.1 → h2.1
|   └── Output Layer: softmax → [0.74 WILL FAIL, 0.26 WILL NOT FAIL]
|
├── Reality check
|   └── Actual outcome: DID NOT FAIL → Error = 0.74
|
└── Backpropagation (gradient descent, w ← w − η·∂E/∂w)
    ├── Age → h1.1 (loudest voice, drove the wrong answer) → WEAKENED
    ├── Days-Since-Service → h1.2 (under-weighted true signal) → STRENGTHENED
    └── h2.1 "Wear & Neglect" → WILL FAIL → MODERATED
        └── Re-run RTU-04 → P(fail) ≈ 0.41 → prediction flips to WILL NOT FAIL
```

### Vocabulary (A07-specific)

| Term | Definition |
|---|---|
| Feed-forward network | A network where information flows one direction, input → hidden layers → output, with no loops |
| Weighted sum | z = Σ(wᵢ·xᵢ) + b — each neuron's raw input before activation; a weighted vote over its inputs plus a bias |
| ReLU | f(z) = max(0, z) — an activation function chosen to keep gradients strong in deep stacks, vs. sigmoid's saturation problem |
| Softmax | Converts raw output scores into probabilities that sum to 1 (e.g., [0.74, 0.26]) |
| Backpropagation | Uses the chain rule to compute ∂Error/∂w for every weight — how much each connection contributed to a wrong prediction |
| Gradient descent | The update rule w ← w − η·∂E/∂w; learning rate η controls step size (too large overshoots, too small crawls) |
| Overfitting | When a model memorizes training examples instead of generalizing — guarded against with a held-out validation set |

### Real-World Applications

- Predictive maintenance on commercial RTUs and chillers.
- Cleanroom environmental-monitoring anomaly detection (pharma/biotech
  HVAC) — same architecture pattern, different domain.
- Smart-building BAS optimization; dispatch prioritization from live
  fault-code telemetry.

## Questions I Still Have

- With only 5 labeled examples in this illustrative dataset, how many real
  labeled service records would actually be needed before this architecture
  stopped being dominated by a single feature (age) and started reliably
  weighing the interaction terms?
- L07's Task 3 finding (100× learning rate won on easy data) — at what
  point does a dataset stop being "easy" enough to tolerate that, and is
  there a way to detect that threshold besides trial and error?

## Connection to Clay Climate AI / My Work

This is the most direct crossover in the whole course — the RTU failure
predictor is built on the exact failure-mode data I already know from field
work (age, days since service, ambient load, fault codes), and the
Discussion Points section explicitly names cleanroom environmental
monitoring and BAS optimization as applications of this same architecture.
This is a legitimate blueprint for a future Clay Climate AI feature, not
just a classroom exercise.
