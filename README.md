# Project Doom Repository

<img width="845" height="247" alt="image" src="https://github.com/user-attachments/assets/375ae5d5-4ca2-4f56-bc0b-38d2a9d8e8d4" />

<sub>*Cutout from AI generated versiob of something you'd never guess the prompt for, nor, naybe, what it is supposed to look like. But it FUCKS!*</sub>

> **This repository exists to provide a lightweight continuity layer between ChatGPT conversations and across multiple game sessions.**

It is intentionally optimized for:

- **Laziness**
- Recoverability
- ~~Archaeology~~
- Avoiding 10,000-message browser death spirals

<sub>Archeology: We strike archeology instead of removing it for archival purposes! In seriousness, we will have the builtin history benefits of git/GitHub and we will use a simple subfolder structure to keep track of individual gane session states, ex: `/sessions/some-descriptive-name/...`</sub>

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

Except: It is necessary to transfer basic game mechanics to have meaningful discussions on both the macro and micro level. As we will learn, at neither level is it possible to make meaningful decisions without imvolving both. Fictional game example: 

> <dub>**macro:** win through conquest, micro: build, military in stable or castle (3-4 turns per unit),  10 turns to produce blacksmith increasing overall production with m units, macro: we build blacksmith because we can await unit production until we have scouted nearby enemy closely, we should build a scout first, then blacksmith, that's 13 turns total, and scouts have then 10 turns to travel to and check enemey territory, ... _informed discussion ensues_</sub>

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
