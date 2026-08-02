# Mini CDR — Module 04: Games Change Everything

Module 04 covers two Canvas items: A04 (What is Raytracing?) and L04
(Explore Generative AI for Visualizing Rendering History). A05 was
previously (incorrectly) documented here — it's been moved to Module 05,
where it actually belongs on Canvas.

## A04 — What is Raytracing?

```
Mini CDR — A04: What is Raytracing?
|
├── Problem / Prompt
|   └── Explain raytracing (definition, how it differs from
|       rasterization), survey where it's used across industries, and
|       give concrete real-world examples.
|
├── Approach
|   └── Structured around the reverse-of-real-light explanation first
|       (why raytracing shoots rays from the camera, not the light
|       source), then built out from definition → industries → named
|       examples (Cyberpunk 2077, Minecraft RTX, Pixar RenderMan) so each
|       claim had a concrete anchor.
|
├── What worked
|   └── Leading with the rasterization-vs-raytracing contrast made the
|       "why does this cost so much more" question answer itself before
|       it needed to be asked.
|
├── What didn't / had to change
|   └── n/a — straightforward research report, no real revision needed.
|
├── What I'd do differently next time
|   └── Include a synthetic-training-data angle earlier — it only shows
|       up briefly under "Scientific and AI Simulation" but it's the most
|       directly AI-relevant application in the whole report.
|
└── Key concept takeaway
    └── Raytracing's cost isn't a flaw to be optimized away — it's the
        direct tradeoff for eliminating lighting approximations. AI
        upscaling (DLSS) is what's currently shrinking that cost, not
        raytracing itself getting cheaper.
```

## L04 — Explore Generative AI for Visualizing Rendering History

```
Mini CDR — L04: Explore Generative AI for Visualizing Rendering History
|
├── Problem / Prompt
|   └── Build a visual timeline of 8 major milestones in computer
|       graphics rendering history, using generative AI (DALL-E) to
|       produce a representative image for each milestone, then
|       critically reflect on AI as a historical-visualization tool.
|
├── Approach
|   └── Picked 8 milestones spanning 1960s ray casting through 2020+
|       AI-accelerated path tracing, wrote a period-specific, technically
|       grounded prompt for each (not generic "1960s computer" prompts),
|       and deployed the result as a live interactive site rather than a
|       static deck: https://cg-timeline-evolution.netlify.app/
|
├── What worked
|   ├── Writing technically specific prompts (e.g. naming ray-surface
|   |   intersection, RT cores, DLSS explicitly) instead of vague
|   |   aesthetic prompts — this is what separated "looks like the era"
|   |   from "actually represents the technology."
|   └── Pairing every image with real historical sourcing (Appel 1968,
|       Whitted 1980) so the AI visual was illustration, not the
|       historical claim itself.
|
├── What didn't / had to change
|   └── n/a — no correction needed, but the reflective-analysis section
|       required real self-critique (technical accuracy, anachronism
|       risk, prompt dependency) rather than just praising the tool.
|
├── What I'd do differently next time
|   └── Generate multiple candidate images per milestone and document
|       *why* one was chosen over the others — right now only the final
|       selected image and prompt are shown, not the selection process.
|
└── Key concept takeaway
    └── Generative AI is a supplement to research, not a replacement for
        it — prompt quality is entirely bottlenecked by the prompter's
        existing subject knowledge, which undercuts the idea of AI image
        generation as an independent educational resource.
```
