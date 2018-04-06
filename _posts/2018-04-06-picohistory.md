---
layout: default
title: Picohistory
date: 2018-04-06
category: gamedev
tags: picohistory
---

## Classic games, remade on the PICO-8

The idea here was to take a few old games and rebuild them, with modifications,
for the [PICO-8 fantasy console](https://www.lexaloffle.com/pico-8.php).
I ended up with four; they're linked below.

If you have any critique after playing, please feel free to submit it
at [this form](https://goo.gl/forms/S9iV9UQGe6da58Bv2).

<ul>
 {% for post in site.tags.picohistory %}
  {% unless post.title == "Picohistory" %}
    <li>
     <a href="{{ post.url | absolute_url }}">{{ post.title }}</a>
    </li>
  {% endunless %}
 {% endfor %}
</ul>

This was an interesting project;
I didn't run into the PICO-8's limitations as much as I expected.
On the other hand, working in Lua,
and building most of several games from the ground up, was quite educational.
The results are more entertaining than I expected of such old things, too.


I did use a chunk of engine code from [Under Construction (by Glip and Eevee)]("https://eev.ee/release/2016/05/25/under-construction-our-pico-8-game/")
in Pong, but the later ones stripped out most of it in favor of something I understood better
by way of building it myself. I think that was the right choice for rapid development,
but none of the stuff I built really lends itself to a re-usable engine, so who knows.
