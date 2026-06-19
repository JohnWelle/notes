# Project Doom Repository

This repository exists to provide a lightweight continuity layer between ChatGPT conversations and across multiple game sessions.

It is intentionally optimized for:

- Laziness
- Recoverability
- Archaeology
- Avoiding 10,000-message browser death spirals

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
3. Push directly to `main` (style points awarded for force-pushes)
4. Start a fresh chat
5. Upload `current.md` (preferred) or provide a public link
6. Upload only the screenshots that remain strategically relevant

The objective is not perfect memory.

The objective is fast rehydration.

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

## Image Selection Rules

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

## current.md Rules

`current.md` is the source of truth.

It should contain:

- Strategic objective
- Current game state
- Known facts
- Open questions
- References to relevant screenshots

It should not contain:

- Entire chat histories
- Long philosophical debates
- Detailed reconstruction of Kevin incidents

Summaries beat transcripts.

## Naming

Certain recurring concepts may appear in campaign notes.

Examples:

- Project Doom
- Project VROOM
- Bread Optional
- Priorities
- Kevin
- Nekheb

These names are considered self-documenting.

## Known Facts

- Great Walls can be built on mines.
- Rumpetroll is superior tadpole nomenclature.
- Fixed-width turn numbers sort correctly.
- Every piece of technical debt began life as a successful business decision.

## Unverified Theories

- Kevin.

```

```
