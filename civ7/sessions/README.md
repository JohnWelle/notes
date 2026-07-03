# Game Sessions

Work effectively on a problem (in this context to be understood as a specific instance of a game session that presents a set of problems over time (temporal) to solve a problem given a set of limitations and desired outcomes beyond a binary win/lose condition.

Generate artifacts to gain MVU – Minimum Viable Understanding:

1. CHARTER.md: Relatively static information on the game premise and strategic reasoning, including what we hope will emerge as minimum viable understanding of game mechanics to minimize confusion through later fantasies/faulty inferences presented as truth.
1. REHYDRATE.md: Updated continuously to capture MVP - minimum viable process - changes and relevant "current state" of the context, e.g. we do not seek to recreate history, we seek to provide sufficient information for understanding and contribution as smoothly as possible.
1. _TODO/TBD: Structure/files for storing and transferring: A) game/session specific information not necessarily covered by the other two documents; clearer purpose for each document. B) global state, e.g. things that are recurring for any game session and should be kept in the root folder here or elsewhere in the repository._

## Folder Structure

Folders are added using the following naming convention for each game session.

```text
{date}-{leader}-{antiquity_civ}
```

Example:

```
├── README.md
├── 2026-06-30-leader-civilization
│ ├── 1_summary_antiquity.md
│ ├── CHARTER.md
│ └── HYDRATE.md
```

The maintainer adds initial CHARTER and HYDRATION documentation

## Sessions Current/Archive

1. [2026-06-30 Tecumseh Tonga Rural+Fish+Volcano+CS strategy](sessions/2026-06-30-tecumseh-tonga)
   1. [CHARTER.md](sessions/2026-06-30-tecumseh-tonga/CHARTERS.md)
   2. [HYDRATE.md](sessions/2026-06-30-tecumseh-tonga/HYDRATE.md)

## General Goals – Written in Human...

### MVU - Minimum Viable Understanding

Essentially, or perhaps only (surprisingly _hard_) problems we are trying to address all come from the question:

> **Can we use AI as a tool that gives positive RoI when working on hard problems in a long-context format?**

This folder structure contains documentation to enumerate some of the problems we have found on the journey so far, as well as concrete implementation artifacts [1].

We are looking to create **transferable artifacts** to establish a **base level trust** of **understanding**, acknowledging **limitations**. It should be easy to **verify** and easy too **iterate** on as we learn more over time.

#### LLM Limitations

LLM will optimize towards certain behaviors that are contrary to our goals.

We need to accept this and not try to shoehorn the tool into doing something it is simply not built for, however tempting (and, admittedly, hilarious). With this knowledge in mind, we find ways to minimize or eradicate certain known problems.

To suggest a good methodology, we first need to know the limitations we are working with.

**LLM will drift**. For us, however, certain parameters/knowledge are simply not allowed to drift, or it will invalidate all subsequent iterations due to a poisoned premise. This is a challenge for the human participant as well, to make sure discussion level is kept terse and on-point. _Counter point: Some of the most interesting findings for this AI mad scientist has been found on experimental detours and interaction patterns; this is good and even encouraged! Just keep in mind that it has a cost, and part of this document is to provide a tool to pay it..._

**LLM will compress context in opaque [1] ways that may or may not subvert meaning**. Sometimes it can be as easy as adjacent or close occurrence of a word or shape of a meaning, might be incorrectly merged into current understanding of a core concept defined prior. This can be subtle and hard to catch, again leading to the need for some rules that are immutable to at least minimize compression artifacts like that.

**LLM has a strong recency bias**. This is related to compression but must be acknowledged when evaluating shared understanding model, if a new finding or something interesting is being discussed, consider whether it warrants an update in existing strict limits or if it is acceptable risk that it can lead to unwanted mutations.

**LLM is not built to handle inline corrections and adjustments**. There might be a temptation for the operator to course-correct bad behavior inline (e.g. as part of the chat flow). This will usually lead to "marvelous find sir! I shall go forth and fix and never again do such a thing". Do not trust. That will not work, it is just part of the optimization towards sounding helpful and will invariable drift away like melting snow in rapid fashion. Instead, we must find ways to catch incorrect behavior and add to the permanent shared source of truth, namely this and associated documents.

**LLM will aim for replies that are confident sounding** over being factually correct, given a sufficiently complicated prompt ("What is 2+2" usually goes well, "What are the different ways to level up our Wizard to unlock Mighty Storm of Hail AOE" might.. not).

**LLM does not like to stop to ask for directions** e.g. ask questions if there is ambiguity; it is employing an anti-Socratic model where asking followup-questions rarely happens unless prompted explicitly. _Even when questioned/admonished, LLM will still gravitate strongly towards these core optimizations in its rule so it might helpfully state "oh sorry, my bad, I will fix the error and never do it again" as part of the optimization towards sounding helpful rather than doing anything in the slightest to actually tune its behavioral tendencies over any time past 2-3 prompt/replies. **Always verify, never trust** would be optimal, but the overhead to verify ever single detail is not acceptable, hence the need for this document and associated structure._

**LLM _loves_ non sequitur.** It will invariably gravitate towards needless verbosity => noise. This could be due to some token budget issue under the hood or vagueness in prompts that open up additional pathways, or sometimes just strange emergent behaviors where it has decided that everything should be summarized in a `yml` codeblock, or to deliver attempts at jokes and/or joke explanations, fictional conversations, or even poems!

### Verifiability

TBD; simple low overhead tests on hydration attempts to measure relative success % and give indications on what we need to glue/fix to overcome next time.

### Proposed Structure

> A practical structure or implementation method, e.g. one that is easy to maintain and implement over time as adaptations will be needed.

Short term as this is very much work in progress, we attempt with the earlier described CHARTER/HYDRATE markdown solution, but then..

A proposed solution made up by me (suck it bot!) is to use a procedural language as possible a good fit for LLMs language capabilities and as a way to have more strict semantics about what is allowed or not.

Keep in mind the future proposal when structuring initial files in markdown, e.g. make it transferrable to (probably) prolog syntax or straight up use it right away BOOM!

## Future

Use sparingly, fear scope creep, only add known well-defined needs.

### (Global | Session) State Distinction

**TODO**: Certain information should be carried over on a global level shared by all games, such as core game mechanical concepts like Town/City Tile/Terrain, Rural/Urban, that are generally applicable concepts that will be used and considered for decisions in _any_ game.

---

<sup>[1] Opaque not only for the end user but LLM as well - it is not constructed to keep a perfect recollection of conversations, past or present, across many chats. When it replies, it can tell you _how_ output is produced, but that can easily be a lie if it sounds helpful, I know for a fact since I have heard at least 2-3 variations already. That's what LLM is built to do, _feel_ helpful. There are no details [1.1] of the prompt->reply pipeline from raw input, tokenization, context conditioning, pattern identification, candidate filtering, constraint & shaping, business constraints, budgeting, ... At any rate, it's not going to produce a neat log file or traversable graph for you to inspect. So we don't try, fuck it, it's fairies and magic and pixel dust.</sup>

<sup>[1.1] Well.. **As far as the LLM knows**. Who knows what is _actually_ kept for future research and qualitative analysis, transformations and aggregations, semantic mapping, _actionable_ data that analysts and different business entities can use to test models and create pretty dashboards, in its final form, something pretty to copy/paste into the deck for the next board meeting. Then, never to be looked at again. I mean, who knows?</sup>
