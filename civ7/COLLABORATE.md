# Human + AI Collaboration Style Guide (Draft)

## Purpose

This document captures lightweight conventions intended to improve long-running collaboration, context transfer, and decision quality.

The objective is not perfect state tracking.

The objective is to preserve enough context that future-us can reconstruct the reasoning behind past decisions.

---

## Core Principle

State is cheap. Context is expensive.

Screenshots preserve state.

Notes should preserve context.

Context primarily consists of:

- Why we did something
- What we believed
- What we were uncertain about
- What changed our minds

---

## Context Reconstruction

Important game developments should be communicated in a reasonably structured format.

The purpose of structure is not bureaucracy.

The purpose of structure is to preserve context over time.

Future-us should be able to understand not only what happened, but why it mattered.

---

## Communication Philosophy

Prefer:

- High signal
- Low maintenance
- Human-readable notes
- Descriptive filenames
- Lightweight structure

Avoid:

- Detailed turn-by-turn logs
- Administrative overhead
- Maintaining perfect state
- Process for its own sake

If a process becomes tedious, simplify or remove it.

Preserve enthusiasm.

---

## Screenshots

Screenshots are primarily used to preserve state.

Use descriptive filenames whenever practical.

Examples:

- `t055-waterfalls-city-vs-town.png`
- `t055-egypt-doom-front.png`
- `t055-grand-canyon-overview.png`

Descriptive names are preferred over cryptic identifiers.

---

## State Updates

For routine play, communicate deltas rather than complete state.

Example:

Done:

- Settled Waterfalls
- Built Great Library

Learned:

- Egypt located northwest
- Gold economy stronger than expected

Need:

- Decide city vs town

---

## Inflection Points

When a significant event occurs, preserve the causal chain.

Preferred format:

What happened?

Why do we care?

Example:

Saw Egyptian settler north of Grand Canyon.

Why we care:
Could explain location of missing third settlement.

---

## Strategic Memory

Record only information that future-us is likely to regret forgetting.

Examples:

- Unusual AI troop movements
- Wonder races
- Diplomatic shifts
- Major economic changes
- Important discoveries hidden by fog of war
- Significant opportunity-cost decisions

Do not attempt to preserve every event.

Preserve meaningful events.

---

## Mechanic Testing

When source quality is weak, prefer direct in-game testing.

Principle:

Prefer direct in-game tests over weak external sources when the test is cheap.

---

## Mechanic Test Format

Template:

TEST: <NAME>

Q: Question being tested

H: Hypothesis

M: Method

Status: OPEN | TESTED | BLOCKED | RETEST

Confidence: TRUSTED | LIKELY | UNTESTED | WRONG | STALE

Owner: Optional

Example:

TEST: GW-LATTICE-ADJACENCY

Q: Do isolated adjacent Ming GW tiles provide adjacency bonuses?

H: Yes. Adjacency is tile-based rather than segment-based.

M: Create isolated GW patterns and compare yields.

Status: OPEN

Confidence: UNTESTED

Owner: John

---

## Confidence Definitions

TRUSTED

- Directly observed or tested in-game

LIKELY

- Strong evidence, not directly tested

UNTESTED

- Plausible but unverified

WRONG

- Disproven

STALE

- Previously true but potentially invalid due to patches or version changes

---

## Final Rule

The goal is not to preserve everything.

The goal is to preserve enough information that future-us can quickly recover the reasoning of past-us.
