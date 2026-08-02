# AI-Collaboration Engineering Vocabulary

Reference glossary for how AI-assisted work is actually being managed in
this repo — the vocabulary behind the mini-CDR and prompt-history
convention. Written to be interview-ready: each term has a real-scale
definition, not just a textbook one.

---

## 1. Agent Verification Loop

**Definition:** A repeatable cycle where an AI's output is checked against a
stated expectation before being trusted, rather than assumed correct because
it "looks right" or ran without errors.

**Real-world scale it's built for:** Agents with autonomy — the AI is
taking actions (deploying, modifying files, calling APIs) with less human
review per step.

**At my scale:** I *am* running this, informally, every time I click "add
item" and confirm it actually worked before moving on. The formal name for
that habit is the Verification Loop.

**Interview-ready definition:** "A verification loop means the agent states
what should happen, I test it, and we don't move forward until the actual
result matches the expected one."

---

## 2. Prompt Contract

**Definition:** A set of standing constraints that govern *how* an AI must
behave across an entire session or project — not a single instruction, but
rules that persist and apply to every future prompt.

**Real-world scale it's built for:** Teams or agents operating with real
autonomy over time, where "the AI did something I didn't expect" has real
cost — shared codebases, production systems, multiple people relying on
consistent AI behavior.

**At my scale:** The per-commit checklist and Communication Standard I've
already been using are a prompt contract — I just hadn't named it. Any
document that says "always do X, never do Y, for every future interaction
in this project" is a prompt contract by definition, regardless of size.

**Interview-ready definition:** "A prompt contract is a standing set of
rules — like always verifying before committing, never skipping
documentation — that the AI has to follow for every prompt in the project,
not just the one it's currently on."

---

## 3. Reverse Prompting

**Definition:** When the AI asks the human clarifying questions before
acting, instead of the human being the only one who initiates prompts.

**Real-world scale it's built for:** Any project with ambiguity — this
one isn't actually a "big project" technique, it's a good-habit technique
at any size. Its value is inversely related to how well-specified your
request was, not how big the codebase is.

**At my scale:** Fully applicable — "should check-off just toggle a class,
or should it also persist to storage?" is a reverse prompt your checklist
app genuinely benefits from.

**Interview-ready definition:** "Reverse prompting is when I let the AI ask
me questions before building, instead of it guessing at ambiguous
requirements and building the wrong thing."

---

## 4. Context Management

**Definition:** The practice of keeping an AI's working understanding of a
project accurate and current, so it doesn't lose track of earlier
decisions, drift into contradictions, or "forget" as a session goes long.

**Real-world scale it's built for:** Long-running sessions and large
codebases — where context windows fill up and an AI's memory of decisions
made hours/days earlier degrades.

**At my scale:** Still real, just smaller — re-reading my README/prompt-
history.md at the start of a session *is* context management. The technique
doesn't change with scale, only how much effort you put into it.

**Interview-ready definition:** "Context management means making sure the
AI's understanding of the project stays accurate over time — re-grounding
it in prior decisions instead of letting drift creep in as the session gets
longer."

---

## Where this shows up in this repo

- **Mini CDRs** (`assignments/mini-cdr.md`) are the write-up half of the
  Verification Loop — stating what should have worked, what actually did,
  and what I'd change.
- **Prompt history** (`assignments/prompt-history-note.md` for backfilled
  modules, `prompt-history.md` going forward) is the log that makes Context
  Management and Reverse Prompting visible after the fact — proof the
  thinking happened, not just the output.
- **README.md's per-commit workflow** functions as an informal Prompt
  Contract, even before this glossary named it.
