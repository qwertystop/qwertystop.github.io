---
layout: default
title: "An Analysis of Platform Games, Part 2"
slug: platformers-beyond-data
category: analysis
tags: games
---

In my [previous post](/analysis/platformers-by-data), I went into
detail on my attempt to quantify the design of platformers at a broad level for
analysis. This time, the results, and moving on from them. Last time was **The
Data-Driven Analysis of Platformers**, and now we have:

## And Why It Didn't Work
Turns out, nuance is an important thing. *Sure*, it sounds obvious in
retrospect...

Anyway, first thing I did was look for some correlations. Unfortunately, I am
no statistician, and freely admit I don't know how to do that rigorously.
So I took the spreadsheet, color-coded everything, sorted it a few different
ways. Apart from games in a series often appearing to be fairly similar to each
other, nothing jumped out at me. And that much wasn't exactly interesting.

I also wrote [a d3 script][cfdg] to take the data and allow it to be grouped and
organized. Again, though, I didn't see many patterns, and what I did find
was mostly unhelpful.

As such, instead of directly presenting patterns from the data, I'm doing my
best to salvage things: For each category, I've gone into detail on what nuance
was lost by my too-rough analysis, and what patterns I can see through close
examination, even if I can't quantify them.

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

- 3D *Mario* games have at least a little bit of story and more varied layouts,
  mostly avoid ranged combat, and give some form of air-jump (which also
  provides improved air control).
- 3D *Metroid* games all give the player an air-jump early enough to count as
  "Yes" rather than "Slightly/Special" (though on the other hand, it's much
  more limited than in the 2D games – this is a more granular than my
  data-collecting supported). They're quite similar beyond that, though.
- 3D *Sonic* games have more linear gameplay, often remove jump-combat and
  water, provide an airjump, and have some emphasis on a story.

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

There is the one interesting note that 3D *Mario* and *Sonic* games tend to
include a story while the 2D ones avoid it, but that doesn't seem to extend to
2D vs. 3D in general.

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

**The games with more player choice tended to be of mixed layout**, while both
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
combat-styles, but that **the combat style does not make for a reliable predictor
of much else about a game**.

The idea I had for jumping combat seems to have been relatively accurate, but
since the time I compiled this dataset, I've heard of at least one game
(*[Downwell][downwell]*) that shows it's not a perfect summary.

# CLIP OF DOWNWELL HERE

It may not have made it on the list, but *Downwell* is a platformer that takes
place largely in freefall: while you do have a gun in addition to the option to
stomp enemies, that gun only shoots down, so you're still lining up jumps (from
one head to the next) as the core of the combat.

Compare that to *Donkey Kong Country: Tropical Freeze*:

# CLIP OF DKCTF HERE

This is very much the sort of game I was thinking of in my earlier analysis:
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

### Three approaches to the power-up

Power-ups were another badly-defined grouping. In some cases – *Mario* and
*Sonic* come to mind for their high variety – power-ups are a way to make the
game temporarily easier, until you mess up. A few seconds of invincibility
([traditionally][sonic-invuln] [with][mario-invuln] [music][kirby-invuln]), is
a common one across a variety of games. *Sonic* games often provide [shields
with side-effects](http://sonic.wikia.com/wiki/Item_Box#List_of_power-ups),
*Mario* games tend more towards costumes (that look like [miscellaneous
objects](https://www.mariowiki.com/List_of_power-ups) until used). In both
of these cases, and some others, power-ups are treated by the game design as a
prize, and a bit of relief: Find them, and things get a bit easier for a while.

On the other hand, *Kirby* games (for example) treat power-ups more like
equipment. They're not required, but they're not hidden prizes, either: You can
find them all over the place, there's a wide variety of powers, and you only
rarely need to have any specific one (usually for optional challenges, where
the challenge is "how do I get to this place without losing this power" rather
than having to do anything particularly tricky when you get there). The games
tend to be built around the assumption that you've got something, without
caring about what it is. Another game that demonstrates this pattern (though
they're not as heavily emphasized there) is *Castlevania: Symphony of the
Night* (specifically, the
[sub-weapons](http://castlevania.wikia.com/wiki/Symphony_of_the_Night_Inventory#Sub-Weapons)).
In both cases, powers aren't required, and they aren't (usually) a prize;
they're just one more thing to mess around with.

In yet a third group, some games will shove a power-up at you at the start of a
section, which provides a major change in the gameplay while it lasts. You
can't beat the level without that boost, and it won't be given where it isn't
necessary. One example of this is the Feather in *Celeste*:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/GJA504P2i9w?rel=0&amp;start=550" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

The Feather gives Madeline (the redhead) the ability to fly for a few seconds.
Most of the areas with a Feather in that game require her to fly efficiently
around obstacles from each Feather to the next, before running out of time and
falling. This also appears in some levels of *Yoshi's Island*, which turn Yoshi
into various vehicles at the starting-point of a section, and teleport him back
there if he can't reach the end before a time limit. For example, the third
"Secret" level in the GBA remake is focused entirely on such transformations.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/YjUJ7AeG1jk?rel=0&amp;start=79" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Submerged diversions

Swimming is generally treated by most platformers as something similar to the
third kind of power-up: A section of the game that plays differently from the
rest. Where water is present in a game, and not treated as an instant-death
hazard, there's two common ways of handling it (and one less-common), plus one
optional addendum.

First, and most-common in my experience, is the **free-swimming** approach. You
go in the water, and you can swim around as you like. Some games do
this by slowing movement and replacing "jump" with "swim up a little", leaving
the controls otherwise unmodified; other games let you swim in any
direction using the usual direction controls, with "jump" becoming "swim a
little faster". The former approach is more common in 2D, and the latter in 3D.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/mCHgirqdiHc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/IuCO9GC9_ZM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Second is **sinking**. In this case, water reduces movement speed and (usually)
increases jump height, but the character can't swim, and instead just sinks to
the bottom.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Y7ABdzKLkwY?rel=0&amp;start=124" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Either of these are sometimes, but not always, combined with a drowning risk –
if you stay underwater for too long in one go, game over. Usually, there's
air bubbles or something to extend the time limit; some games will technically
have a time limit but rarely have a water section long enough for it to matter.

Finally, and rarest, is **floating**. The character floats on the surface of
the water, and can't swim under. This is presumably rare because of how little
it offers in gameplay, relative to simply having solid ground. Most often, this
combines with either limits on what can be done while floating (e.g. no
carrying objects, or no attacks), or involves the use of momentum to dive for a
short time before floating back up (find somewhere high to fall from so that
you can get through an underwater passage). This appears near the start of the
Yoshi's Island video in the previous section (rewind to before where it loads).
I couldn't find a better clip – as I said, this is rare.

### Air control, airjumps, walljumps BETTER TITLE

### How to measure difficulty? BETTER TITLE

## Pushing the boundaries BETTER TITLE, ALSO THIS IS A NEW SECTION

[vigaroe-yoshi]: http://www.vigaroe.com/2017/05/difficulty-yoshis-island.html
    "Difficulty, Yoshi's Island"
[cfdg]: https://qwertystop.github.io/config-d3-fdg/
    "Configurable force-directed graph"
[downwell]: https://www.devolverdigital.com/games/view/downwell
    "Publisher's official page for Downwell"
[sonic-invuln]: https://youtu.be/BbzjOKqaQPY?t=11s
[mario-invuln]: https://youtu.be/HKYVwSOe4Qo
[kirby-invuln]: https://yout.be/neE5SgVjfDs
