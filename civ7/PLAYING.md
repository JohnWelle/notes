# Playing (Draft)

This document is, for reasons unknown to man, a needed companion for myself first and foremost at the time of this writing, to remember the cardinal rule (always remember), and then other random shit as the turns pass by.

## CARDINAL RULE!

This is the cardinal rule (always remember): DO NOT INSTALL ANY MODS WHATSOEVER

## Mods

Oh, you're still here smarty-pants? Well then. Have at it.

### Memento Editor

Game state sometimes leaks between a prevously played game when you attempt to create a new game with new leader, settings and mementos. This is probably not the memento editor's fault, but nevertheless, the unlock feature seems to randomly stop working. You can, however, still unlock adding the 3rd memento. Theory: The game state that is retained when starting a new game is missing the mod state or incorrectly carried over to a new game.

#### Proposed Fixes

##### IN-game state reset

- Simplest and quickest "fix" might be to go to Additional Content -> Add-Ons -> Disable User Content -> Enable User Content.
- If it's helping, it might be needed to go to Content -> UI Test and run a short while, 10 seconds or so, shouldn't matter but meh, who knows how and when state is assigned or reset under the hood. Anyway, it spins up the game engine to test graphics settings it seems. Needing the game engine for various resets or other probably dumb reason seems to be a thin. thing, example to level up all leaders to max level; apparently the mod literally cycles through all leaders and increment their XP gradually, so not possible to mutate directly, needs to be "played through".
- Unsubscibe/Subscrtibe
