# Civ 7 AI Experiment

> **IMPORTANT!** This document is deprecated but kept for historical reasons and possible cherry-picking useful bits... Use [sessions/README.md](sessions/README.md) as entrypoint. It will be refactored eventually. Maybe!

---

This repository exists to provide a lightweight continuity layer between ChatGPT conversations and across multiple game sessions.

Etymology: We are not quite sure how the name _emerged_, but it was at some time chosen as the "project name" for reseaching the viability of waging bloody war against Egypt, our only real threat at that poimt. It has since then, after a few iterationss, morphed into becoming the name of the entire project, e.g. speaking broadly, a Human<->AI Complex Problem Solving experiment, with focus on quick iterations and quantifiable, _practical_ measures to improve learning and produce objectively better results.

It is intentionally optimized for:

- Laziness
- Recoverability
- **Avoiding 10,000-message browser death spirals**

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
6. Add any screenshots that can help provide more context to the current state, e.g. map overview, production stats, and so on.

The objective is not **perfect memory**.
-- Exception: Some information requires more fidelity than other, specifically **game mechanics in detail** to enable meaningful strategic and micro level decisions

The objective is fast rehydration with **sufficient degree of completeness**.
-- Clarification: Speed to gp from rich context A to fresh context B with sufficient information to get started directly; speed of compute or time to make structural changes in this repository are sevondary.

<br />
<details>
  <summary>
    Example: macro/micro flow of a turn
  </summary>
  <Br />
  <em>Background: Turn 30 in age Antiquity (1/3 defined ages) a checkpoint is set to discuss future war plans and its implementation.</em>
  <Br />
  <table>
    <thead>
      <tr>
        <th>T</th>
        <th>Turn State</th>
        <th>Decision Type</th>
        <th>Action</th>
        <th>Notes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>30</td>
        <td>City.production</td>
        <td>micro.research</td>
        <td>
          Finished Settler, add new item to build queue:<br /><br />
          <ul>
            <li>Civilian Unit: Settler (5)</li>
            <li>Military Unit: Horseman (4)</li>
            <li>Military Unit: Archer (3)</li>
            <li>Military Unit: Spearman (3)</li>
            <li>Production/Military Building: Blacksmith (12)</li>
          </ul>
        </td>
        <td>Only realistic build options included to reduce noise</td>
      </tr>
      <tr>
        <td>30</td>
        <td>City.production</td>
        <td>macro.discussion</td>
        <td>
          Focus: Start war against Egypt as she is threatening our win condition
          (culture). We have decided that we need to do something, the question
          is when the optimum time to strike based on war goals.<br />
          <ul>
            <li>
              Option A: Start building units immediately and optimize
              time-to-war as much as possible: Early win => better terms for us
              => reduce overall war effort by enabling a narrower goal due to
              time bought [rationale] ...
            </li>
            <li>
              Option B: Balanced. We have some key buildings that we want
              regardless for later purposes, building Blacksmith now would
              increase production by 20% so depending on total number of units
              needed, we could shave the total amount of turns and be ahead a
              building... [much discuss]
              <ul>
                <li>
                  1: Scout Variant. Build additional scout and send toward enemy
                  in addition to any in field (1). Delay improves knowledge,
                  e.g. enemy unit dispositions and any undiscovered land they
                  may have.
                </li>
              </ul>
            </li>
          </ul>
        </td>
        <td></td>
      </tr>
      <tr>
        <td>30</td>
        <td>City.production</td>
        <td>micro.action</td>
        <td>
          Start producing Blacksmith (12) according to decision, look for
          production/turn improvements that
          <span style="font-style: italic">can</span> be done at various costs
          to improve production and thereby shave turns, also known as "shaving
          turns" or min/max approach.
        </td>
        <td>Noticed trick to reduce production by 1 turn ...</td>
      </tr>
      <tr>
        <td>30</td>
        <td>Town.Focus</td>
        <td>micro.research</td>
        <td>
          List options available (Fort Town, Tourist Resort, Fishing Village,
          etc.) along with critical stats, where growth rate and yield output is
          the most important to form decisions, though there could be additional
          variables such as ongoing war effort and strategic location...
        </td>
        <td></td>
      </tr>
      <tr>
        <td>30</td>
        <td>Town.Focus</td>
        <td>macro.discussion</td>
        <td>
          Town was settled with the purpose of becoming a City – this is
          typically part of general expansion strategy when choosing locations
          for a new settlement. Discussion: Cost 400 gold to ... tempo gain by
          early conversion, e.g. earlier -> earlier building X producing Y ->
          cumulative value of getting Y 1-n turns earlier
        </td>
        <td>
          Could afford to buy an additional scout as well, how much information
          do we need and how long to connect (count movement speed, distances.
          enemy teorritory etc.)
        </td>
      </tr>
      <tr>
        <td>30</td>
        <td>Town.Focus</td>
        <td>micro.action</td>
        <td>
          Convert Town to City, -400 gold. Total gold available after:
          <strong>233</strong>
        </td>
        <td></td>
      </tr>
    </tbody>
  </table>
</details>
<br />

> **TODO:** links.nd
> Trusted sources for game mechanics and different leader characteristics etc. These are large community-driven initiatives, not official game developer documentation, but they are generally much more detailed and updated frequemtly as gamee mechanics change. That is not to say that all information is 100% verifiable. For more advanced dynamics there are still some topics that noone seemingly have the answer to, so game of unknowns indeed!
>
> - https://civilization.fandom.com/wiki/Civilization_VII
> -

### current.md Rules

`current.md` is the source of truth.

It should contain:

- Strategic objective
- Current game state
- Known facts
- Open questions
- ~~References to relevant screenshot~~

It should not contain:

- Entire chat histories
- Long philosophical debates
- Detailed reconstruction of Kevin incidents

Summaries beat transcripts.

<sub>Re: Screenshots</sub>

### Naming

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
Salmon...?<sub>?</sub>
```

> > > > > > > > > >
