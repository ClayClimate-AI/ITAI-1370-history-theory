# Mini CDR — Module 08: Fact or Fiction (A08/L08)

```
Mini CDR — A08/L08: Understanding GANs Through Story
|
├── Problem / Prompt
|   └── Use a storytelling activity to experience GAN mechanics firsthand
|       — write stories (Generator role) across fact/fiction/mixed
|       categories, then classify unlabeled stories (Discriminator role),
|       and map the experience back onto real GAN architecture.
|
├── Approach
|   └── Wrote the "mixed" story (Story C) deliberately using a real,
|       verifiable fact (Goodfellow's actual GAN origin story) as an
|       anchor, then embedded fabricated specifics around it — testing
|       the credibility-anchoring technique directly rather than just
|       describing it.
|
├── What worked
|   ├── Grounding Story A (the "fact" story) in small, mundane, specific
|   |   details instead of anything dramatic — that's what made it read
|   |   as authentic, and evaluators who guessed "fiction" cited its
|   |   relatability as the very reason they doubted it.
|   └── The reveal-and-reflection phase mapped cleanly onto backprop's
|       error signal — specific evaluator feedback ("that accuracy
|       figure seemed too precise") is a real, legible analog to a
|       gradient update.
|
├── What didn't / had to change
|   └── n/a — activity-based assignment, no revision needed after the
|       fact.
|
├── What I'd do differently next time
|   └── Track how evaluator accuracy changed across multiple rounds
|       (write → classify → reveal → write again) to see whether the
|       "adversarial pressure improves both sides" claim actually holds
|       up quantitatively, not just narratively.
|
└── Key concept takeaway
    └── Mixed content — real facts blended with fabrication — is harder
        to detect than either pure fact or pure fiction, because early
        true claims transfer credibility to what follows. This is the
        same mechanism that makes GAN-generated deepfakes and synthetic
        disinformation dangerous at scale.
```
