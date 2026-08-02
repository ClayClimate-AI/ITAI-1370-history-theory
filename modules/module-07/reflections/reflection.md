# Reflection — Module 07: Deep Learning – Neural Networks

## L07 — TensorFlow Playground

**What challenged me this module:**
Isolating one variable at a time across five tasks while holding everything
else constant — it's tempting to change multiple settings at once when
exploring a tool, but that makes it impossible to attribute the result to
anything specific.

**What clicked that didn't before:**
The learning-rate task was the real surprise: a 100× more aggressive rate
actually *won* on this dataset (0.006 vs 0.020 test loss). I expected
"aggressive learning rate = worse," and the honest result forced me to
write the more careful conclusion — that this is a property of easy, clean
data tolerating recklessness, not evidence that bigger learning rates are
generally better.

**How I'd explain this concept to someone who knows nothing about AI:**
A neural network with too few neurons can't bend its decision boundary
around a circular pattern — it just draws something close to a straight
line and gets it wrong a third of the time. Give it more neurons and it
traces the circle almost perfectly. More "capacity" isn't about being
smarter in the abstract, it's about having enough moving parts to match
the shape of the problem.

**One thing I want to go deeper on:**
Why XOR is specifically the case that breaks single-layer perceptrons
(Minsky & Papert's 1969 critique) — I can state that it's non-linearly
separable, but I want to be able to show why geometrically, not just cite
it.

**How this connects to the broader AI landscape:**
Task 5 (dataset complexity) is the whole argument for why image and speech
models need deep, specialized architectures instead of small generic
ones — the same 4-neuron network that solved Gaussian blobs perfectly
couldn't touch the spiral. Capacity has to match the problem, every time.

## A07 — Predicting HVAC Failures with a Neural Network

**What challenged me this module:**
Making the backprop step honest instead of hand-wavy. It's easy to say "the
network learns from its mistakes" — it's harder to actually walk through
which specific weight gets blamed for a wrong answer and why, in a way that
holds up to the real math (gradient of the error with respect to that
weight) instead of just asserting it.

**What clicked that didn't before:**
The RTU-04 example only works as a teaching case because it's genuinely
ambiguous — an old unit (high risk) that was just serviced (protective
signal). The network's first pass over-trusted age and got a confident
wrong answer. That's not a flaw in the demo, that's the entire point: a
single miss on a genuinely tension-filled example is what makes
backpropagation's blame-assignment visible instead of abstract.

**How I'd explain this concept to someone who knows nothing about AI:**
The network looked at an old air conditioner that had just been serviced
and got fixated on "old = bad," predicting it would fail. It was wrong. So
the network adjusted: it trusted "old" a little less and "recently
serviced" a little more. Do that thousands of times across real examples,
and it stops overreacting to any single feature and starts weighing them
together the way an experienced tech actually would.

**One thing I want to go deeper on:**
How the learning rate η actually gets chosen in practice (this deck names
the tradeoff — too large overshoots, too small crawls — but not how you'd
tune it for a real, noisy field dataset instead of five illustrative rows).

**How this connects to the broader AI landscape:**
This is Module 01's symbolic-vs-learned tension made completely concrete:
no human wrote a rule saying "age 15 AND serviced within 30 days = don't
flag." The network had to learn that interaction from a wrong prediction.
That's the whole argument for why deep learning displaced hand-coded expert
systems — some interactions are too subtle to enumerate by hand but emerge
naturally from enough labeled examples and a big enough miss.
