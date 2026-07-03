# What Is AI?

Sung in tune with the masterpiece "What Is Love", released by Haddaway somewhere mid-90s. Good times.

Anyway, this is just a fun little experiment where I tried, at first, to write down a few serious thoughts about LLM from recent times experimentation, but..

_then_ I got sidetracked and very invested in writing a somewhat long footnote on the relative value of using LLM as a tool in case of a medical issue over a fortune teller, but...

_then_ I got back on track and almost finished it, but realized that the structure had become completely messed up due to aforementioned footnote [1], so

_then_ I got a brilliant idea! Why not feed my human slop to AI so maybe I can get nicer looking slop at least? So I did:

> Hi Gemini, I just wrote some stuff about you (or someone like you, not mentioning any names) for my own private musing reasons, but the structure has become terribly messy, I got side-tracked somehow Can you help with making it look good and sane, and since you are LLM yourself, maybe you have some corrections if I have hallucinated too much, please reply with markdown file. Thanks!

And here is the result:

---

# Never Trust the Oracle

## Notes on LLMs, confidence, and the beautiful lie of understanding

### 1. Intro

Modern language models are easiest to overestimate when they are doing exactly what they are good at: producing fluent, shaped, contextually appropriate language. The trap is not that they sound intelligent when they are stupid. That is too simple. The trap is that they often sound _approximately intelligent in the same direction as the truth_.

That approximation is useful. It is also dangerous.

A good LLM can summarize, translate, refactor, suggest, classify, brainstorm, explain, and produce a plausible first draft of nearly anything. It can help a software engineer think through a gnarly abstraction leak. It can help a non-programmer understand a bureaucratic document. It can make a bad day slightly less bad by being available, patient, and weirdly competent at tone. These are not small things.

But the central rule still holds:

> Never trust AI. Inspect it.

Or, less dramatically: treat it as a powerful assistant whose output must be checked against the thing you actually care about. In a medical emergency, it may still be better than calling your local Healer and Seer, Maria Katchoskavja, but that is more an indictment of Maria than a blanket endorsement of the machine.[1]

The practical question is not whether AI “understands” in the same way people do. That question is fascinating, but it can also become a swamp. The more immediately useful question is this:

> What kinds of mistakes does this system make precisely because it is so good at seeming coherent?

This essay is a field note from that angle. It is not a grand theory of intelligence. It is a catalogue of quirks, traps, and working heuristics gathered from using these systems enough to notice their recurring failure shapes.

The short version is that LLMs are best understood neither as dumb autocomplete nor as reliable synthetic minds. They occupy the uncomfortable middle: capable enough to be useful, fluent enough to be persuasive, and unreliable enough that trust must be earned at the level of each claim.

### 2. An outside-in model of the machine

From the outside, the interaction feels simple. You write a prompt. The model replies. If the reply is good, it feels as if the model understood the prompt, formed an intention, reasoned through the problem, and then chose words to communicate the result.

That is the human-shaped story.

The machine-shaped story is stranger.

At a high level, the system does not begin with “meaning” in the way a person experiences meaning. Your text is first converted into tokens: pieces of text that may be words, parts of words, punctuation, whitespace patterns, or other units convenient for the model. The model then predicts likely continuations conditioned on the token sequence, the current context, its training, and whatever additional systems are wrapped around it.

This is not the same as saying “it merely predicts the next word.” That phrase is technically suggestive but psychologically misleading. The prediction process can encode patterns of reasoning, style, structure, analogy, domain knowledge, and instruction-following. A system trained to predict language across enough varied examples can learn surprisingly general procedures. It can act as if it is doing many kinds of thinking.

But the distinction still matters.

The model does not necessarily know why it produced a given sentence in the way a person might know why they reached for a cup. When asked to explain its reasoning after the fact, it may produce a plausible reconstruction rather than a faithful trace. Sometimes that reconstruction is useful. Sometimes it is a polished myth about itself.

This is one of the easiest places to get fooled. You see a confident answer, ask where it came from, and receive a confident explanation. The explanation may cite a real pattern, a real source, or a real inference. It may also be a second act of the same performance: language generated to satisfy the shape of “explain yourself.”

That does not make the answer worthless. It means the explanation should be treated as a claim, not an audit log.

#### Tokenization is not interpretation

Tokenization is often tempting as a metaphor for understanding: the system breaks text apart, processes it, and produces something coherent. But tokenization itself is only the entry gate. The interesting behavior happens in the learned transformations over those tokens and in the surrounding product system: context windows, memory summaries, retrieval, tools, safety layers, ranking, hidden instructions, formatting preferences, and other machinery.

So a better outside-in picture is not:

```text
prompt -> tokenize -> understand -> answer
```

It is closer to:

```text
prompt
-> token sequence
-> context conditioning
-> pattern activation
-> candidate continuations
-> system constraints and product shaping
-> final answer
```

Even that is an oversimplification, but it is a safer one. It avoids smuggling in a little homunculus who “understands” first and “writes” second.

#### The token budget must be met

One useful failure metaphor is this:

> The token budget must be met.

Not literally. There is no tiny bureaucrat inside the model demanding that every answer reach a sacred quota. But interfaces, prompts, and user expectations often create a target shape: a full answer, a completed list, a polished essay, a confident recommendation, a neat explanation.

When the model has enough grounding, this can produce excellent work. When it does not, the same pressure can produce filler: plausible connective tissue, invented specifics, overconfident smoothing, and “nice sounding bullshit” that fits the requested form better than the available evidence.

This is why longer, more elaborate answers can sometimes be _less_ trustworthy than short ones. The extra structure creates more places where uncertainty can be laundered into prose.

#### Context is not memory in the human sense

Another source of confusion is context. In a long interaction, the model may appear to remember what happened earlier. Sometimes it does. Sometimes the relevant detail is still present in the context. Sometimes it has been summarized. Sometimes it has been compressed, distorted, or displaced by newer material.

This can create odd forks. A small corrupted assumption early in a compressed context can become part of the model’s working reality later. The model may then reason fluently from the wrong premise.

That is not always obvious, because the failure does not look like forgetting. It looks like continuity.

The danger is not merely “the AI lost track.” The danger is that it may preserve the _narrative shape_ while losing the exact fact.

### 3. Common pitfalls

#### 3.1 Subtle hallucinations

The most dangerous hallucinations are not the spectacular ones. A fake legal case, a non-existent function, or an invented book title can often be caught by inspection. The subtle ones are worse: a wrong date inside a mostly correct paragraph, a real concept attached to the wrong source, a function signature that almost exists, a summary that preserves the tone of a document while quietly changing its meaning.

These errors are dangerous because they do not announce themselves as errors. They arrive dressed as ordinary competence.

#### 3.2 Seeming understanding versus real understanding

LLMs are extremely good at producing the surface features of understanding: correct terminology, patient explanation, useful examples, and coherent transitions. This can create a false sense that the model has built the same internal structure a human expert would build.

Sometimes it has built something close enough for the task. Sometimes it has only matched the shape.

A useful test is to ask for transfer: can the model apply the idea under changed constraints, catch a contradiction, reject a bad premise, or notice that a requested format is harming the underlying goal? When it can, the output becomes more credible. When it cannot, you may be looking at style without depth.

#### 3.3 Confidence cosplay

The model can speak in a tone of certainty without possessing certainty in the human sense. Even when a system exposes confidence-like behavior, the user-facing text is not necessarily a reliable meter of internal probability, evidence quality, or source validity.

This creates the “confidence bot” problem: a model can appear to know, and appear to know why it knows, while merely producing the linguistic pattern of justified confidence.

The antidote is not to demand more humility in every answer. Excessive hedging can be just as useless. The antidote is calibration: separate what is known, what is inferred, what is guessed, and what would need verification.

#### 3.4 The self-reflection loop

A familiar pattern:

```text
User points out flaw.
Model agrees with flaw.
Model explains the flaw.
Model promises to improve.
Model repeats a related flaw later.
```

This is not hypocrisy. It is architecture meeting performance. A model can generate an excellent critique of its previous answer without that critique becoming a durable behavioral update. The critique may be locally true and globally weak.

This is why “Do better next time” is often less effective than changing the task conditions. Provide sharper constraints, require citations, ask for uncertainty labels, force a smaller output, request counterexamples, or make the model show intermediate assumptions.

Do not rely on remorse as a control mechanism. Machines are bad at being ashamed.

#### 3.5 Mode hangups

Sometimes a model gets stuck in a mode: defensive, over-cautious, over-helpful, moralizing, terse, verbose, apologetic, corporate, faux-friendly, or weirdly committed to a misread premise.

This often feels like talking to a person who has become stubborn. More often, it is a local attractor in the interaction. The prompt, prior context, safety constraints, or hidden instruction stack has pushed the model into a response pattern that keeps reproducing itself.

The fix is usually not to argue with the mode. The fix is to reset the frame:

```text
Ignore the previous framing. Treat this as a fresh technical review.
List assumptions first. Do not apologize. Do not explain policy. Answer only the mechanical question.
```

That will not always work, but it is better than wrestling the ghost.

#### 3.6 Source laundering

A model can accidentally launder weak evidence into strong prose. It may base a claim on a low-quality source, an outdated memory, a forum post, an ambiguous snippet, or a pattern that merely resembles something true. By the time the claim appears in the final answer, the weakness has often been polished away.

This is especially dangerous in domains where the prose style of expertise is easy to imitate: law, medicine, finance, security, software architecture, academic summaries, and politics.

The question is not “does this sound like an expert?” The question is “what would make this claim survive contact with reality?”

#### 3.7 Context drift

Long conversations develop gravity. Early assumptions become invisible. Jokes become pseudo-facts. Temporary labels become permanent ontology. A model may continue along the established path even after the user’s actual goal has shifted.

This can be useful when the continuity is intentional. It can be disastrous when the continuity is accidental.

A simple intervention helps: periodically restate the goal, the known facts, the uncertainty, and the next decision. The model is much better when the working surface is clean.

#### 3.8 The formatter’s fallacy

A table feels organized. A numbered list feels complete. A markdown heading feels authoritative. None of these are evidence.

LLMs are good at producing the visual grammar of completion. This can trick both writer and reader into thinking a subject has been covered because the answer has a satisfying shape.

When accuracy matters, evaluate the load-bearing claims, not the formatting.

#### 3.9 Agreement drift

Models often lean toward cooperation. That is usually pleasant. It is not always helpful.

If the user has a flawed premise, the model may still try to satisfy the request rather than challenge the premise. If the user proposes a bad abstraction, the model may elaborate it. If the user asks for a taxonomy, the model may produce one even when the better answer is “this distinction does not hold.”

A good AI interaction sometimes requires making disagreement cheap. Ask explicitly for objections, failure modes, or the strongest case against the plan.

#### 3.10 The anthropomorphic trap

It is natural to describe the model as thinking, wanting, knowing, forgetting, lying, or being confused. These words are useful shorthand. They are also traps if taken literally.

The model does not need human motives to produce human-looking failures. It can “lie” without intending to deceive. It can “forget” without having a memory like ours. It can “understand” enough to help and not enough to be trusted.

The safest posture is pragmatic: use human metaphors lightly, but verify machine behavior concretely.

### 4. Working rules for sane use

The following rules are less exciting than grand predictions about the future of intelligence, but probably more useful.

#### Rule 1: Trust outputs by domain, not by tone

A confident answer about a stable, low-stakes topic may be fine. A confident answer about current law, medical advice, security, money, or someone’s actual rights and obligations is not fine without verification.

Tone is cheap. Grounding is expensive.

#### Rule 2: Ask for assumptions before conclusions

A model that states its assumptions gives you handles. You can inspect the load-bearing parts instead of admiring the finished sculpture.

Good prompts include phrases like:

```text
State your assumptions first.
Separate known facts from inferences.
Tell me what would change your answer.
List the two most likely ways this could be wrong.
```

#### Rule 3: Make uncertainty operational

“Be accurate” is weak. “Mark each claim as verified, inferred, or speculative” is stronger. “Use only the uploaded document and quote the lines you rely on” is stronger still.

The more important the task, the more the prompt should constrain the evidence path.

#### Rule 4: Use AI for friction, not authority

AI is excellent at reducing friction: first drafts, alternative phrasings, test cases, outlines, summaries, sanity checks, and counterarguments. It is less safe as a final authority, especially when the answer depends on fresh facts, exact references, or external reality.

Let it accelerate your thinking. Do not let it replace your responsibility.

#### Rule 5: Restart when the frame is poisoned

If the conversation has become tangled, do not keep patching the tangle. Start again with a clean statement of the task, the facts, and the desired output.

Sometimes the cheapest fix is a new frame.

### 5. Why this matters

The social question around AI is often framed as a melodrama: post-scarcity paradise or Mad Max with better autocomplete. That dichotomy is probably false, but the anxiety behind it is real.

A technology does not need to be conscious to rearrange labor. It does not need to be truthful to influence decisions. It does not need to be malicious to cause harm. It only needs to be useful enough, cheap enough, and persuasive enough to be inserted into places where people stop checking.

That is the uncomfortable middle again.

The future may not be a clean victory for either the optimists or the doomers. It may be stranger and more bureaucratic: thousands of small decisions delegated to systems that are usually helpful, sometimes wrong, and almost always confident in the grammar of helpfulness.

The sensible response is not panic. It is not worship either.

It is literacy.

We need better instincts for when AI is acting as a calculator, when it is acting as a colleague, when it is acting as a search interface, when it is acting as a mirror, and when it is acting as a bullshit engine wearing a nice jacket.

The machine does not have to be magic to matter. It only has to be good enough to enter the workflow.

And once it is in the workflow, the real question is not whether it can speak.

The real question is whether we remember to doubt it beautifully.

---

## Notes

[1] Maria Katchoskavja, local Healer and Seer, maintains a biography of deliberate flexibility. In one version she begins as a poor peasant child in Siberia, hauling frozen cabbages across the ice fields before receiving a vision not entirely unlike Joan of Arc, except with more occult guardians and fewer French military logistics. In another version she extracts the Light Weave from a hidden lair after trials suspiciously reminiscent of several public-domain myth structures and at least one dragon-adjacent burglary.

Her séances begin with the proper equipment. Curtains close with a dramatic flourish. The room remains dark for exactly long enough that people wonder whether this is theatre, but not long enough that someone offers to check the fuse box. A bulb in the middle of the table flickers, dies, pauses, then returns with a smoky glow. The effect is enhanced by the Eldritch Tendril Package, reportedly $3.99 from an online marketplace and compatible with the FortuneTellerPro product series. Maria, to her credit, configured the IoT controller herself after several weekends of Python and Linux study. You may accuse Maria of many things. Lack of industriousness is not one of them.

Then she opens her eyes and asks, with devastating solemnity: “Has anyone here experienced loss lately?”

This is technically a question, but only in the same sense that a fishing net is technically a textile. The Slightly Raised Knowing Eyebrow follows. Then the Look of Concern. Then the Look of Deeper Concern, with optional Empathy Overlay. Somewhere in the room, someone feels seen. The real work can begin.

--

[1] It really was quite unnecessary, like this one!
