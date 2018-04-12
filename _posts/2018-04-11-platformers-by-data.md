---
layout: default
title: "An Analysis of Platform Games, Part 1"
slug: platformers-by-data
category: analysis
tags: games
---

## Some context
This piece (and its [follow-up][pt2]) were
originally written as a class project; I've decided to present my results in
hypertext because I need to include images and video. Also, the blog-post
format allows for a slightly nicer tone than a formal paper.

The class, as a whole, was about the concept of originality, and the varied
ways in which creative works can draw on earlier, preexisting works. The
project could be basically anything, as long as I was able to plausibly claim relevancy.

## The Data-Driven Approach

At first, the most interesting topic I could think of was to perform a
data-driven analysis of… something. I decided fairly quickly that games –
specifically, [platformers](https://en.wikipedia.org/wiki/Platform_game) –
would be a good group to work with: something I had a decent amount of
experience with, and constrained enough in gameplay that I could come up with a
slew of questions to ask about any given game without needing to put `N/A` too
many times. Additionally, the genre is old as such things go (and still fairly
popular) which gives a nice, wide variety of titles to pick from. This also
allows me to include and several very long-running series, and thus explore
any design patterns that might show up in them.

In the end, I settled on twenty different fields. Each is named below, along
with its defining question and any elaboration that felt necessary.

### Series:
- **What series is the game in?**
    - My process was to keep adding games as they occurred to me until I ran
      out of time, and seriality wasn't the only thing I was trying to cover.
      As such, there are games with no series here, as well as series where I
      didn't include all of the games.

### Subgenre:
- **Does the game fit into any smaller category within "platformers"?**
    - These are unavoidably subjective; I came up with four.
    - *Action* refers to a platformer where the actual platforms are more often
      a setting for combat than an agility or navigation challenge. Combat is
      generally some mix of easily-dispatched enemies and significant boss
      fights, with few or none in a middle-ground.
    - *Challenge* platformers, in contrast, have little or no combat and a very
      strong focus on difficult movement-based challenges, each challenge
      usually being fairly small and contained. High precision and low reaction
      times are a must.
    - *Collectathon* is... slightly negative, as a term, I'll be honest. These
      games are about hunting through a large world for hidden things. New
      content is gated behind semi-arbitrary counts of how many such things
      you've already found. Usually, there's several types of things to
      collect, and the things you're finding are more often scattered or
      hidden, rather than being placed explicitly as the targets of distinct
      levels or challenges.
    - *Metroidvania* is, contrary to how it sounds, a fairly widespread name
      for the category. These are games where the player explores an
      interconnected world, continually gaining new abilities and/or learning
      skills and mechanics that allow them to access an ever-increasing portion
      of that world.

### Secondary genre:
- **Does the game fit into any genres besides "platformer"?**
    - The only genre I found among the games I included was *RPG*, short for
      "role-playing game" and referring to games with some form of progression
      of capabilities for the player-character, as well as (usually) a
      significant narrative aspect.

### Year of release:
- **What year was the game initially released in?**
    - Remakes don't count, and in cases where the game was released to
      different markets at different times, I used the earliest. This doesn't
      completely pin down the environment at the time of development, since
      games might take more or less time to make, but still gives enough
      context for the potential of some sort of progression.

### Primarily vertical or horizontal:
- **In what direction does the player traverse the world?**
    - Valid values are *Horizontal*, *Vertical*, and *Mixed*.

### Backtracking:
- **Is the player often required to cross the same areas multiple times?**
    - Valid values are *Yes* and *No*.

### Physical structure:
- **Does the player commonly have multiple valid routes by which to progress?**
    - Valid values are *Open* (indicating many choices), *Linear* (indicating
      no choices), and *Mixed* (indicating long alternating periods of one or
      the other).
    - If there's only one correct route but also one or more incorrect routes
      (dead-ends, optional areas, places to return to later), and exploration
      is required to know which is which, that counts as multiple routes.

### Jump combat:
- **Is the standard "jumping" action also used to dispatch enemies?**
    - This is distinct from an action with the primary purpose of attacking,
      which incidentally causes vertical movement.  Valid values are *Yes* and
      *No*.

### Melee combat:
- **Is there an action dedicated to attacking enemies near the player
  character?**
    - For example, a sword-swing, punch, or a projectile with extremely limited
      range. This does not require that the game visually displays some form of
      physical contact, only that the attack has a small maximum reach.  Valid
      values are *Yes* and *No*.

### Ranged combat:
- **Can enemies be fought at a significant distance?**
    - For example, guns, archery, or some magic. Projectiles are usually but
      not always involved.  Valid values are *Yes*, *No*, and
      *Slightly/Special* (e.g. ranged combat using thrown environmental objects
      which are not always present and can't be hoarded, or ranged weapons only
      available in certain circumstances).

### 2D/3D:
- **Does the game features 2D or 3D gameplay?**
    - This is about gameplay, not graphics: If the game displays 3D models, but
      the player can only move within and interact with a 2D plane, that's a 2D
      game.  Valid values are *2* and *3*.

### Collectibles:
- **Does the game feature some objects whose purpose is to be sought and
  found?**
    - A game which visualizes level-completed by placing some shiny thing
      at the end of each level does not count here; that's just a
      differently-shaped finish line. Nor does a game which has health or ammo
      pickups; those have a use.
    - Upgrades do count, if they don't provide anything mandatory, and need to be
      *found* rather than being bought or given as rewards.
    - Maybe they're hidden, maybe they're behind a puzzle or you need to be really
      good to get them, but there's lots of them.
    - Valid values are *Yes* and *No*.

### Power-up:
- **Are there things to be found which provide a temporary change in
  gameplay?**
    - You get a thing, it gives you some bonus, but eventually (maybe it's
      timed, maybe it's when you get hurt, maybe it's until-end-of-level) it
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
- **How much can the player steer while in the air?**
    - This is mostly by feel, but as rough guidelines: *Strong* indicates that
      you can fall from above a hazard, avoid it, and land directly below it,
      or that you can jump moving forwards, reverse direction, and land behind
      your starting location. *Weak* indicates enough control to aim for a
      small platform, but not to do the above acrobatics without a very long
      fall. *None* indicates that the trajectory of a jump cannot be modified
      after leaving the ground.

### Airjump:
- **Can you jump while airborne?**
    - Valid values are *Yes*, *No* and *Slightly/Special* (indicating that
      airjumping is available only in limited situations).

### Walljump:
- **Can the player jump off of the side of a wall (rather than the ground)?**
    - Valid values are *Yes*, *No* and *Slightly/Special* (indicating that
      walljumping is available only in limited situations).

### Leeway for errors:
- **How much room does the game give the player to make mistakes without being
  kicked out?**
    - This was my attempt to partially quantify difficulty, inspired initially
      by [a blog
      post][http://www.vigaroe.com/2017/05/difficulty-yoshis-island.html] by
      the pseudonymous "Ghoul King", on the idea of separating a *difficult*
      game from a *punishing* one. More on that later.
    - Valid values are *Low* (one or zero mistakes), *Moderate* (two or more),
      and *High* (basically infinite, such as games where health regenerates so
      you're fine if you don't rush).

### Multiplayer:
- **Does the main game have multiplayer (not separated as a different game)?**
    - Multiplayer minigames separate from the main game don't count; neither do
      "race" or "battle" modes on a distinct set of rules and levels from the
      main game.
    - Valid values are *No*, *Co-op*, and *Competitive*, but I didn't find any
      of the latter.

### Story:
- **Does the game have a story, and if so, how much does it matter?**
    - This is probably the most subjective field here, because just about every
      game is going to at least have a tiny introductory cutscene or a few
      paragraphs in the manual to provide context.
    - *Yes* indicates that the story is a driving force for the game.
    - *Cue* indicates that the story doesn't have much impact beyond an
      in-character way to give the player hints at what they need to do next.
    - *No* indicates that whatever story might exist isn't particularly worth
      dwelling on, and doesn't even come up often; the fun lies entirely elsewhere.

My data is available [in CSV form](https://github.com/qwertystop/config-d3-fdg/blob/master/data.csv).

## Now what?

Well, this was all how I started my analysis. In [part two][pt2], I move on to
how I finished my analysis, and what I did afterwards. Join me next time for
**And Why it Didn't Work**!

[pt2]: /analysis/platformers-beyond-data
