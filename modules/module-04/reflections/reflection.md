# Reflection — Module 04: Games Change Everything

Covers A04 (What is Raytracing?) and L04 (Rendering History Timeline).

## A04 — What is Raytracing?

**What challenged me this module:**
Explaining raytracing precisely without leaning on jargon the reader would
have to already know — the "reverse of real light" framing took a few
drafts to get right.

**What clicked that didn't before:**
Raytracing isn't slow because it's poorly optimized — it's slow because it
refuses to approximate. Rasterization's speed comes directly from the
shortcuts raytracing exists to eliminate. That reframed "why is this
expensive" from a limitation into a design choice.

**How I'd explain this concept to someone who knows nothing about AI:**
Instead of simulating every bit of light in a scene (impossible), the
computer works backwards — it only calculates the light that would actually
reach your eye through each pixel. Minecraft RTX is the clearest proof:
same blocky game, completely different lighting, once raytracing replaced
the old flat approximations.

**One thing I want to go deeper on:**
How DLSS's neural upscaling actually decides which pixels to "fill in" —
right now I understand it conceptually as AI-assisted upscaling, not
mechanically.

**How this connects to the broader AI landscape:**
CUDA (2006) is the quiet hinge in this whole story — a rendering
accelerator that turned out to be the same hardware substrate deep
learning needed. Two revolutions running on one architectural bet.

## L04 — Rendering History Timeline

**What challenged me this module:**
Getting AI-generated images to represent *technical* milestones accurately
rather than just looking period-appropriate. A "1960s mainframe" prompt is
easy; a 1960s mainframe that actually gestures at ray-casting logic took
more specific prompting.

**What clicked that didn't before:**
Generative AI for historical visualization has a real ceiling: prompt
quality depends entirely on the prompter already understanding the subject.
That undercuts the idea of AI as an independent research shortcut — it's
only as good as the knowledge you bring into the prompt.

**How I'd explain this concept to someone who knows nothing about AI:**
For eras where no real photos exist of the actual milestone (nobody
photographed "ray casting" happening in 1968), AI can fill that visual gap
with something plausible. But plausible isn't the same as accurate — the
image looks right without necessarily depicting the real math underneath.

**One thing I want to go deeper on:**
Whether there's a way to validate an AI-generated technical illustration
against the real underlying process (e.g., an actual ray-surface
intersection diagram) rather than relying on visual plausibility alone.

**How this connects to the broader AI landscape:**
This is the same lesson as A05's RLHF discussion from a completely
different domain: fluent, confident output (whether text or image) isn't
the same as verified-accurate output. The tool's confidence and its
correctness are two separate variables.
