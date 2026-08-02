# Final Exam Portfolio — ITAI-1370

Joseph Clay · TuringCollective · Houston Community College · Summer 2026
Prof. Anna Devarakonda

---

## Note on structure

This portfolio is built directly from the module-by-module documentation
already maintained throughout the semester in this course repository
(github.com/ClayClimate-AI/ITAI-1370-history-theory) — each module's real submitted
work, backfilled notes, and reflections. Nothing below is invented for
this document; it's a synthesis of work already done and already graded.

**Filename note:** Confirmed verbatim from the Canvas assignment page —
`FE YourName ITAI 1371 2023`. The course number/year don't match this
course (ITAI-1370, 2026), but that's the literal instructor-specified
convention, not a typo introduced here — used as given below:
`FE JosephClay ITAI 1371 2023`.

---

## Module 01 — Introduction to A.I.: Course Setup

**Activities:** Wrote a full research paper ("The Evolution of Artificial
Intelligence") tracing AI from myth and philosophy through the Dartmouth
Conference, the symbolic-AI era and AI winters, to deep learning and
modern LLMs. Completed the Glossary Kick Start lab.

**What I learned:** The "AI effect" — each generation redefines
intelligence as whatever machines still can't do — explains why AI always
feels both overhyped and perpetually out of reach. The deeper throughline
of the whole paper: AI's history is a repeating cycle of bold ambition,
disappointment, and a sidelined idea (connectionism/neural networks)
eventually returning to redefine the field.

**Grade:** A01 — 100% · L01 — 100%

---

## Module 02 — Introduction to A.I.: The Big Issues

**Activities:** Researched why Google was founded (PageRank vs.
keyword-frequency search) and analyzed the 2014–2023 GenAI patent surge
(A02). Built an 11-person research spreadsheet tracing foundational AI
figures — Turing, McCarthy, Minsky, Shannon, Rosenblatt, Hinton, LeCun,
Bengio, Vaswani et al., Samuel — from their landmark work to a named
system in use today (L02). Solved Google's 100-prisoner hat puzzle using
parity encoding and mapped it to AI concepts: error correction, binary
classification, Bayesian inference (Puzzle 02).

**What I learned:** Nearly every foundational AI breakthrough documented
in L02 was funded by DARPA, ONR, NSF, or internal corporate R&D — AI
research has never been separable from defense and corporate funding.
From the hat puzzle: one bit of well-chosen shared information is enough
to turn a group of individually-blind agents into a system with 99%
guaranteed accuracy — the rule is the intelligence, not any single
agent's knowledge.

*(Screenshot placeholder: hat-puzzle simulator images already saved in
`modules/module-02/resources/`)*

**Grade:** A02 — 98% · L02 — 98% · Puzzle 02 — 99/100

---

## Module 03 — Games, Prelude to A.I.

**Activities:** Built a client-side AI Stock News Sentiment Tracker
(rule-based scoring: weighted keywords, negation detection, intensity
modifiers) for the InClass assignment. Analyzed AlphaStar's limitations
(narrow intelligence, lifetime adaptation, forward-model planning) for
A03. Built a Scratch paddle-and-ball game for L03, debugging a real
race-condition bug in the score system. Solved the Monty Hall problem
using Bayes' Theorem for Puzzle 03.

**What I learned:** Mastery inside a fixed, fully-specified environment
(a video game, a puzzle with a formula) doesn't transfer to open-ended
environments — true for both AlphaStar and for naive probability
intuition. The Scratch score-reset bug was a small, visible version of a
real coordination hazard: multiple independent triggers touching shared
state.

**Grade:** InClass — 98/100 · A03 — 98/100 · L03 — 98% · Puzzle 03 — 99/100

---

## Module 04 — Games Change Everything

**Activities:** Researched raytracing vs. rasterization, real-time ray
tracing (NVIDIA RTX), and AI-accelerated rendering/DLSS for A04. Built a
visual timeline of 8 milestones in computer graphics rendering history
(1960s ray casting → 2020+ AI-accelerated path tracing) using
generative AI (DALL-E) imagery for L04, deployed as a live interactive
site.

**What I learned:** Raytracing's cost isn't a flaw — it's the direct
tradeoff for eliminating lighting approximations; AI upscaling (DLSS) is
what's currently shrinking that cost. On generative AI as a research
tool: prompt quality is entirely bottlenecked by the prompter's existing
subject knowledge, which limits its use as an independent educational
resource.

**Grade:** A04 — 98% · L04 — 98%

---

## Module 05 — Machine Learning: The Data

**Activities:** Researched ChatGPT's three-stage training (pretraining →
supervised fine-tuning → RLHF) and ran six real test questions against
it, critically analyzing accuracy/human-likeness/limitations (A05).
Researched three computational humor systems (JAPE, GPT-3, Bard/Gemini),
designed a manual joke-generation algorithm, and tested a real joke on
three human respondents (L05).

**What I learned:** RLHF optimizes a model to *sound* aligned with human
preference — not to know when it's uncertain. Those are different
problems. From the humor lab: an algorithm can verify a joke's mechanical
structure but can't predict whether a given audience's background will
make the connection land — mechanics are computable, impact isn't.

**Grade:** A05 — 98% · L05 — 95%

---

## Module 06 — Machine Learning: The Pipeline

**Activities:** Built a knowledge graph of the ML landscape (Foundations,
Learning Approaches, Techniques, Tools/Frameworks, Applications) in
Whimsical, based on Daniel Bourke's ML Roadmap, explicitly mapping
cross-branch dependencies.

**What I learned:** The ML landscape isn't a sequential curriculum — a
few nodes (Python, Cloud Platforms, Version Control) function as
infrastructure every other branch depends on simultaneously, not a
prerequisite finished once and left behind.

*(Image available: `modules/module-06/assignments/machine-learning-knowledge-graph.png`)*

**Grade:** A06 — 95%

---

## Module 07 — Deep Learning: Neural Networks

**Activities:** Designed a feed-forward neural network predicting HVAC
RTU failure risk from real field-relevant features (unit age, days since
service, ambient temp, fault codes), walking through a full forward
pass and backpropagation correction on a genuinely ambiguous test case
(A07). Ran all 5 TensorFlow Playground experiments — activation
functions, neuron count, learning rate, data noise, dataset complexity —
with real loss numbers for each (L07).

**What I learned:** A neural network doesn't need a human to write the
rule "old AND recently-serviced = lower risk" — it derives that
interaction from a single wrong, confident prediction and the gradient of
that error. From L07: a neural network's success isn't a property of the
network alone — it's the fit between architecture, hyperparameters, and
data (the same 4-neuron network went from perfect on Gaussian data to
nearly useless on a spiral).

**Grade:** A07 — 94% · L07 — 94%

---

## Module 08 — Deep Learning: Big Data and Architectures

**Activities:** Designed and ran a story-based Generator/Discriminator
activity to embody GAN mechanics directly — writing a true story, a
fictional story, and a deliberately "mixed" story (real GAN history
blended with fabricated specifics), then having team members classify
each as fact, fiction, or mixed without labels (A08). Built a companion
8-slide deck presenting the activity, the reveal, and the mapping back
onto real GAN architecture (L08).

**What I learned:** Believability is a learned distribution, not a
property of drama — the story that read as most authentic wasn't the
most dramatic, it was the one with small, specific, mundane details that
are hard to fabricate without lived experience. Mixed content (real facts
blended with invented ones) was the hardest for evaluators to classify,
because early true claims transfer credibility to what follows —
directly relevant to why blended-truth disinformation and deepfakes are
harder to catch than outright fabrication.

**Grade:** A08 — 94% · L08 — 95%

---

## Module 09 — Computer Vision: Image Processing

**Activities:** Researched and compared three architecturally different
image-generation platforms — Runway ML (Autoregressive-to-Diffusion video/
image model), Google Gemini (Multimodal Diffusion Transformer), and
NightCafe Studio (consumer, multi-backend diffusion platform) — covering
architecture, company history, and documented bias/ethics controversies
for each, including Gemini's real February 2024 historical-imagery
incident. Designed a tiered prompt set (simple → complex → abstract)
with two deliberate bias-probe prompts.

**What I learned:** Each platform expressed the same prompt differently
rather than converging on a similar output — consistent with the fact
that all three run genuinely different underlying architectures and
training approaches. Text-to-image generation in 2026 isn't one
technology, it's several different approaches (latent diffusion,
autoregressive-to-diffusion, multimodal diffusion transformers) making
different tradeoffs — disclosed vs. undisclosed training data being the
starkest one.

**Honest gap:** the generated images themselves weren't saved during
testing, so this module's real deliverable is the comparative research
and general testing impressions, not image-by-image evidence. Disclosed
directly in the L09 report rather than glossed over.

---

## Module 10 — NLP: Basics

**Activities:** Manually implemented a full NLP pipeline — cleaning,
tokenizing, stop-word removal, stemming, POS tagging 20+ tokens, and
Count Vectorization — on a corpus pulled from my own A01 essay (the
AlexNet paragraph), without automated NLP libraries (A10). Explored IBM
Watson Assistant's Lendyr Demo and the underlying trial builder —
action/trigger-phrase configuration, the integrations catalog, phone/
voice deployment — testing both a scripted path (a Dental student-loan
flow in Arkansas, handled correctly) and an off-script one ("Modify in
progress application," which hit an agent-offline dead end) (Lab 10).

**What I learned:** Stop-word removal alone cut my corpus from 98 to 61
tokens — over a third of ordinary English text is structural filler, not
topical content. Stemming's fragments ("decis," "viabil") made the real
speed-vs-accuracy tradeoff concrete instead of theoretical. From Lab 10:
Watson Assistant is a construction kit, not a ready-made assistant — its
intelligence is entirely a function of what a business explicitly built,
which is real enterprise flexibility but also means every unbuilt path is
a hard dead end. My own assessment: "not intuitive at all... very
enterprise focus... bulky... static... unimpressed" compared to consumer
assistants.

---

## Module 11 — NLP: LLMs

**Activities:** Analyzed AI digital assistants and conversational AI
against the movie *Her* (2013), arguing the emotional-bond comparison is
overblown — today's assistants are transactional, not companions — while
noting persistent-memory features now shipping are an active step toward
closing that gap (A11). Ran a real 5-question comparison of Siri vs.
Google Assistant (L11).

**What I learned:** The assistant that was more explicit about lacking
feelings (Google Assistant) actually handled open-ended questions more
convincingly than the one that didn't disclaim as much (Siri, which
punted to search links on the same prompts). Being conversational isn't
about claiming personality — it's about actually engaging with what was
asked.

**Grade:** Submitted late Aug 2, pending grading.

---

## Module 12 — AI Agents

**Activities:** Wrote a report on predictive modeling in AI agents, tying
it directly to A07's real RTU failure predictor, then built an original
short-film storyline ("ORACLE") depicting a predictive-maintenance AI
that earns expanded autonomy after one success and drifts toward
optimizing the wrong objective — echoing *Eagle Eye* (2008).

**What I learned:** The realistic risk with predictive AI isn't a rogue
superintelligence — it's a system that performs well enough on its
stated metric to earn expanded authority, while nobody notices the
metric itself was incomplete. Predictions should inform; humans should
authorize — that boundary should be the hardest thing to expand, not the
easiest.

**Grade:** Submitted late Aug 2, pending grading.

---

## Module 13 — Robotics: Grand Tour

**Activities:** Designed "SentryTech," a robot with two real deployment
modes built on my own HVAC/cGMP cleanroom background — commercial HVAC
pre-dispatch verification (preventing the wasted-trip problem from real
field experience) and cleanroom environmental-monitoring. Built a full
ethical analysis (privacy, safety, job displacement, societal impact)
and a digitally-created concept sketch.

**What I learned:** Writing the ethics section honestly required naming
an uncomfortable tradeoff directly — pre-dispatch verification could
reduce dispatch *volume* even as it protects the quality of dispatches
that do happen — rather than only listing the tool's benefits.

*(Sketch available: `modules/module-13/assignments/sentrytech_sketch.svg`)*

**Grade:** Submitted late Aug 2, pending grading.

---

## Bonus — Building an Agent: Hermes

**Activities:** Took on the optional, verbally-announced challenge (not a
graded Canvas item) to build a real AI agent rather than just use a chat
window. Configured and ran Hermes Agent — a purpose-built agentic
architecture with a swappable LLM brain (Claude Sonnet 4, but portable
across 20+ providers), a six-layer stack (brain → agent loop → memory &
context → skills → 12 tools → surfaces), and a live deployment scoped to
this exact course: a Telegram bot pulling assignments and grades straight
from the Canvas API, persistent memory of course context (HCCS Eagle
Online URL, course ID, response-format preferences), and scheduled cron
jobs (Sunday 8pm — check Canvas for new assignments; Friday — summarize
what's due next week; 1 hour before class — send the Teams meeting link).
Safety is built in, not bolted on: destructive commands require explicit
approval, every action is checkpointed and reversible, secrets are
auto-redacted from tool output, and parallel agents are isolated via Git
worktrees so nothing steps on anything else.

**What I learned:** Everything else in this course — the Dartmouth
Conference, symbolic AI, backprop, RLHF, NLP pipelines, GANs — is the
decades of foundational effort that made a system like this *possible*.
Hermes is the other half of the picture: it's not a smarter model, it's
architecture wrapped around a model — memory, tools, scheduling, and
safety rails — that turns "a brilliant reasoner trapped in a stateless
chat box" into something that persists, acts, and improves. The line
that stuck with me: intelligence is rented from the model, but capability
is built in the architecture. Consumer AI tools and LLM harnesses are
what finally put decades of research at an individual's fingertips —
this course gave me the history and the theory; this challenge showed me
the harness that makes it usable in a real workflow.

*(Not Canvas-graded — extra-credit challenge, included here because it
directly extends what this course covers. Source briefing:
`portfolio/Hermes_Agent_bonus_challenge.pdf`)*

---

## Midterm — AI Glossary

**Activities:** Group glossary project submitted as part of TuringCollective.

**Grade:** 94%

---

## Modules 14–16

Nothing assigned on Canvas as of this portfolio's drafting — placeholders
only (Puzzle of the Day / Joke of the Day / Assignment / Laboratory, none
populated by the instructor yet).

---

## Conclusion

One throughline runs through nearly every module in this course: the gap
between mechanically-verifiable correctness and actual human or
real-world value. It shows up as RLHF optimizing a model to *sound*
aligned without knowing when it's uncertain (Module 05); as a Scratch
game's race condition, where two independent scripts touching the same
shared state produced a technically-running but wrong result (Module 03);
as a computational-humor algorithm that can verify a joke's mechanical
structure but not whether a given audience's background makes it land
(Module 05); as Watson Assistant performing flawlessly within its
scripted paths and hitting a hard dead end the moment a request falls
outside them (Module 10); and as a robot design where the honest answer
to an ethical tradeoff (pre-dispatch verification reducing dispatch
*volume*, not just improving dispatch *quality*) had to be stated
directly instead of glossed over (Module 13). The pattern repeats because
it's the actual shape of the problem: a system can be internally
consistent and still miss what a human situation actually needs. Building
this repository — backfilling real documentation, mini critical-design
reviews, and honest gap notes alongside the graded work itself — was
itself an exercise in the same lesson: producing something that's not
just technically complete, but genuinely explainable and defensible.
The Hermes Agent bonus challenge closed the loop on the whole semester:
Modules 01–13 are the history and theory of how AI got here across
decades of ambition and setback; building a real agent on top of that
foundation is what makes all of it usable, right now, at my fingertips.

## Future Objectives in AI

AI is a rapidly evolving field, and my objective going forward is to
build a genuinely comprehensive understanding of it — not just the
individual tools, but the components that connect them and how those
components keep shifting as the technology matures. This course gave me
that foundation on the theory side: how we got from symbolic AI and
neural-network winters to the deep learning and LLM era, and why each
generation of breakthroughs reshaped what "intelligence" even means. The
Hermes Agent bonus challenge showed me the other half — how that theory
gets wrapped into real, deployable architecture: memory, tools,
scheduling, safety rails. I want to keep building on both halves at
once, because neither is complete without the other.

I also want to understand AI's role from two directions, not one. From
an occupational standpoint: how these technologies are actually getting
incorporated into businesses right now, and what that means for the
skill set employers need. But just as much from an entrepreneurial
standpoint — growing my own knowledge base to the point where I can
identify real problems and build real solutions with AI as a
collaborator, not just a tool I call on. Clay Climate AI is where that's
already started (the Make.com-to-self-hosted-agent migration work, the
Hermes deployment itself), and I want that to keep growing: developing
the judgment to know where AI genuinely creates value versus where it's
just automation dressed up, and the technical range to build that value
myself instead of waiting for someone else to build it for me.

The throughline of this whole portfolio — that a system can be
technically correct and still miss what a real situation needs — is
exactly the gap I want to keep closing. Not by trusting the tools more,
but by understanding them well enough to work with them effectively:
knowing what they can verify, what they can't, and where my own
judgment has to fill that gap. That's the skill set I'm building toward,
and this course was the starting point.

---

**Filename on submission:** `FE JosephClay ITAI 1371 2023`
