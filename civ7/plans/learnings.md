# Learnings And Quirks

It's interesting to approach modern LLM AI from the perspective of breaking down / reverse engineering different modes, strictures and limitations in modelling, data structures, retention policies, reduction artifacts, ... all the things.

Here are some of my observations:

1. Never trust AI. NEVER. Except if you have a medical emergency, then it's probably better than calling your local Healer and Seer, Maria Katchoskavja [1]

1. Subtle Hallucinations Danger Zone

1. Real Understanding vs Seeming Understanding

1. Self-Reflection Dilemma -> Retrospective Analysis Agrees with Flaw -> Promise To Improve and Adapt -> Rinse and Repeat. Back to rule 1

1. Mode Hangups. When AI gets stuck in a particular defensive mode, perhaps some edge case triggered that makes it entirely confused and (more) useless than normal.

1. Confidence Bot – impossible to consistently make AI use evaluations of confidence levels to stop going into con-bot mode where it will happily lie through its teeth based on anything from thin air emergent properties to shit-posting on some unknown forum, but certainly guarded by any mechanism to effectively filter bad data. [todo: maybe move this somewhere ekse or as a footnote, too long] Or perhaps more concretely; it seems like roughly the following is true:

prompt
->
parse prompt
->
tokenization pipeline pass #1
->
find high % matches, maybe confidence used initially as filtering mechanism, maybe represent as an AST but would not surprise me the least if it's markdown all the way down!
->
evaluate response
->
criteria met -> pass on to the put-on-makeup and a new dress pipeline before responding
->
criteria not met (36% confidence, 3 passes)
->
function to evaluate % confidence and number of passes to determine next step
->
pass, recurse
->
do not pass, go to new fun magical pipeline Token Budget Must Be Met pipeline where things tend to get funky...

For sufficiently simple and constrained prompts (not requiring too much back and forth context [1]), this typically works very well and why LLM AI takes up a lot of space currently, both among investors and regular people noticing its effects in the workplace or at home or just as hobby enthusiasts.

It's more than just a fancier Alexa though, it has possibly, though probably not according to this observer, ground-breaking, cataclysmic (insert dramatic word) consequences for society at large, e.g. will this mean a complete overhaul of how we divide labor, akin to the tumultus changes following the Industrial Revolution, or.. worse? Maybe 20% become redundant, maybe 50, maybe all! What will happen then? Can we trust Big $ Venture Capital Bros to consider the social impact of this particular technology and offer mitigations and safeguards on the implementation level, or.. Should they even? We get back to the age-old discussion about whether its possible or even desirable to curtail technology and science with artificial regulations, but people might turn to their politicians nevertheless; "something must be done" they'll say. The politician might try to understand the pitfalls, maybe they will succeed, and act quickly with sane regulations and spearhead international initiatives, or.. they might just pretend to do something about it for a while, secretly hoping it just all goes away. Perhaps the more realistic option.

So where does that take us? Post-Scarcity vs. Mad Max seems to be a common dichotomy used when discussing the emergence of AI and possible outcomes at the tail end. It smells like a false dichotomy, and it probably is, but.. the concerns are real, at least in the sense that they are felt. People are thinking about AI, some with concern, some with an eye for possibilities, some with a slight yawn and a knowing smirk, thinking "let the games begin..".

[above and below should not be connected here, different style, different content, refactor]

If at some point its token budget is spent, e.g. response is at an unsatisfactory percentage of completeness, we get in addition:
-->
fill in missing bits with nice sounding bullshit, no matter where it comes from.

The Token Budget Must Be Met.

[1] I would _guess_ that context compression is a process that is running continuously as opposed to the on-demand tokenization. It will have impact though, since it can lead to interesting forks if compression has led to a corrupted "fact" making the evaluation criteria wrong at an early stage. But that is clearly just one of many possible failure modes.

, nevertheless keeping the exact score/references as part of some global state in the tokenization process that can be used in the final output as visible decorators to each segment in the reply. Maybe you see something obviously incorrect presented in a self-assured way, and ask: "Oh, how did you derive X here? What is your confidence and how did you derive it, sources?". Sometimes you can actually get a real (or at least real sounding) answer stating that source X or Y was used and confidence was high because so and so. Other times it will just say it couldn't recreate it because that's not how we roll with tokens and shit, bitch. Or well, not exactly that.

[1] Her background is shrouded in deliberate mystery, malleable in structure to allow for adaptations depending on audience, but generally something along the lines of [timeline representation]:

--> Poor peasant upbringing in Siberia, carrying frozen cabbages from the vast ice fields and hacking like chopping wood so they could eat that day at least.

--> Vision and message from God somehow eerily similar to Joan de Arc -

--> Quest to extract the Light Weave from the Occult Guardian working for Unknown Ascendant with Deep Powers and Ambiguous Agenda with Many Dangerous Trials (accidentally, surely, not at all dissimilar from Oddysey's Trials)

--> Snatched it from the Guardian Lair by being clever little girl (somehow similar to the part in The Hobbit when Bilbo outwits Smaug)

--> [Placeholder for emotional manipulation bit for current audience]

--> Fled to the Americas (or where she may currently reside) after [witch hunt facsimile], all good now!

Then, Maria cuts the silence:

"And Here We Are Gathered..."

Thought seemingly aborted, she closes her eyes, and takes a deep breath, appearing to gaze inwards. Eyeballs darting to and fro under the lids, seeming to indicate that a great number of things are currently under Divine examination, and that she might not be in entirely the same dimension, time-wise or otherwise, as the audience. [footnote about using this time to make mental shopping list].

Then, eyes opening suddenly, she's back among the present in our dimension.

"Has Anyone Here Experienced Loss Lately?"

Needless to say, delivered with a tone that conveyed that she very much meant that as a rhetorical question as her Divine Powers had gathered as much from reading the Spirit Energy in the room already thank you very much.)

This then, followed by the staple Slightly Raised Knowing Eyebrow – a common facial addon to the Rhetorical Question package ["rhetorical question of the face"] - Again, she is slowly scanning the room, a little pacier now and without the intermittent pauses for eye contact, until.. She stops. Gaze fixed and screwed up at maximum intensity, she now deploys the Look of Slight Concern add-on to the Raised Eyebrow add-on. Her face starts to shift, by various contortions, from Concern, Understanding, Random Surprise, before landing in some variation of Empathy. This seemed to paint a picture that for the recipient seemed to – again _eerily_ – translate to sympathy for their inner turmoil and feelings of sorrow, pain.. almost as if the soul was laid bare for her to see –– _**she sees me?**_

Now the real work could begin.

Prosecuted a bit, fled here and there, now all good, see? [Closes curtains with a dramatic and sudden flourish, room now shrouded in darkness for exactly 3.4 seconds, the perfect artistic pause duration to make sure people start to wonder "what the huck is going on here?" but arrested before "did a fuse blow? I better offer to help..". She taps a hidden button on the floor, then something starts to emanate from the large bulb on the circular table they are all seated around – [footnote -->] as one would expect, this is not the time and place to subvert expectations, Maria knows this better than most – first a few intermittent flicks, then suddenly dark again followed by a new artistic pause - for obvious reasons is a bit shorter this time (1.3s-1.5s), before a steady light starts to slowly build amid swirly smokey effects, some times cut by tendrils contracting and expanding all spooky-like [footnote --> Eldritch Package, $3.99, Ali Baba – only compatible with FortuneTellerPro product series]. Then "All Gathered Here..." (having learnt the art of making every word said Capitalized and possibly of some Hidden Occult Significance, [footnote or cut] sometimes causing issues at breakfast when discussing who toasts the bread and gets the kids out for school with their lunch meals packed and so on. [rephrase art/package thing and transition to ALL CAPS] It's not an art you just turn off, so, "Kramushka, Take On Your Wool Hat So Your Ears Don't Freeze Or So Help Me Babushka I Will Slap Your Ears So Hard They Fly Off Like Cabbage Leaf In Bad Storm, And Maybe Then You Will Think About Not Being Stupid Little Shit, Eh?" – in this case, the ALL CAPS package would have been a better fit for the use case.)

Yes, I did that, I turned it into a gender stereotype punchline for no discernible reason. Sue me, ha!

## Bits

...[probably merge with planned footnote for eldritch package] -- including the "eldritch tendrils package" show until the room is dimly lit by an eerie, bulb controlled by a IoT At Home package bought from Ali Baba and programmed by Maria after she had spent some weekends picking up basic Python and Linux skills.

You can accuse Maria for many things, lack of industriousness is not one of them.

when living as peasant girl in Siberia, very much Joan de Arc style progression"
briefly summarized as "extracted the Light from the Occult Guardians when living as peasant girl in Siberia, very much Joan de Arc style progression". Then, and only then, might AI be a better alternative. Marginally so.

with wild, fantastical claims about her past life in Siberia where occult secrets are still guarded, ... (many Russian occult powers). Marginally.
