# Mini CDR — Module 07: Deep Learning – Neural Networks

## L07 — TensorFlow Playground

```
Mini CDR — L07: TensorFlow Playground
|
├── Problem / Prompt
|   └── Run 5 exploration tasks in TensorFlow Playground (activation
|       functions, hidden-layer neuron count, learning rate, data noise,
|       dataset complexity), documenting configuration, results, and what
|       was learned for each.
|
├── Approach
|   └── Held every variable constant except the one being tested per task,
|       using the same base network (1 hidden layer, 4 neurons, circle
|       dataset) as the control, so each result could be attributed to
|       exactly one changed parameter.
|
├── What worked
|   ├── Running actual epoch/loss numbers for every configuration (not
|   |   just describing results qualitatively) made the "30× improvement,"
|   |   "24× worse," and "100× learning rate" comparisons concrete and
|   |   checkable instead of impressionistic.
|   └── Testing 3 additional datasets in Task 5 (Gaussian, XOR, Spiral)
|       against the SAME fixed network tied directly back to Task 2's
|       capacity lesson — capacity that's optional for easy data becomes
|       mandatory for hard data.
|
├── What didn't / had to change
|   └── The learning-rate task (Task 3) initially risked reading as "bigger
|       learning rate = better" from the raw numbers alone; had to add the
|       explicit caveat that this result is specific to easy, clean data
|       and not a general recommendation.
|
├── What I'd do differently next time
|   └── Report an actual empirical measurement of *when* an aggressive
|       learning rate starts to fail (by increasing noise or dataset
|       complexity) instead of stating the risk only in the abstract.
|
└── Key concept takeaway
    └── A neural network's success isn't a property of the network alone —
        it's the fit between architecture, hyperparameters, and data. The
        same 4-neuron network went from perfect (Gaussian, 0.000 loss) to
        nearly useless (Spiral, 0.485 loss) with no change except the data.
```

## A07 — Predicting HVAC Failures with a Neural Network

```
Mini CDR — A07: Predicting HVAC Failures with a Neural Network
|
├── Problem / Prompt
|   └── Build a PowerPoint exploring deep learning by designing a
|       simulated feed-forward network for a real problem, showing the
|       architecture, a worked forward pass, and how backpropagation
|       updates weights after a wrong prediction.
|
├── Approach
|   ├── Chose a domain I actually know (commercial RTU failure
|   |   prediction) instead of a generic textbook example, so every
|   |   design choice (which 4 input features, why ReLU, what the
|   |   hidden-layer "concepts" mean) could be justified against real
|   |   field knowledge, not just cited theory.
|   └── Deliberately picked a worked example (RTU-04) where the features
|       conflict — old unit, but just serviced — so the network would
|       actually get it wrong and the backprop step would have something
|       real to demonstrate.
|
├── What worked
|   ├── Using a genuinely ambiguous example instead of an easy one made
|   |   the learning step meaningful — a network that predicts correctly
|   |   on the first try doesn't teach you anything about how backprop
|   |   assigns blame.
|   └── Naming the hidden-layer neurons as interpretable concepts ("Wear
|       & Neglect," "Thermal Stress," "Early Warning") made hierarchical
|       representation tangible instead of abstract math.
|
├── What didn't / had to change
|   └── Early framing treated the four input features as self-evidently
|       correct; had to go back and add the domain justification for
|       each one (mechanical failure pathway + availability on routine
|       service calls) so the choice wasn't just asserted.
|
├── What I'd do differently next time
|   └── Show what happens with a second training example after the
|       RTU-04 update, to demonstrate the weights continuing to converge
|       rather than stopping the story at one correction.
|
└── Key concept takeaway
    └── A neural network doesn't need a human to write the rule "old AND
        recently-serviced = lower risk" — it derives that interaction
        from a single wrong, confident prediction and the gradient of
        that error. That's the practical argument for learned systems
        over hand-coded rules when the interactions are too subtle to
        enumerate.
```
