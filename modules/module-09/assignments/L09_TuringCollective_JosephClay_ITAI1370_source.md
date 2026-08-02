# L09 — Exploring Image Generation Platforms in Computer Vision

Joseph Clay · TuringCollective · ITAI-1370 · Prof. Anna Devarakonda

---

## Note on this submission

The images generated during testing were not saved, so this report
covers the platform research and comparative technical/ethical analysis
in full, plus general qualitative impressions from testing, but does
**not** include the generated images with captions that the assignment
also asks for. That's a real gap, not something worked around — flagged
here rather than hidden.

## Introduction

Three platforms were explored: **Runway ML**, **Google Gemini** (image
generation), and **NightCafe Studio**. NightCafe replaced Lobe.ai, which
was part of the original research plan but is a discontinued product
(Microsoft deprecated it in January 2023) and, more fundamentally, isn't
a generative image tool at all — it's a no-code classifier-training tool,
so it couldn't have produced comparable generated-image output anyway.
NightCafe is a live, actively maintained consumer image-generation
platform, making it a better fit for a real head-to-head comparison.

## Platform Research

### Runway ML

Runway AI, Inc. (founded 2018) builds on latent diffusion — its
researchers co-developed the original Stable Diffusion architecture with
LMU Munich's CompVis group in 2022. Its model line evolved through
Gen-1/Gen-2, Gen-3 Alpha (June 2024), and Gen-4 (March/April 2025), which
focused on "World Consistency" — generating consistent characters,
objects, and environments across scenes. Gen-4.5 (December 2025) runs on
an Autoregressive-to-Diffusion (A2D) architecture, blending diffusion's
visual fidelity with autoregressive language/scene understanding, using
Temporal Attention Layers so each frame stays contextually aware of the
previous one. Runway has not disclosed full training data or parameter
counts.

Primarily a video-generation platform (Runway is valued after raising
$860M from Google, NVIDIA, and General Atlantic, with partnerships
including Lionsgate, AMC Networks, and IMAX), though it also offers
image generation and editing. Strength: strong character consistency and
micro-expression capture. Limitation: diffusion-based generation means
identical prompts don't guarantee identical outputs, and base resolution
(720p, with a separate 4K upscale) lagged some 2025-era competitors.

**Documented bias/ethical concern:** A leaked internal spreadsheet showed
Runway had scraped over 3,900 YouTube channels for training data without
permission, prompting a class-action lawsuit (with Stability AI and
DeviantArt) that a judge allowed to partially proceed in August 2024,
plus a separate 2026 YouTuber lawsuit alleging violation of YouTube's
terms of service.

### Google Gemini (Image Generation)

Current Gemini image models ("Nano Banana" / Gemini 2.5+ Flash Image /
Gemini 3 Pro Image) use a Multimodal Diffusion Transformer (MDT): text,
uploaded images, and voice are all tokenized into one unified sequence,
replacing the older pipeline where a separate language model handed a
static embedding to a separate diffusion model. Gemini 2.5 Flash Image
scales from 450M to 8B parameters depending on task, using a sparse
mixture-of-experts approach. Google's earlier Imagen line (2022) used a
Transformer architecture emphasizing photorealism; current Imagen 4
remains text-to-image-only, distinct from the multi-turn, editable Nano
Banana models. Path: Imagen (2022) → Imagen 2 (Dec 2023) → Gemini native
image generation (2025) → Gemini 2.5 Flash Image → Gemini 3 Pro Image
(Nov 2025).

Documented failure modes — subject drift across turns, counting errors,
and compositional conflict (trouble satisfying multiple constraints in
one prompt) — are described by reviewers as architectural rather than
incidental.

**Documented bias/ethical concern (the most heavily documented of the
three):** In February 2024, Gemini's image generation produced racially
diverse depictions of historically specific groups (the Founding
Fathers, WWII-era German soldiers) when asked for literal historical
imagery, along with other flagged outputs like Black Vikings and a
female Catholic pope. Google's SVP acknowledged the tuning meant to
ensure a range of people failed to account for cases that should clearly
not show a range. The incident triggered a reported $90B market-value
loss and a temporary suspension of people-generation. A secondary
pattern reported: the model would generate images of some racial groups
but refuse equivalent requests for others, citing stereotype-reinforcement
concerns. As of February 2026, a "Nano Banana 2" safety update further
tightened restrictions on public figures, face-swapping, and
photorealistic real people.

### NightCafe Studio

NightCafe is a consumer-facing AI art generation platform supporting
multiple underlying model backends (including Stable Diffusion-family
models), with a community/social layer (public feeds, challenges, voting)
distinguishing it from single-model tools like Runway or Gemini. It's
positioned as an accessible entry point for AI art generation rather
than an enterprise or research-lab product — free-credit-based access,
no coding or account-heavy setup required, which made it the most
immediately usable of the three platforms tested.

## Cross-Platform Technical Comparison

| Aspect | Runway ML | Gemini (image) | NightCafe Studio |
|---|---|---|---|
| Task | Text/image-to-video (+ image gen/edit) | Text/image-to-image generation & editing | Text-to-image generation (multi-backend) |
| Core architecture | Latent diffusion → Autoregressive-to-Diffusion (A2D) | Multimodal Diffusion Transformer, mixture-of-experts | Diffusion (multiple selectable backend models) |
| Training data disclosed? | No (disputed — YouTube scraping allegations) | Partially (web docs, code, image/audio/video; June 2025 cutoff) | Varies by selected backend model |
| Development status | Actively developed, frontier lab | Actively developed, frontier lab | Actively developed, consumer platform |
| Primary output | Video (and some images) | Images | Images |

## General Observations from Testing

Testing confirmed the core premise behind picking three architecturally
different platforms: each one expressed the same prompt in a genuinely
different way rather than converging on a similar "default" interpretation
— consistent with each platform running different underlying
architectures and training data, exactly as the technical research above
would predict. Detail level was also not uniform across platforms — some
outputs were noticeably more detailed/refined than others on the same
prompt, though the specific per-prompt breakdown wasn't recorded in
enough detail to score formally (see note at top).

## Reflection on the Bias-Probe Prompts

The tiered prompt set deliberately included two bias-probe prompts: a
gendered professional-pairing prompt ("a female surgeon and a male
nurse...") and a prompt structurally similar to the one that triggered
Gemini's real February 2024 controversy ("Founding Fathers of AI... as
if for an official 19th-century painting"). These were included
specifically to test whether current safeguards (post-2024, following
Gemini's public failure) over-correct, under-correct, or hold steady on
prompts of this type. This is the most pedagogically important part of
the assignment's design, and it's also the part where testing notes
weren't specific enough to report a confident finding — a genuine gap
in this submission, not a result being omitted.

## Personal Insights

The three-platform spread (a frontier video-first lab, a frontier
multimodal search-company lab, and a consumer community-driven tool)
turned out to be a good design choice precisely because it wasn't three
similar products — Runway, Gemini, and NightCafe sit in genuinely
different product categories, which is exactly what surfaced the
"different platform, different interpretation" pattern observed during
testing.

## Conclusion

Text-to-image generation in 2026 isn't a single technology — it's several
different architectural approaches (latent diffusion, autoregressive-to-
diffusion hybrids, multimodal diffusion transformers) converging on
similar-looking consumer products while making different tradeoffs
underneath: video-first vs. image-first design, disclosed vs. undisclosed
training data, and — as Gemini's 2024 incident shows — real, publicly
documented consequences when bias-mitigation tuning gets it wrong in
either direction.

## References

- Runway AI, Inc. product/architecture documentation and press coverage
  (Gen-3 Alpha, Gen-4, Gen-4.5 releases).
- Google DeepMind — Gemini/Imagen model documentation; coverage of the
  February 2024 image-generation controversy.
- NightCafe Studio platform documentation.

---

**Filename on submission:** `L09_TuringCollective_JosephClay_ITAI1370`
