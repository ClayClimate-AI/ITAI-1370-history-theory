# Reflection — Module 10: NLP – Basics

## A10 — Manual NLP Pipeline

**What challenged me this module:**
Stemming by hand was the hardest part to do honestly — it's tempting to
"fix" an ugly non-word fragment like "viabil" or "decis" into something
that looks more correct, but that would misrepresent what a real
rule-based stemmer actually produces. Leaving the imperfect fragments in
was the right call, and reflecting on why they happen was more valuable
than a cleaner-looking but dishonest result.

**What clicked that didn't before:**
Stop word removal cutting the corpus from 98 to 61 tokens made the
"structural filler vs. topical content" distinction concrete instead of
abstract. Over a third of ordinary English text is words like "the" and
"of" — necessary for grammar, carrying almost nothing about what the text
is actually about.

**How I'd explain this concept to someone who knows nothing about AI:**
Before a computer can do anything useful with text, it has to turn words
into numbers — that's the whole point of every step in this pipeline.
Cleaning and splitting the text into words is step one; stripping out
filler words and normalizing the rest gets you down to what actually
matters; and the final vector is just a list of counts a machine can
finally do math with.

**One thing I want to go deeper on:**
How real-world stemmers/lemmatizers handle exceptions at scale — my
22-word stop list and manual suffix rules worked for one paragraph, but
a production pipeline needs those rules to generalize across millions of
documents without someone hand-checking every fragment.

**How this connects to the broader AI landscape:**
Every LLM I've used all semester (ChatGPT in A05, Claude building this
repo) has some version of this pipeline running invisibly underneath —
tokenization especially, since that's literally how models like GPT
process input. Doing it by hand on 98 words made visible what normally
happens silently on billions.

## Lab 10 — IBM Watson Chatbot (Lendyr Demo)

**What challenged me this module:**
Separating "this platform is technically impressive" from "this platform
was actually pleasant to use" — Watson Assistant's enterprise tooling
(integrations catalog, voice/phone deployment) is genuinely capable, but
that capability came with real setup overhead that made the hands-on
experience feel bulky and static compared to consumer assistants.

**What clicked that didn't before:**
The gap between a scripted path and an unscripted one is where Watson
Assistant's design shows its real limits — "Modify in progress
application" hit a dead end (agent offline, file a ticket) not because
the platform is unintelligent, but because nobody had built that path.
It's a chatbot construction kit, not a chatbot — the intelligence is
entirely in what the business chose to build.

**How I'd explain this concept to someone who knows nothing about AI:**
Most consumer chatbots (Siri, ChatGPT) can respond to almost anything you
throw at them, imperfectly. Watson Assistant is the opposite: it responds
very well to the exact paths a business built for it, and falls apart
completely the moment you step outside them.

**One thing I want to go deeper on:**
Whether Watson Assistant's Search feature (shown in IBM's own tutorial,
connecting the assistant to an external knowledge base) would have
actually caught the "Modify in progress application" request if it had
been configured — or if that specific request genuinely had no good
automated answer regardless of setup.

**How this connects to the broader AI landscape:**
This is the enterprise mirror of L11's finding: Google Assistant handled
open-ended questions better than Siri by actually engaging instead of
falling back to search links. Watson Assistant's dead end here is the
same failure mode at enterprise scale — a system that's excellent within
its built scope and has nothing beyond it.
