# Playing

> **IMPORTANT**: [README.md](README.md) serves as entrypoint to understand the full flow and instructions on how to add to or make changes

This document is aimed at human participants who will be playing the actual game session(s). We will not provide any specific

## Game

> Currently this is a single game project, but the overall structure can be fairly easy to extend by adopting a folder structure that allows for specific subfolders as containers for different game projects:
>
> Current:
>
> Multi-game:

- Game: [Civiization VII](https://en.wikipedia.org/wiki/Civilization_VII)
- Version: 1.4.1
- DLCs: All
- Mods: Many (**TODO**: Enumerate installed mods)
- Platform: [Nvidia GeForce NOW](https://www.nvidia.com/en-us/geforce-now/)
- Description: 4X turn based strategy game series created by god-among-mortals Sid Meyer and developed and published by Firaxis.
- Game Setup:
  - Map: Fractal Continents
  - Size: Large
  - AI Players: 9
  - Independent States: 24
  - Leader: Tecumseh
  - Antiquity Civilization: Tonga
  - Exploration Civilization: ...? Likely Hawaii but to TBD finally
- Select Reason:
  - Test classic pairing with a few new ideas centered around various meta concepts that are being discuss different civ-communities and YouTube channels:
    - **Prerequisite Knowledge: Rural vs Urban Meta**. Patch v1.4.0 introduced a severe overhaul to some of the core game mechanics that has had a significant impact on what is considered "optimal play". See [nomenclature](#nomenclature) to find detailed descriptions of common terms
    - **Classic Tecumseh & Tonga in New Meta**
      - The pairing of Tecumseh and Tonga was immediately found; Tonga has scouts that can traverse oceans as the only civilization in the game in the Antiquity era. This means that this combo, on a typical continent based map type, will have access to _at least_ twice as many Independent States (later to become City States if suzereined). Tecumseh is the leader that arguably has the most beneficial bonuses towards suzereining, and reaping benefits thereafter.
      - In the new Meta this combo has probably faded a little in the background since their strong synergy does not seem to be particularly gained or harmed by the meta changes. But, what if we made a few tweaks and see what happens? Yes, it might be fun!! Or bomb totally but we're finding out...
      - Variation:
        - Volcano Engine: Set disaster level to Catastrophic and roll for a good volcano start. We are jacking the volcano fueled yield games as part of a more rural-centric strategy to catch those delicious bonus yields.
        - Coastal Preference: Tonga has a lot of bonuses towards coastal terrain adjacencies and bonuses on coastal rural improvements and resources, eg. fishing boats. This is nothing new, but we try to go more aggressively for coastal-first to make sure we set up an _engine_ which will not reach full potential until Exploration, or if we choose to pivot have been an important part of the rural/fishing/volcano experiment to see how well it works.
        - Open: The _most likely_ win condition to go for is probably culture due to the availability of very good coastal civs in Exploration. The aggressive suzereining of City States means we will have a diverse set of bonuses and yield income types. TBD!

### Nomenclature

**City Specialist**. When a city grows and there are open spots for specialists, the player can optionally choose to populate a specialist slot for a happiness/gold price to gain other yields, ideally in total net positive numbers, but some yield types are more desirable than others such as hammers, science and culture so it can be a calculated decision to go with a small net loss if the conversion is deemed net beneficial.

**Urban** (tile): A tile becomes urban once a building has completed on it to form a _district_, then it is _irrevocably_ transformed to an urban tile. An urban tile always have two district slots. When a tile has received two buildings so that the two districts are populated it is renamed in the game to a _quarter_, the distinction plays a role since there are various bonus systems attached to both urban districts and quarters, though quarters has more/better availability. The transformation to an urban square will almost always remove the yield and use the building provided yield instead.

**Rural** (tile): A tile with valid terrain type to place an _improvement_ e.g. plantation, fishing boat, mud pit, woodcutter, quarry, mine, farm. When it has been improved it can then be further stacked with Unique Improvements, a rural building type that stacks with the tile yields rather than replacing.

Fairly complex game with many win conditions, interveawing game mechanics, discoverable strategies, a reasonable degree of randomness (too much -> hard to verify hypothesis without large sample sizes, too little -> too predictable and easy to define optimal play). Also, human thinks it's fun.

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

343 x
