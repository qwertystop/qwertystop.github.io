---
layout: default
title: "An Analysis of Platform Games"
category: analysis
tags: games
---

## Some context
This piece was originally written as a class project; I have decided to present
my results in hypertext because I need to include images and video. Also, the
blog-post format allows for a slightly nicer tone than a formal paper.

The class, as a whole, was about the concept of originality, and the varied
ways in which creative works can draw on earlier, preexisting works. The
project could be basically anything, as long as I was able to plausibly claim relevancy.

## The Data-Driven Approach…

At first, the most interesting topic I could think of was to perform a
data-driven analysis of… something. I decided fairly quickly that games –
specifically, [platformers](https://en.wikipedia.org/wiki/Platform_game) –
would be a good group to work with – something I had a decent amount of
experience with, and constrained enough in gameplay that I could come up with a
slew of questions to ask about any given game without needing to put `N/A` too
many times. Additionally, the genre is old as such things go – and still fairly
popular – which gives a nice, wide variety of titles to pick from. This also
allows me to include and several very long-running series, and thus explore
any design patterns that might show up in them.

In the end, I settled on twenty different fields. Each is named below, along
with its defining question and any elaboration that felt necessary.

### Series:
- **What series is the game in?** Since my process was to keep adding games
  until I ran out of time, and since seriality wasn't the only thing I was
  trying to explore, there are games with no series here, as well as series
  where I didn't include all of the games.

### Subgenre:
- **Does the game fit into any smaller category within "platformers"?** These
  are unavoidably subjective; I came up with four.
- *Action* refers to a platformer where the actual platforms are more often a
  setting for combat than an agility or navigation challenge. Combat is
  generally some mix of easily-dispatched enemies and significant boss fights,
  with few or none in a middle-ground.
- *Challenge* platformers, in contrast, have little or no combat and a very
  strong focus on difficult movement-based challenges, each challenge usually
  being fairly small and contained. High precision and low reaction times are a
  must.
- *Collectathon* is... slightly negative, as a term, I'll be honest. These
  games are about hunting through a large world for hidden things. New content
  is gated behind semi-arbitrary counts of how many such things you've already
  found. Usually, there's several types of things to collect, and the things
  you're finding are more often scattered or hidden, rather than being placed
  explicitly as the targets of distinct levels or challenges.
- *Metroidvania* is, contrary to how it sounds, a fairly widespread name for
  the category. These are games where the player explores an interconnected
  world, continually gaining new abilities and/or learning skills and mechanics
  that allow them to access an ever-increasing portion of that world.

### Secondary genre:
- **Does the game fit into any genres besides "platformer"?** The only genre I
  found among the games I included was *RPG*, short for "role-playing game" and
  referring to games with some form of progression of capabilities for the
  player-character, as well as (usually) a significant narrative aspect.

### Year of release:
- **What year was the game initially released in?** Remakes don't count, and in
  cases where the game was released to different markets at different times, I
  used the earliest. This doesn't completely pin down the environment at the
  time of development, since games might take more or less time to make, but
  still gives enough context for the potential of some sort of progression.

### Primarily vertical or horizontal:
- **In what direction does the player traverse the world?** Valid values are
  *Horizontal*, *Vertical*, and *Mixed*.

### Backtracking:
- **Is the player often required to cross the same areas multiple times?**
  Valid values are *Yes* and *No*.

### Physical structure:
- **Does the player commonly have multiple valid routes by which to progress?**
- Valid values are *Open* (indicating many choices), *Linear* (indicating no
  choices), and *Mixed* (indicating long alternating periods of one or the
  other).
- If there's only one correct route but also one or more incorrect routes
  (dead-ends, optional areas, places to return to later), and exploration is
  required to know which is which, that counts as multiple routes.

### Jump combat:
- **Is the standard "jumping" action also used to dispatch enemies?** This is
  distinct from an action with the primary purpose of attacking, which
  incidentally causes vertical movement.  Valid values are *Yes* and *No*.

### Melee combat:
- **Is there an action dedicated to attacking enemies near the player
  character?** For example, a sword-swing, punch, or a projectile with
  extremely limited range. This does not require that the game visually
  displays some form of physical contact, only that the attack has a small
  maximum reach.  Valid values are *Yes* and *No*.

### Ranged combat:
- **Can enemies be fought at a significant distance?** For example, guns,
  archery, or some magic. Projectiles are usually but not always involved.
  Valid values are *Yes*, *No*, and *Slightly/Special* (e.g. ranged combat
  using thrown environmental objects which are not always present and can't be
  hoarded, or ranged weapons only available in certain circumstances).

### 2D/3D:
- **Does the game features 2D or 3D gameplay?** This is about gameplay, not
  graphics: If the game displays 3D models, but the player can only move within
  and interact with a 2D plane, that's a 2D game.  Valid values are *2* and
  *3*.

### Collectibles:
- **Does the game feature some objects whose purpose is to be sought and
  found?**
- A game which visualizes level-completed by placing some shiny thing
  at the end of each level does not count here; that's just a
  differently-shaped finish line.
- Nor does a game which has health or ammo pickups; those have a use.
- Upgrades do count, if they don't provide anything mandatory, and need to be
  *found* rather than being bought or given as rewards.
- Maybe they're hidden, maybe they're behind a puzzle or you need to be really
  good to get them, but there's lots of them, 
- Valid values are *Yes* and *No*.

### Power-up:
- **Are there things to be found which provide a temporary change in
  gameplay?** You get a thing, it gives you some bonus, but eventually (maybe
  it's timed, maybe it's when you get hurt, maybe it's until-end-of-level) it
  wears off.
- Valid values are *Yes* and *No*.

### Swimming:
- **Does the game feature swimming (or other aquatic traversal mechanics)?**
- Typically, games with swimming either repurpose "jump" as "swim up", or let
  you move in any direction and use "jump" as "swim forward" (or "swim
  faster").
- Games without will either not feature water, feature water as an
  instant-death hazard, or have the player sink to the bottom. In the latter
  case, if the water is not purely cosmetic, this usually means slower
  movement, altered jumps (either higher or lower), and maybe a timer.
- Valid values are *Yes*, *No*, and *Sink* (if it's purely cosmetic, it counts
  as "No", not "Sink").

### Air control:
- **How much can the player steer while in the air?** This is mostly by feel,
  but as rough guidelines: *Strong* indicates that you can fall from above a
  hazard, avoid it, and land directly below it, or that you can jump moving
  forwards, reverse direction, and land behind your starting location. *Weak*
  indicates enough control to aim for a small platform, but not to do the above
  acrobatics without a very long fall. *None* indicates that the trajectory of
  a jump cannot be modified after leaving the ground.

### Airjump:
- **Can you jump while airborne?** Valid values are *Yes*, *No* and
  *Slightly/Special* (indicating that airjumping is available only in limited
  situations).

### Walljump:
- **Can the player jump off of the side of a wall (rather than the ground)?**
  Valid values are *Yes*, *No* and *Slightly/Special* (indicating that
  walljumping is available only in limited situations).

### Leeway for errors:
- **How much room does the game give the player to make mistakes without being
  kicked out?** This was my attempt to partially quantify difficulty, inspired
  initially by [a blog
  post][vigaroe-yoshi] by the
  pseudonymous "Ghoul King", on the idea of separating a *difficult* game from
  a *punishing* one. More on that later.
- Valid values are *Low* (one or zero mistakes), *Moderate* (two or more), and
  *High* (basically infinite, such as games where health regenerates so you're
  fine if you don't rush).

### Multiplayer:
- **Does the main game have multiplayer (not separated as a different game)?**
  Multiplayer minigames separate from the main game don't count; neither do
  "race" or "battle" modes on a distinct set of rules and levels from the main
  game.
- Valid values are *No*, *Co-op*, and *Competitive*, but I didn't find any of
  the latter.

### Story:
- **Does the game have a story, and if so, how much does it matter?** This is
  probably the most subjective field here, because just about every game is
  going to at least have a tiny introductory cutscene or a few paragraphs in
  the manual to provide context.
- *Yes* indicates that the story is a driving force for the game.
- *Cue* indicates that the story doesn't have much impact beyond an
  in-character way to give the player hints at what they need to do next.
- *No* indicates that whatever story might exist isn't particularly worth
  dwelling on, and doesn't even come up often; the fun lies entirely elsewhere.

My data is available [in CSV form](https://github.com/qwertystop/config-d3-fdg/blob/master/data.csv).

## … And Why It Didn't Work
Turns out, nuance is an important thing. *Sure*, it sounds obvious in
retrospect…

Anyway, first thing I did was look for some correlations. Unfortunately, I am
no statistician, and freely admit I don't know how to do that rigorously.
So I took the spreadsheet, color-coded everything, sorted it a few different
ways. Apart from games in a series often appearing to be fairly similar to each
other, nothing jumped out at me. And that much wasn't exactly interesting.

# TODO EMBED SCREENS HERE

I also wrote [a d3 script][cfdg] to take the data and allow it to be grouped and
organized. Again, though, I didn't see many patterns, and what I did find
wasn't very helpful.

Closer examination still wasn't very productive, and further consideration led
me to find reasons why none of my metrics worked out.

So, let's go down the list, shall we?

### Seriality and dimensions

The whole point of establishing a series is that the consumer knows what to expect,
no? As such, it's no surprise that **games in the same series tended to have a
lot in common**. Unfortunately, that doesn't give me very much information. Every
metric was similar across all or almost all of the games in any given series.

One notable standout here was a correlation with the **2D/3D divide**, which
seems almost like a subseries: Games in the same series most often had
differences in metrics when one game was 2D and the other was 3D. This is a
somewhat interesting design choice; 2D and 3D games are capable of presenting
similar experiences, but developers of platformers seem not to want to go in
that direction. This is more true in some cases than others, of course: Compare
Metroid games, which are usually fairly similar in gameplay, to Mario or Sonic,
which have two fairly distinct blocks.

Dotted lines separate 2D from 3D games; solid lines separate series from each
other.

<iframe src="/assets/html/2d-3d-mario-sonic-metroid-table.html" style="width:150%;height:30em"></iframe>

 In each series, we can see that some traits are consistent in a series,
but others are much more common on (or exclusive to) either 2D or 3D games.

- 3D Mario games have at least a little bit of story and more varied layouts,
  mostly avoid ranged combat, and give some form of air-jump (which also provides
  improved air control).
- 3D Metroid games all give the player an air-jump early enough to count as
  "Yes" rather than "Slightly/Special" (though on the other hand, it's much
  more limited than in the 2D games – this is a bit of lost nuance). They're
  quite similar beyond that, though.
- 3D Sonic games have more linear gameplay, often remove jump-combat and water,
  provide an airjump, and have some emphasis on a story.

### Genre savvy? Not so much.

Unfortunately, I didn't have enough games here that could be classified with
subgenres or secondary genres; when I did, they were mostly in the same series,
which would tend to mask whatever commonalities were actually part of the genre.

There is insufficient data for a meaningful result here.

### Plot and player-count: Mainly a side-note.

The presence or absence of a story generally meant little for the rest of the
gameplay: **A story can be applied to, or witheld from, just about any game
that doesn't have its narrative as a major design focus**. Additionally, many
of the games listed here are from a time when technical limitations prevented
there from being enough memory to fit a story into a game at a reasonable
price, and most of the rest are in series that were established during that
time. If narrative was never why people bought the game, it's hard to justify
the expense of hiring writers for the sequel.

There is the one interesting note that 3D Mario and Sonic games tend to include
a story while the 2D ones avoid it, but that doesn't seem to extend to 2D vs.
3D in general.

**Multiplayer, too, has very little impact**, for roughly similar reasons.
It's a tack-on much more often than it's a core part of the game's design.
Most platformers don't have it; when it is present, any influence it might have
on the game design would have to be more abstract than these metrics. Many
platformers that have a cooperative multiplayer mode treat it with a
light-hearted tone, as well: more "friends romping around" than "everybody
working together", with the game as a whole designed more around the
single-player experience. It was not a good decision to include multiplayer in
this project; it's a distraction, not a useful measure.

### Getting the shape of things
The next three had a noticeable – if obvious-in-retrospect – correlation. Using
[the graphing script from before][cfdg], I sorted the games by their layout and
the amount of player choice available, and then tried various color-codings. My
results, with labels and a legend:

![Screenshot of automated grapher](/assets/img/layout-structure-backtrack.png)

The games with **more player choice tended to be of mixed layout**, while both
other categories of choice (and thus, the data as a whole) were
majority-horizontal. Additonally, all open games had backtracking, while very
few other games had it.

This might not be especially surprising, but I suppose it's nice to see my
intuitions confirmed.

### Combat styles
The three different means of combat aren't mutually exclusive, so they took up
three fields in my chart, but practically speaking it only makes sense to
consider them together. When I was assembling the list, I had a few ideas of
what they might indicate – melee combat leading to a sort of heedless-charge,
action-y style; ranged combat for something slow and exploratory, using cover
or hiding; jumping combat for a game that's really just about the platforming,
with enemies used as temporary mobile obstacles or platforms rather than as
something you actively fight.

Two of these predictions were incorrect, and the third was questionable.

My assumptions of pacing differences in melee and ranged combat seem to have
been based on (poor, inaccurate, dim) recollections of specific games: 3D Sonic
games for melee combat, and the Metroid series for ranged combat.

Taking them one at a time, here's footage to illustrate why those assumptions
don't hold. Clips from two melee-combat games, two ranged-combat games, and
one game that features a mix of both combat styles.

# FOOTAGE HERE FROM CASTLEVANIA, SONIC COLORS, METROID FUSION, CONTRA, KIRBY 2
# INCLUDE COMMENTARY POINTING THINGS OUT IN EACH CLIP

To be clear, my point here is not that these games are representative of all
combat-styles, but that the combat style does not make for a reliable predictor
of much else about the game.

The idea I had for jumping combat seems to have been relatively accurate, but
since the time I compiled this dataset, I've heard of at least one game
(*[Downwell][downwell]*) that shows it's not a perfect summary.

# CLIP OF DOWNWELL HERE

It may not have made it on the list, but *Downwell* is a platformer that takes place largely in
freefall: while you do have a gun in addition to the option to stomp enemies,
that gun only shoots down, so you're still lining up jumps (from one head to
the next) as the core of the combat.

Compare that to *Donkey Kong Country: Tropical Freeze*:

# CLIP OF DKCTF HERE

This is very much the sort of game I was thinking of in my earlier analysis;
"enemies" serve mainly as things to jump over or bounce off of, rather than as
something to fight.

### Collectibles COME UP WITH A BETTER TITLE

#### Mastery and challenge
Collectibles, as measured here, are perhaps the worst case of lost nuance in my
dataset. In some games, such as the original *Yoshi's Island* or the *New Super
Mario Bros.* sub-series, finding all the hidden things is a goal in and of
itself. They're all over the place (*Yoshi's Island* has twenty-five; *New
Super Mario Bros.* has three), and finding all of them unlocks even more
levels, the hardest in the game. These games use collectibles as a way for the
player to prove their mastery, and then reward the player with more challenges
to master.

# YOSHI'S ISLAND SCOREBOARD, ADD CAPTION

#### Many small prizes
In others, such as most "Metroidvania" games, collectibles take the form of
small upgrades (usually for health, ammunition, or similar). These games
usually show you a counter or percentage, and might give a special
congratulation at the end for 100% completion, but the main reason to hunt them
down is that they make the game easier (or that you find them while looking for
something else). They're not required, and in fact, players looking for a
challenge are as likely to go for a no-upgrade run as they are to aim for 100%.
In this case, finding them all is about persistence more than anything else,
and the journey is most of the reward, because anyone who's played the game
enough to find all the upgrades is unlikely to actually need them. Still, the
fact that each one provides some tangible benefit can get players to look – or,
at least, to enjoy incidental finds – when the journey isn't enough on its own.

# SCREEN ILLUSTRATING SUPER METROID OR SOTN COLLECTIBLES

#### Standing alone, for better or for worse
Still other games put collectibles front-and-center; this is a defining trait
of "collectathons", which were a major subgenre of early 3D platformers that
haven't gone away completely. In this case, finding all the hidden things is
the entire point; the nominal "goal" of the game as described by whatever plot
there is (usually minimal) is reached long before finding everything, and the
miscellaneous shinies you're hunting down are as likely to be on the other side
of a tricky gauntlet of difficult jumps as they are to be under a random bush
five feet behind your starting location. There may be rewards given at various
increments – usually unlocking new areas to explore – but these will eventually
run dry. The journey is the destination again, but this time without much
pretense of any other reason to search, so those players who aren't motivated
by completionism are unlikely to stay interested for long.

# SCREEN SHOWING COLLECTIBLE COUNT FOR A COLLECTATHON

### Swimming and power-ups COME UP WITH A BETTER TITLE

### Air control, airjumps, walljumps BETTER TITLE

### How to measure difficulty? BETTER TITLE

## Pushing the boundaries BETTER TITLE, ALSO THIS IS A NEW SECTION

[vigaroe-yoshi]: http://www.vigaroe.com/2017/05/difficulty-yoshis-island.html
    "Difficulty, Yoshi's Island"
[cfdg]: https://qwertystop.github.io/config-d3-fdg/
    "Configurable force-directed graph"
[downwell]: https://www.devolverdigital.com/games/view/downwell
    "Publisher's official page for Downwell"
