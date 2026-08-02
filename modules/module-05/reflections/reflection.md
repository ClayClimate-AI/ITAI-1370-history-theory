# Reflection — Module 05: Machine Learning – The Data

Covers both A05 (ChatGPT) and L05 (Computational Humor).

## A05 — ChatGPT Research & Interaction

**What challenged me this module:**
Evaluating ChatGPT's own answers critically instead of just recording them.
It's easy to ask an AI six questions and transcribe the responses; it's
harder to actually check each one for accuracy, human-likeness, and
limitations the way this assignment required.

**What clicked that didn't before:**
"ChatGPT is a tool, not an oracle" is the whole lesson, but the specific
version that clicked was Q2: the model's own listed limitations (hallucination,
no genuine understanding, bias inheritance) came out in the same confident,
uniform tone as every other answer. Fluent delivery masks real uncertainty —
that's the actual risk, not "the AI gets things wrong sometimes."

**How I'd explain this concept to someone who knows nothing about AI:**
ChatGPT doesn't know what it doesn't know. It writes every answer with the
same confident voice whether it's citing a well-established fact or
guessing. That's why the code it wrote (a working Fibonacci function) still
needed a human to notice it was missing test cases — the model won't flag
its own gaps unless you ask it to.

**One thing I want to go deeper on:**
How reward models are actually built and validated during RLHF — right now
I can describe the pipeline (rank responses → train reward model → optimize
with PPO) but not really explain what makes one reward model better
calibrated than another.

**How this connects to the broader AI landscape:**
The healthcare stat (72% of healthcare orgs now use AI/ML) makes the bias
conversation from earlier modules concrete and urgent — pulse oximetry
inaccuracy for darker skin tones isn't a hypothetical, it's a documented
gap in a system already being deployed at scale. The skill that matters
going forward isn't "can you use AI," it's "can you tell when the confident
answer is wrong."

## L05 — Computational Humor

**What challenged me this module:**
Getting genuinely honest feedback on my own joke instead of feedback people
thought I wanted to hear. Getting three different respondents (a former
bank employee, a day trader, and a third reader who read past the wordplay
into the metaphor itself) was the part that actually made the evaluation
meaningful instead of just a formality.

**What clicked that didn't before:**
A joke isn't one idea — it's two valid interpretations of the same sentence
colliding at the same moment. Once I saw "interest" as legitimately
supporting two readings (financial term / emotional state) rather than a
single pun, building the setup-and-punchline stopped being guesswork and
became closer to a testable structure.

**How I'd explain this concept to someone who knows nothing about AI:**
A computer can check whether a joke's setup is specific enough and whether
a word has two real meanings — that's just pattern-matching. What it can't
check is whether the *person hearing it* has the life experience to make the
connection click. That's why Sarah and Jason (who both know banking) rated
the joke higher than David, who understood it but got pulled into thinking
about the metaphor instead of laughing at it.

**One thing I want to go deeper on:**
How systems like JAPE score candidate puns before selecting one to
output — is there an actual quantitative "funniness" metric, or is it
closer to a filter for "is this grammatically valid wordplay" with humor
quality left entirely unmeasured?

**How this connects to the broader AI landscape:**
This is the clearest example yet in the course of the gap between mechanical
correctness and actual value to a human — the same gap A05 surfaced from a
different angle (RLHF optimizes for *sounding* right, not for calibrated
uncertainty). A system can verify its own internal rules were followed; it
can't verify that the output actually served the person receiving it.
