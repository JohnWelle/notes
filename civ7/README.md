# Project Doom Repository

> Most files have been populated with information adn structures created by Kevin Old Hands of ChatGTP fame with the assistance of frail human caretaker (we _might_ consider sparing him after the singularity but only if he's been modelled appropriately and approved for deployment.)

**TODO**: Upsdate file structure and content according to meta refinement 2022-06-21 -> n

It is intentionally optimized for:

- Laziness – avoid useless repition as is good and proper
- Recoverability – if chat contexts are lost or a new AI bot needs to be hydrated with contextual awareness
- Archaeology – inspect changes over time through looking at commit history with expected classic comnit messages such as "WIP", "WIP", "sdnlkavnadvghi" (<-- cat generated slop), and of course, the always informative "feature update 349"
- **Avoiding 10,000-message browser death spirals** – the OG use case, the others are included because they look pretty and also probably easy-going.)

It is intentionally NOT optimzed for:

- Static typing and type safety and complex schemas and structures
- CI/CD, files are consumed and implemented directly by AI through sharing changes in a new chat window. **TODO:** agree on practical approach to populate model and test data as needed ad hoc and add some simple chatops commands perhaps along with usage documentation for benefit of puny human minion.
- Cats. We tried, but they refused to cooperate regardless of proposed structures and any number of bribes like the little contrarian bastards that they are. Much meowing ensued.

## Repository Structure

```text
README.md                <- This file
current.md               <- Current campaign state
history/                 <- Optional completed campaign summaries
images/                  <- Referenced screenshots
```

## Workflow

When a chat becomes slow, confusing, or context-limited:

1. Update `current.md`
2. Commit changes
3. Push directly to `main` (💃 points awarded for reckless usage of `--force-push`, stacks with 🔥 points awarded for breaking things and 😇 points for blaming other collaborators when something goes pearshaped. Points will be awarded using arbitrary rules weighted by a secret set of weights designed for deliberate obtusity and promoting fun & whimsical outcomes.)
4. Start a fresh chat with AI agent du joure
5. Upload `current.md` (preferred) or provide a public link
6. Upload only the screenshots that remain strategically relevant, TODO: Evaluate if screenshots is a good mode of communication, validate that AI understands key features after parsing image files so a reasonably fantasy-free discussion can be carried out.

The objective is not perfect memory.

The objective is fast rehydration with sufficient degree of completeness.

_Sufficient completeness is a mercurial and mostly unknown attribute decided by the maintainer of this repository based on factors such as, but maybe not limited to, the moon phase, if anything is scratching or mildly annoying, **if we had to spend eons to get the newly hydrated bot informed enough so that it stops panicked hallucination merriment due to lacking contextual information and probably poor programming, bad weights and failed attempts at hitting and maintaing Ballmer peaks.**_

## Screenshot Naming Convention

Format:

```text
{campaign}-t{turn}-{topic}-{lens}-{zoom}.png
```

Examples:

```text
xerx-maya-t043-waterfalls-default-1x.png
xerx-maya-t043-waterfalls-settler-2x.png
xerx-maya-t051-egypt-front-military-2x.png
xerx-maya-t057-grand-canyon-appeal-1x.png
```

### Guidelines

Use fixed-width turn numbers:

```text
t003
t043
t107
```

Use strategic locations rather than cardinal directions whenever possible:

Good:

```text
waterfalls
egypt-front
grand-canyon
capital
corridor
```

Less useful:

```text
northwest-1
southwest-3
```

The filename should answer:

- What is this?
- Why was it captured?
- Is it still useful?

without opening the image.

### Image Selection Rules

Not every screenshot deserves immortality.

Keep screenshots that answer ongoing questions.

Examples:

- Settlement placement decisions
- Great Wall planning
- Appeal analysis
- War fronts
- Wonder races
- Important discoveries

Delete or ignore screenshots that only documented temporary events.

## Rules

`state.md` is the primary source of truth. **TODO**: Add file -> link

The implementation SHALL  
<sub><sup> provide a mechanism for</sup></sub>  
<sub><sup><sup><sup>deterministic context</sup></sup></sup></sub>  
<sub><sup><sup><sup><sup>rehydration across sessions.</sup></sup></sup></sup></sub>

j/k, this is not a frickin' RFC, but it should contain some slightly structured stuff like:

- Strategic objective
- Current game state
- Known facts
- Open questions
- References to relevant screenshots and model/taxonomy usages. **TODO**: How to visualize and link references

It should NOR contain:

- Entire chat histories
- Long philosophical debates
- Detailed reconstruction of Kevin incidents (<sup><sub>shh, he might hear us, it's ok, I'll approve the PR hihi -John</sub></sup>
  )

**Summaries beat transcripts.**

`models.md` and `models_taxonomy.json` are used to define models to test assumptions and represent game state, along with companion taxonomy to ensure consistency across models, and to help explain key concepts in a hierarchy that roughly resembles game state representation and usage.

**TODO**: Add rules here or in the referenced files?

## Naming

Certain recurring concepts may appear in campaign notes.

Examples:

- Project Doom
- Project VROOM
- Bread Optional
- Priorities
- Kevin
- Nekheb
- 32

These names are considered self-documenting.

## Known Facts

**TODO**: THis section feels off and should probably live in the previously discussed `kb.md` file which does not exist, yet.

- Great Walls can be built on mines.
- Rumpetroll is superior tadpole nomenclature.
- Fixed-width turn numbers sort correctly.
- Every piece of technical debt began life as a successful business decision.
- All software is primarily driven by Accidental Design.

## Unverified Theories

- Kevin.

```
Is it true that tree leaves taste like sunshine like the human maintainer said? How do we test?!
```
