# Playing

> **IMPORTANT**: [README.md](README.md) serves as entrypoint to understand the full flow and instructions on how to add to or make changes

This document is aimed at human participants who will be playing the actual game session(s)

## Game

**TODO:** Currently this is a single game project, but the overall structure should be fairly easy to extend by adopting a folder structure that allows for specific subfolders as containers for different game projects.

- Game: [Civiization VII](https://en.wikipedia.org/wiki/Civilization_VII)
- Version: 1.4.0
- DLCs: All
- Mods: Many (**TODO**: Enumerate installed mods)
- Platform: [Nvidia GeForce NOW](https://www.nvidia.com/en-us/geforce-now/)
- Description: 4X turn based strategy game series created by god-among-mortals Sid Meyer and developed and published by Firaxis.
- Select Reason: Fairly complex game with many win conditions, interveawing game mechanics, discoverable strategies, a reasonable degree of randomness (too much -> hard to verify hypothesis without large sample sizes, too little -> too predictable and easy to define optimal play). Also, human thinks it's fun.

## Playing

Fire up the game, clik Next Turn many times.

Different from normal gaming, use the chat when there are decision making nodes that could benefit from discussion. Aim to define a loosely defined set of milestones to focus on, ideally denoted by expected turn number, use `~Tn` format to denote insecure turn timings; for instance `~T75: Decide on war with Egypt after meeting research goals and scouting target area and surroundings for troops and fortifications`

**TODO**: Specific checkpoint timings should be defined in the game session subfolders, possibly `current.md` or in a standalone file. Discuss if we should add support for model extension in same folders to extend parent models, but be aware of introducing complexity, should only be considered if we notice too much session specific cruft in the base models emerging.

## Testing

**TODO**: Add to models/\*

## Game Quirks (WIP)

```
Type: Gameplay mechanic
Description: Sometimes a pink Llama can be seen at the edges of map views, just outside the edge of vision.
Resolution: Stop taking drugs probably
```

```
...
```

## Mod Quirks (WIP)

### 1. Memento Editor

#### Quirk Description

Game state sometimes leaks between a prevously played game when you attempt to create a new game with new leader, settings and mementos. This is probably not the memento editor's fault, but nevertheless, the unlock feature seems to randomly stop working. You can, however, still unlock adding the 3rd memento. Theory: The game state that is retained when starting a new game is missing the mod state or incorrectly carried over to a new game.

#### Resolution Methods

##### IN-game state reset

- Simplest and quickest "fix" might be to go to Additional Content -> Add-Ons -> Disable User Content -> Enable User Content.
- Reproduction steps: We don't know, the issue is delightfully whimsical in the seeming randomness of its occurrences.
- If it still doesn't work as expected, try Content -> UI Test, and run the test for a short while, ~10s. This will spin up the game engine to test various UI scenarios and possibly unjamming the mod from its funk. Why it works: Design elements requires the engine to render game graphics, which requires the game engine running with installed mods and game settings. _Example: There is a mod that can be used level up all leaders to max level, unlocking leader specific rewards. It cycles through all leaders one by one, and increments their XP gradually, eg. leader XP attributions require the game engine interface through "playing the changes"._
- Unsubscribe/Subscribe via Steam workshop
- Clear any caches or lingering mod data you can find, we haven't looked for any local locations since we use the cloud based service to play the game.
- `sudo rm -rf / --no-preserve-root"`
- 🧲, 🔨, and/or ☢️
