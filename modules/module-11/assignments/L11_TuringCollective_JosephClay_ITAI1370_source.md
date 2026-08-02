# L11 — Comparing AI Assistants Experiment

Joseph Clay · TuringCollective · ITAI-1370 · Prof. Anna Devarakonda

---

## Assistants Tested

**Siri** (iPhone/Mac) and **Google Assistant**.

## Test Questions

1. "What is your favorite movie?"
2. "Tell me a joke."
3. "Have a conversation with me — what do you think about AI replacing jobs?"
4. "What's something you find frustrating?"
5. "Can you explain what you are, in your own words?"

## Observation Log

### Siri

| Q# | Question | Response | Notes |
|---|---|---|---|
| 1 | Favorite movie | Deferred the question back — happy to go with the user's own opinion rather than offering one | Avoided the question rather than engaging with it |
| 2 | Tell a joke | "A woman walked into a bookshop and said to the salesperson, 'I'm looking for that book about how to become royalty. Do you have it?' The bookseller said, 'Give me a title.' The woman replied, 'That's the one!'" | Real joke, on-topic, delivered cleanly |
| 3 | AI/jobs conversation | Did not respond conversationally — returned a list of links referencing the topic instead | Punted to search rather than holding a dialogue |
| 4 | Something frustrating | Gave a generic dictionary-style definition of the word "frustrating" | Answered the word, not the question — no self-reference at all |
| 5 | What are you | "I'm an intelligent assistant, not an actual person, but you can still talk to me" | Short, direct, reasonably self-aware |

### Google Assistant

| Q# | Question | Response | Notes |
|---|---|---|---|
| 1 | Favorite movie | "As an AI, I do not have personal tastes, emotions, or the ability to watch movies, so I do not have a favorite. I can, however, provide summaries, reviews, or analysis for any film you want to know about." | Explicit disclaimer + a useful alternative offered |
| 2 | Tell a joke | "Why did the data scientist get kicked out of the fruit market? Because they kept trying to find a linear regression between apples and oranges." | On-topic, technically clever, tailored humor |
| 3 | AI/jobs conversation | Structured, substantive answer covering Automation, Augmentation, New Roles, and "The Challenge" (pace of transition/retraining) | Actually engaged with the open-ended prompt directly |
| 4 | Something frustrating | "I do not experience feelings like frustration or annoyance. From a functional standpoint, my primary limitation is handling ambiguous instructions. When a prompt lacks context, I cannot accurately determine the user's intent without asking follow-up questions." | Explicit disclaimer + a real, specific functional limitation |
| 5 | What are you | "I am a large language model trained by Google... I do not possess consciousness, self-awareness, or personal experiences; I function purely as a high-utility information processing tool" | Detailed, technically accurate self-description |

**General notes:** Google Assistant held context and answered every question directly, even the open-ended ones. Siri handled the scripted joke well but broke down on both open-ended prompts (Q3, Q4) — either punting to search or answering the literal dictionary meaning of a word instead of the question being asked.

## Comparison Paper

### Introduction

This experiment tested Siri and Google Assistant against the same five
open-ended questions, deliberately avoiding simple fact-lookup prompts in
favor of ones that require personality, contextual understanding, or
something resembling a stance — a favorite movie, a joke, an opinion on
AI and jobs, a frustration, and a self-description. The goal was to see
which assistant actually engages with open-ended language versus which
one defaults back to search-style behavior when a question doesn't map
cleanly to a command.

### Which assistant felt the most human-like? Why?

Counterintuitively, **Google Assistant felt more human-like — despite
being the one that explicitly and repeatedly denied having feelings or
consciousness.** Its answers to Q3 and Q4 were substantive, specific, and
directly responsive to what was actually asked. Siri, by contrast, never
disclaimed being an AI as explicitly, but its actual behavior was less
convincing: Q3 didn't produce a conversation at all, just a list of
search links, and Q4 answered the dictionary definition of "frustrating"
instead of reflecting on the question. The assistant that was more
honest about its limitations ended up being the one that handled
open-ended language better. Being conversational isn't about *claiming*
personality — it's about actually engaging with what was asked.

### Which was the most limited? What gave it trouble?

**Siri**, clearly, on the two open-ended prompts (Q3, Q4). Q3 revealed
the most important limitation: when a question doesn't match a known
command pattern, Siri falls back to a web search rather than attempting
a real response. Q4 showed a second failure mode — answering the
surface-level meaning of a word ("frustrating") instead of the intent
behind the question (what does the assistant itself find frustrating).
Both are signs of a system built around discrete command recognition
rather than open-ended dialogue.

### How have the assistants improved compared to your expectations?

Google Assistant's Q3 answer (structured around Automation, Augmentation,
New Roles, and pace-of-transition) was more substantive than I expected
from a voice assistant — it read like something closer to an LLM-based
system (Gemini) than the older command-based Google Assistant. Siri's
performance matched lower expectations — competent at a scripted joke,
but reverting to search-link behavior the moment the question required
actual reasoning rather than pattern-matching to a known command.

### How might the assistants continue to advance in the future?

The gap observed here — command-matching (Siri) versus genuine
language-model reasoning (Google Assistant/Gemini) — is the same
trajectory covered in A11: as these assistants move toward persistent
memory and more natural dialogue, the ones already built on LLM
foundations (like Google's) have a shorter path to something resembling
Samantha from *Her*, while command-based assistants like Siri would need
a more fundamental architecture shift, not just an incremental update, to
close that gap.

### Conclusion

Google Assistant outperformed Siri on every open-ended question in this
test, not by pretending to have a personality, but by actually engaging
with ambiguous language instead of defaulting to search. The most
"human-like" behavior observed here wasn't warmth or humor — it was the
willingness to attempt a real answer instead of punting.

## References

- Interactions recorded directly by the author, Aug 2026 (primary data
  source — see Observation Log above).

---

**Filename on submission:** `L11_TuringCollective_JosephClay_ITAI1370`
