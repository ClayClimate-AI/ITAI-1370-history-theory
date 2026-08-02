# Reflection — Module 03: Games, Prelude to A.I.

## L03 — Scratch Paddle Game

**What challenged me this module:**
Debugging without a text stack trace. The score-reset bug (a competing
loop zeroing the score on every increment) had to be tracked down by
reasoning through which sprites were triggering which scripts when — no
line numbers, no error message, just visual blocks and behavior.

**What clicked that didn't before:**
Giving every sprite its own independent `when 🚩 clicked` trigger is what
actually solved the simultaneous-start problem — I didn't need one master
controller sequencing the sprites, I needed each one to react to the same
event independently. Event-driven design over sequential control.

**How I'd explain this concept to someone who knows nothing about AI:**
Three separate pieces (the ball, the paddle, the red line) all needed to
start at the same moment when the flag was clicked, and the ball and the
red line both needed to affect a shared score without stepping on each
other. That's the same class of problem as two people editing the same
spreadsheet cell at once — whoever writes last wins, which is usually not
what you want.

**One thing I want to go deeper on:**
How Scratch's execution model actually schedules multiple `when 🚩 clicked`
scripts under the hood — is it true parallelism, or fast interleaving that
just looks simultaneous?

**How this connects to the broader AI landscape:**
This is a small, visible version of the same coordination problem behind
multi-agent systems: multiple independent actors reacting to a shared
trigger, potentially touching the same state. Scratch just makes the bug
easy to see instead of buried in a stack trace.

## InClass Assignment — AI-Based Stock News Sentiment Tracker

**What challenged me this module:**
Building a sentiment classifier that's actually explainable instead of a
black box — every score needed to be traceable back to specific keywords
and modifiers, not just "the model said so."

**What clicked that didn't before:**
Negation handling is where naive keyword scoring breaks first. "Not
profitable" contains a positive word (profitable) that a dumb keyword
counter would score as good news — the negation-detection layer exists
specifically to catch that.

**How I'd explain this concept to someone who knows nothing about AI:**
The tracker reads news headlines about five stocks and scores them from
-100 (very bad) to +100 (very good) — not by understanding the news the
way a person would, but by matching weighted keywords and checking whether
they're negated. It's a simpler, more explainable stand-in for what an LLM
sentiment classifier does under the hood.

**One thing I want to go deeper on:**
How much accuracy is actually lost going from weighted-keyword scoring to
a real trained sentiment model — is the explainability tradeoff worth it
outside a classroom demo?

**How this connects to the broader AI landscape:**
This is a hand-built, auditable version of something usually done by an
opaque model — a useful contrast to everything else in this course that
leans on "trust the LLM's output."

## A03 (AlphaStar) + Puzzle 03 (Monty Hall)

**What challenged me this module:**
Holding two opposite lessons in the same module: AlphaStar is genuinely
superhuman at StarCraft II, and it's also fundamentally narrow. It's easy to
default to one framing ("AI is unstoppable" or "AI is overhyped") — the
actual answer is both are true depending on what you're asking it to do.

**What clicked that didn't before:**
The Monty Hall reveal isn't random information — it's deliberate, and that's
exactly why it changes the math. Monty always avoids the car and always
avoids your door. Once I saw the reveal as an action with rules rather than
a coin flip, switching stopped being counterintuitive and started being
obvious.

**How I'd explain this concept to someone who knows nothing about AI:**
AlphaStar can beat any human at one specific video game and can't tie its
shoes. It's not that it's "not smart enough" — it's that it was never built
to be smart about anything except that one game. Intelligence in a narrow
box is still a box.

**One thing I want to go deeper on:**
How researchers are actually trying to solve lifetime adaptation — is it a
training-data problem, an architecture problem, or something more
fundamental about how these models learn.

**How this connects to the broader AI landscape:**
Both artifacts point at the same idea from different angles: a system that
performs perfectly inside a fixed, well-defined environment (a game board, a
probability puzzle) can still fail badly the moment the environment gets
open-ended or the rules aren't fully known in advance. That's the gap
between narrow and general intelligence, and it's the gap every "is this AI
actually reasoning" debate ends up circling back to.
