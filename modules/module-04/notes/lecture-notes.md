# Module 04 — Games Change Everything

**Topic Area:** Computer Graphics / Rendering (real Canvas module title:
"Games Change Everything")
**Note:** Backfilled from the completed A04 (raytracing report) and L04
(Visual Timeline of Computer Graphics Rendering Evolution), not written
live during lecture. A05 (ChatGPT) was originally documented here by
mistake — it actually belongs to Module 05 and has been moved there.

---

## Key Concepts

- **Raytracing works in reverse of real light.** Simulating every photon
  from a light source is computationally impossible, so raytracers shoot
  rays outward from the camera through each pixel and calculate what that
  pixel should show based on what the ray hits — far more efficient, still
  physically accurate.
- **Recursive ray tracing (Whitted, 1980)** let rays bounce off reflective
  surfaces and refract through transparent materials — the breakthrough
  that turned flat approximations into physically grounded light
  simulation, producing the first photorealistic CG images.
- **Rasterization vs. raytracing is a speed/accuracy tradeoff**, not just an
  old-vs-new story: rasterization (Quake, 1996) used pre-baked lighting
  approximations for real-time speed; raytracing eliminates those
  approximations at much higher computational cost. AI-accelerated
  upscaling (DLSS) is what finally made full ray/path tracing viable in
  real time (Cyberpunk 2077's Overdrive Mode).
- **CUDA (2006) is the hinge point between graphics and AI.** GPU
  general-purpose computing was originally a rendering accelerator, but
  it's the same parallel compute substrate deep learning depends on — one
  hardware shift enabled two different revolutions.
- **Generative AI is a supplement to research, not a replacement for it**
  (per L04's own reflective analysis): AI-generated images are
  aesthetically plausible but not technically accurate, carry anachronism
  risk when depicting historical periods, and are entirely dependent on
  prompt quality — which itself requires the prior subject knowledge the
  tool is supposedly providing.

## Rendering History Timeline (from L04, as a tree)

```
Computer Graphics Rendering Evolution
|
├── 1960s — Ray casting (Arthur Appel, IBM)
|   └── One ray per pixel from camera; determines visibility only
|
├── 1980 — Recursive ray tracing (Turner Whitted)
|   └── Rays bounce/refract → first photorealistic reflections & shadows
|
├── 1989 — Pixar RenderMan
|   └── Procedural shading; offline production rendering becomes the
|       film-industry standard
|
├── 1996 — Quake / real-time rasterization
|   └── 3D rendering moves from workstations to home computers; GPU
|       becomes the driving force of rendering advancement
|
├── 2001 — Programmable shaders (DirectX 8)
|   └── Per-pixel lighting and bump mapping become customizable, not fixed
|
├── 2006 — NVIDIA CUDA
|   └── GPU general-purpose computing; accelerates both rendering AND
|       deep learning on the same hardware
|
├── 2018 — NVIDIA RTX / DirectX Raytracing
|   └── Real-time ray tracing arrives on consumer hardware
|
└── 2020+ — AI-accelerated rendering (DLSS, path tracing)
    └── Neural upscaling makes full path tracing playable in real time
```

## Vocabulary

| Term | Definition |
|---|---|
| Raytracing | Simulates light by tracing rays in reverse (camera → scene) to determine color/illumination per pixel |
| Rasterization | Older, faster rendering method using pre-baked lighting approximations instead of simulated light |
| Path tracing | The most accurate form of light simulation; combined with AI upscaling (DLSS) to run in real time |
| DLSS | Deep Learning Super Sampling — a neural network trained on high-res frames, used to upscale lower-res rendered output in real time |
| CUDA | NVIDIA's platform enabling general-purpose computing on the GPU — the shared hardware foundation of both modern rendering and deep learning |

## Real-World Applications

- Film/VFX production rendering (Pixar RenderMan, Weta Digital) — quality
  over speed, hours per frame acceptable.
- Real-time gaming (Cyberpunk 2077, Minecraft RTX) — speed constraints
  force the DLSS/AI-upscaling tradeoff.
- Architectural visualization (V-Ray, Unreal Lumen) — photorealistic
  walkthroughs of buildings that don't exist yet.
- Synthetic training-data generation for computer vision AI — raytraced
  scenes producing labeled images that would be expensive to capture for
  real.

## Questions I Still Have

- Given DLSS already uses a neural network to make raytracing viable in
  real time, how much longer before "rendering" and "generative AI" stop
  being treated as separate pipelines entirely?

## Connection to Clay Climate AI / My Work

The rasterization-vs-raytracing tradeoff (fast approximation vs. slow
ground truth) is the same tension I navigate in the Hermes pipeline: a
lightweight rule-based pass handles routine report generation fast, while
anything ambiguous gets routed to a slower, more accurate LLM pass — cheap
approximation where it's safe, expensive accuracy where it matters.
