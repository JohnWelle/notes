# Great Wall

Purpose:
Understand placement, adjacency, and optimization patterns for Ming Great Wall planning.

## Current questions

### GW-001: Irregular lattice adjacency

#### Questions

- Can rotated, inverted, staggered, or ugly Great Wall clusters preserve adjacency?
- As part of the same test, a tangentially related mechanic to test is whether there are any bonus adjacencies for having lattices on shared tiles

#### Why it matters

Terrain will not allow perfect layouts. If ugly layouts work, planning becomes much more flexible.

#### Current belief

Probably yes, but not confirmed enough to promote to rules.md.

#### Evidence:

- Pending screenshots / tile tests.

### Test Runs

#### 1. Lattice Test

##### Setup

1. Set up a new game with Exploration advanced start where all settings can be random or cutest leader [1], and Ming as the chosen civilization
1. Everything can be random settings, except: Choose Ming as the chosen civilization and a map type that isn't too coastal, e.g. a Pangea/Continents map should be fine.
1. Choose 4 towns in the initial setup phase and place them in a concentric pattern with the capital as the center node. Make sure that 3rd ring borders are touching to test settlement<->settlement patterns as well, e.g. adjacency across settlement borders.
   Place several irregular GW patterns and compare adjacency/culture output.
   Progress:
   [----------|||. . . . . . . . . . . . . ]

[1] **IMPORTANT**: According to Kevin when posed the question, oh game on the wall, who is the prettiest leader?

> Benjamin Franklin
>
> - Somehow has "enthusiastic grandfather who accidentally invents electricity while explaining a hobby project" vibes.
> - Not attractive-cute. Character-cute.

(I think he means attractive-cute too, he's just being shy..)

**T0** Init

- INIT: Advanced startup lets you settle your cluster as the first step (T0)
  - 1 city + 2 towns (8) (adds production vector to choose city over towns)
  - Drop all attribute points into culture -> research the Ming civic that enables GW (9 turns)
- SCIEMCE: Cartography

- GOVERNMENT CGOICE: The one with the GOLD! Purchase
- OBSERVATION: +70 happiness about 70 pop. Take note! Celebration => -15 science => 13 turns
- OBSERVATION: Towns will not fill their border potential ~2nd ring. Settle accordingly to make sure you build up connections. Cities 2-3 rings probably a bit terrain dependent on which tiles are 2 or 3.
- RESEARCH – WONDER: **Forbidden City**
  - Astronomy (10T | )=> Forbidden City (750)
- RESEARCH – WONDER: **Serpent's Mound** =>
- RESEARCH - MECHANICAL: Check if there are bonuses for garrissoned units on GW tiles

**T1-T8**

- Build basic infra and save

**T8**

- MISTAKE: Researched Cartography (10T) first, should have researched Astronomy (10T). Astronomy unlocks Serpent's Mound whic we definitely will shoot for HARD meow.
- Map tacks

**T9**

- RESOURCE COUNT: Check each town and city for antiquity resources (carried over to exploraion) as well as new resources. Counts are based on town/city full potential to 3rd ring; where there are overlapping tiles + resource the resource will be counted in the nearest town/city core, if tie, town/city closest to capital centre chosen. _!! Coastal resources not counted_.
  - CITIES
    - YIANGTHAN (21): A(n) E(n)
    - GUYIANG (19):
  - TOWNS
    - KAIFENG (8)
    - GUANGZHO (8)
    - GULIN (8)
    - HANGZHOU (2 – late settle)
- Map Tacks, define lattice clusters for Great Wall placement
  - Number of tiles, POTENTIAL (supports improvement)
  - Number of tiles, READY (has improvement)
  - Mumber of tiles, COMPLETE (ha)
  - Number of clusters => tiles:
- Produce and purchase as many GWs as possible with priorities (1) cluster (2) city since cities are more built out -> tiles and can both gold purchase and produce with hammers GW segments
- TODO: Let's check if there is anyway to more deterministically determine the resoure transition to exploration, specifically find answers to these questions:
  - Transitioning resources from previous age; a) which resources are _always_ carried over? b) are there any resources that are carried over with a probablity chance e.g. 50% chance of staying on tile. c) is there any chance that a carried over resource can change position to another tile?x
  - Placement of new age specific resources, a) which resources are available to add in the Exploration age? b) are there any weighting / distribution pattern that can be looked up, e.g. 5 bananas per 1 apple, or a % to denote chance of given up on a given tile, settlement or empire. C) will an improvenebt + UI on a tile "block" it for being assigned resources? That could be HUGE!

T10-Tn

- Continue to spend all gold and focus on buildng out GW tiles and improvements

T15

- Serpent's mound

Scaling shit

340 + 340*.5 + 340*1 + 340*1.5 + 340*2 + 340*2.5 + 340*3 + 340*3.5 + 340*4 + 340*4.5 + 340*5

#### 2.

N/A
