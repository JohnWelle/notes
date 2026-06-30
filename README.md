# Project Doom Repository

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
_... But some information requires more fidelity, specifically **game mechanics in detail** to enable meaningful strategic and micro level decisions_

The objective is fast rehydration with **sufficient degree of completeness**.
_... speed defined as time to go from rich context A to fresh context B with sufficient information, where sufficient can be seen as a dynamic variable with associated measures that we continuously improve or use to test out ideas [1]_

<sub>[1] Add `experimental` branch that we can use to test some wilder ideas. Branches and chat contexts are cheap, we should use them to accelerate learning. If not that, we can hope for hilarious failures in unexpected ways, which has an intangible value of its own! Some examples ideas that has been AI-Human slopped are `youtube-video-parser` methodology for AI to consume and generate a transcript of audio, frame summaries (ideally key frames but can be arbitrary interval, where the problem it solves is that the types of instructional/detailed videos I have in mind, most of the presented content has a strong anchoring in displaying game imagery and using the mouse to highlight some specific detail.

1. Validation:
1. Check technical feasibility of fetching YouTube videos, including any effect it might have on bandwidth or size limitation due to my account type, and whether its a reasonable use of compute resources, though.. if we can download YouTube, I mean **ALL THE VIDEOS**\_\*\*, on the back of a million Nvidia GPUs, well, it could be interesting!
1. Audio transcript fidelity, sanity check if it corresponds with YouTube CC text to see if something gets lost in translation. <strong>GATE</strong></sub>
1. Audio information quality, are we able to make sense out of it practically speaking ("ah, so if I buy that building and place it on a river or floodplains tile I keep the yields like when you build an improvement? That must be more powerful after the last patch, omg, gonna try, brb, one more turn...") I suspect _some_ degree of augmentation might be required, but we'll have to test and try.
1. Test Keyframe Comprehension Augmentation on a few sample videos from known good content sources. We can discuss presentation and organizing principles and details like KeyFrame intervals, e.g. how many images, megabytes and gigabytes in bandwidth and maybe storage and compute for image processing. **GATE:** How can we quickly test and see if it seems doable, if not we have some fallbacks we might be able to fallback to, e.g. parametrizable intervals or smarter solution that interprets significant changes in image and take snapshots `-B 4 -A 4 ` when change is detected. But we're probably going a bit too far by then.. tbd
1. Here we can branch off, but we should at least try to find a way to extract _actionable information_ from the overall content, e.g. key takeways, such as: "OMG FUCK!!! ISABELLA AND ICELAND IS SIIIICK, ITS GONNA GET BANNED IN MULTIPLAYER GAMES FOR SURE, HAVE YOU SEEN SUCH A THING 3 CIVICS LIKE BANG IN ASS OUT OF BOX WOOOOOW" (apologies for unexpected Tecumseh, see `/lore` for wildly unnecessary details and outrageous claims. At your own risk of course, you might have to sign a tiny little Release of Liability form along with a few obligatory medical checks and vaccines and oddly, extremely rigid enforcement of ID checks, even in unlikely places like that nice park surrounded by baton wearing private security patrolling diligently back and forth on the military-grade ramparts, with one job and one job only:

<details>
    <summary>
        <strong>Redacted</strong> | Contains inner layer of redaction, however, this layer of misdirection was unfortunately required since malicious black hat hackers discovered dark web ways to reverse engineer the original redaction and well, the media coverage... you cam imagine. This solution was graded "robust" after advanced UX tests using novel methods to surprise a reasonable percentage to AB test results between shocked and no-shocked participants, as well as the participation frequency in each group. Perhaps, surprisingly, more of the shocked people were willing to participate, if you mean chasing the UX people like angered tigers with pepper spray can be seen as participation. Despite these minor hick-ups, the test passed and I can therefore say with unlimited certainty that it is impossible for any entity, living or dead, man or Jesus Christ himself – famous break out artist, to reach past this barrier of inscrutable protection perfection. Anyway,  if you get past anyway and see something suspicious, please reach out to security@indian-asylum.smokecloud immediately.Label as Urgent and please include Attn:TECUMSEH in the subject for visibility and immediate RED level escalation.
    </summary>
    <h3>STOP READING NO IM NOT TACUMSEH I TYPE IN ALL CAPS BECAUSE THIS IS VERY IMPORTANT, DO NOT CONTINUE!</h3>
    <blockquote>
    BITCFUFUUUUUUH, SWEAR TO GOD AND BULL IN HIGH PLACE IF ONE MORE FUCKING FUCCCKKCKCCKCKK TIME JUMP ON SMOEN AN TEHY HAVE NOD ID I AMA FLIP SO BAD YOU NO IDEA, I WILL SHOOT ARROW IN FACE SOOOOO FF HARD HEAD ECPLODE IN MANY MANY BITS AND BLOOD AND SHIT AND THEN YOU WILL BE JUST PISS ON THE WALL AND I KEEP IT FOR LONG TIME SO TO WARNING FOR OTHERS OK CLEAR NOW DOCK ASSHOLE MONGO? OK NWO GO GET ME GUARD OVER THERE WITH NICE LOOKING ARM AND SEND HIM TO BUSH, GOOOOOOO I PISS ON YOU FUCK SHIT 
    </blockquote>

    <h3>TEST</h3>

    <strong>WORDS MAY APPEAR REDACTED</strong><em> -- author of redaction not original author comments: every single word in the text was individually tested through various heuristics resulting in an appropriate-ness score, and as an incredible statistical outlier, _every single word_ was deemed offensive in one way or another, we have never seen anything like it before, we are setting up a few more tests now, research grant wagon in motion!</em>

</details>

<!-- ```typescript
type YouTubeAIMagicSlice = {
  keyFrameImageUrl: string; // Overkill if no easy...
  ketFrameParsedRaw: YouTubeKeyFrameRaw; // Experimental type, tbd if value

  // TODO: s vs hh:mm:ss vs ?
  keyFrameSequenceNumber: number;
  keyFrameStartsAt: number;
  keyFrameEndsAt: number;

  totalProgress: number;
  totalLength: number;

  audioTranscript:
};
```
 -->
<!-- chapter descriptive-text-key | KeyFrame 1 <--- audio --> KeyFrame 2 chapters -> keyframe audio transcript + analysis based on combining audio and image data to create a more coherent whole; AI gets the fun job! -->

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
