# Module 08 — Deep Learning: Big Data and Architectures

**Topic Area:** Generative Adversarial Networks
**Note:** Backfilled from the completed A08 (Fact or Fiction: story-based
GAN exploration) and L08 (companion presentation deck), not written live
during lecture.

---

## Key Concepts

- **The Generator/Discriminator adversarial loop, embodied.** A08's
  activity structure directly mirrors GAN training: team members write
  stories (Generator phase — produce something meant to pass as real)
  and then classify each other's stories as fact/fiction/mixed
  (Discriminator phase — judge authenticity), with a reveal-and-reflect
  step standing in for the gradient signal that flows back to update the
  Generator.
- **Believability is a learned distribution, not a property of drama.**
  The most convincing story (Story A) wasn't the most dramatic one — it
  was the most statistically plausible, full of small, specific,
  low-stakes details (a named school, a precise percentage, an ordinary
  emotional arc) that are hard to fabricate without lived experience.
- **Mixed content is the hardest to classify.** Story C (real GAN facts —
  Goodfellow's actual Montreal-bar origin story — blended with invented
  specifics like a fabricated MNIST accuracy figure) caused the most
  evaluator disagreement. Credibility anchoring: once a reader accepts
  early true claims, later fabricated ones inherit that trust.
- **Adversarial pressure improves both sides.** Knowing evaluators would
  scrutinize every detail pushed story authors toward more precise,
  consistent narratives — the same dynamic that drives a GAN's Generator
  toward increasingly realistic output as its Discriminator improves.

## The GAN Framework, mapped onto the activity (as a tree)

```
Fact or Fiction Activity ←→ GAN Training
|
├── Story Author ←→ Generator
|   ├── Crafts narratives from imagination + knowledge
|   ├── No direct access to evaluator's internal reasoning
|   └── Learns what "reads as true" from experience, same as a Generator
|       learns a training distribution
|
├── Story Evaluator ←→ Discriminator
|   ├── Assigns a verdict (fact/fiction/mixed) from feature extraction:
|   |   detail density, emotional tone, internal consistency, domain
|   |   plausibility
|   └── Best evaluators noticed inconsistent specificity (a suspiciously
|       exact number), not surface-level engaging prose
|
└── Reveal & Reflection ←→ Backprop / Loss Signal
    ├── "That accuracy figure seemed too specific" → precise error signal
    └── Nash equilibrium analog: the point where evaluators are
        genuinely uncertain which story is real
```

## Vocabulary

| Term | Definition |
|---|---|
| GAN (Generative Adversarial Network) | Two competing networks — a Generator producing synthetic data, a Discriminator judging real vs. fake — trained jointly (Goodfellow et al., 2014) |
| Mode collapse | A real GAN failure mode where the Generator finds a narrow slice of output space that exploits the Discriminator's blind spot, and stops producing diverse output |
| Credibility anchoring | Embedding real, verifiable facts early in a false narrative so later fabrications inherit the reader's trust |
| Nash equilibrium (GAN context) | The training endpoint where the Generator's output is indistinguishable from real data and the Discriminator can do no better than chance |

## Real-World Applications

- Deepfakes and synthetic media specifically exploit the "mixed content is
  hardest to detect" finding — blending authentic and invented features
  to evade detection (Karras et al., 2019).
- Data augmentation, style transfer, and drug discovery all rely on the
  same Generator/Discriminator training loop explored here narratively.

## Questions I Still Have

- The activity's evaluators improved at spotting suspiciously precise
  details (Story C's 94.7% figure) — is that the human equivalent of
  what a real Discriminator network actually learns to detect, or is
  human pattern-recognition finding a completely different signal than
  a trained model would?

## Connection to Clay Climate AI / My Work

The credibility-anchoring finding (real facts early, fabrication later,
trust transfers) is directly relevant to reviewing AI-generated content
in the Hermes pipeline — a generated report that opens with accurate,
verifiable details is exactly the kind of output that needs the most
scrutiny on its later claims, not the least.
