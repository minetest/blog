---
layout: post
title: "May, June, and July in Minetest (14)"
authors: [MisterE]
editors: [GreenXenith]
contributors:
  - Rubenwardy
  - EmptyStar
  - Athozus
  - Lemente
  - CodeScratcher
description: >
  Work on the 5.8 release continues with some exciting new engine improvements, a classic game makes its way to
  ContentDB, and the use of Minetest in education was explored.
#forum_topic: https://forum.luanti.org/viewtopic.php?f=18&t=29501
tags:
  - last_month
image: /static/blog/2023_MayJune/header.png
asuna:
- src: /static/blog/2023_MayJune/asuna1.png
  caption: Crystal Forest
- src: /static/blog/2023_MayJune/asuna2.png
  caption: Cursed Lands Under
---

Work on the 5.8 release continues with some exciting new engine improvements, a
classic game makes its way to ContentDB, and the use of Minetest in education
was explored.

<!-- more -->

- [Engine News](#engine-news)
- [Games News](#games-news)
- [Mods News](#mods-news)
- [Art and Builds](#art-and-builds)
- [Education](#education)
- [Server News](#server-news)
- [In Other News](#in-other-news)

## Engine News

Several improvements have been in the works for Minetest 5.8. On touchscreens, it will be possible to [place nodes with
a single tap](https://github.com/minetest/minetest/commit/fc3d6c1dd9ae754e863e1d9386984a314acf1386). [New texture
modifiers have been added](https://github.com/minetest/minetest/commit/8cd129604934077f900ec587d8230fd640822934),
allowing developers to adjust texture hue, saturation and lightness, change contrast, create textures of arbitrary size,
and more.

[Rubenwardy's settings page
redesign](https://github.com/minetest/minetest/commit/d35672e78e904cbc4312637409fd6a3242e74bac) has been merged, marking
an important step towards a better user interface.

{% include figure.html src="/static/blog/2023_MayJune/settings.png" caption="The new settings menu" %}

Another major improvment is [Desour's sound
refactor](https://github.com/minetest/minetest/commit/edcbfa31c9eb636edca2ed8b10eace8e003a0a08) which fixes several bugs
(such as lag from loading large audio files) and adds many new features such as fade-in for positional audio.

Finally, [x2048 added antialiasing post-processing
filters](https://github.com/minetest/minetest/commit/c09a3a52acaffbcb389ea6d7005916f59f73f1db) for smoother graphics.

## Games News

### Asuna

{% include figure_gallery.html items=page.asuna %}

[Asuna](https://content.luanti.org/packages/EmptyStar/asuna/) by
[EmptyStar](https://content.luanti.org/users/EmptyStar/) welcomes the otherworldly wonders of the
[Everness](https://content.luanti.org/packages/SaKeL/everness/) mod to its domain! From the sparkling vistas of the
crystal forests to the haunted bogs of the cursed lands, down to the depths of its lush caves, icy caverns, and beyond—
Everness is now a crown jewel of the Asuna experience. With a few personal touches and careful integration into Asuna's
fantastic fabric of biomes, Everness graces every corner of the world.

Along with the inclusion of Everness, much work has been done to improve Asuna's underground, new biomes have been
added, and landscapes are now more diverse than ever. Join the new [Asuna Discord server](https://discord.gg/DqtD9kuk2R)
to stay up-to-date with Asuna's development.

### BlockColor

{% include figure.html src="/static/blog/2023_MayJune/blockcolor.png" caption="Blocks and colors" %}

In an effort to preserve an old, interesting game project, the [mt-historical](https://github.com/mt-historical)
organization has added [BlockColor by MrChiantos](https://content.luanti.org/packages/mt-mods/blockcolor/) to
ContentDB. The name says it all: It's a world of blocks painted with a soothing palette of colors.

### Mineclone 2

The latest [Mineclone](https://content.luanti.org/packages/Wuzzy/mineclone2/) update, ["The Very Nice
Release"](https://git.minetest.land/MineClone2/MineClone2/releases/tag/0.84.0), went live last month. It is mostly a
quality-of-life update with bugfixes, performance, texture, and audio improvements.

{% include youtube.html id="5aHym2jUB1M" %}

## Mods News

### Mail

{% include figure.html src="/static/blog/2023_MayJune/mailmod.png" caption="New Mail Features" %}

Many servers rely on the [Mail mod](https://content.luanti.org/packages/mt-mods/mail/) for in-game communication.
Since the beginning of the year, the [mt-mods](https://github.com/mt-mods) organization has developed many new features
and fixed several bugs using feedback from the [YourLand server](https://your-land.de/). They also added translations
for at least 6 new languages. The biggest new addition is the "Sent Messages" folder, which required a complete rewrite
of the storage system (by BuckarooBanzay).

Other new features include mailing lists, sorters and filters, drafts, multiple-message selection, and a new "About"
page.

Most recently, the [1.2.0 release](https://github.com/mt-mods/mail/releases/tag/1.2.0) has brought settings, a trash
system, major performance improvements, and bug fixes.

Contributors to the mail mod include Athozus, S-S-X, BuckarooBanzay, fluxionary, and the YourLand server.

### Plushie Invasion

{% include figure.html src="/static/blog/2023_MayJune/plushies.png" caption="Fluffy creatures and characters" %}

You may have noticed a recent rise in plushie content for Minetest. Three new mods— [Fumo
Plushies](https://content.luanti.org/packages/aSliceOfCake/fumoplushies/), and [Amogus
Plushie](https://content.luanti.org/packages/aSliceOfCake/amogus/) by
[aSliceOfCake](https://content.luanti.org/users/aSliceOfCake/), and
[Plushies](https://content.luanti.org/packages/Atlante/cat_plushies/) by
[Atlante](https://content.luanti.org/users/Atlante/)— introduce a plethora of fluffy decorations.

### Nodecore Cat Realm

{% include figure.html src="/static/blog/2023_MayJune/nc_catrealm.jpg" caption="Cat Kingdom" %}

The [Nodecore CatRealm modpack](https://content.luanti.org/packages/Warr1024/catrealm/) by
[Warr1024](https://content.luanti.org/users/Warr1024/) and Mearson introduces a new
[NodeCore](https://content.luanti.org/packages/Warr1024/nodecore/) dimension inhabited by cats. Craft a portal, pay a
cat a prill, and step out onto the mythical cat sky islands. Find new ores and craft powerful tools. Conquer the land of
the cats!

### Arena_lib

{% include figure.html src="/static/blog/2023_MayJune/weather.png" caption="Rain in the Arena" %}

Development on [Arena_lib](https://content.luanti.org/packages/Zughy/arena_lib/) by
[Zughy](https://content.luanti.org/users/Zughy/) is nearing completion. With the latest update [(6.3.0,
"Piove?")](https://gitlab.com/zughy-friends-minetest/arena_lib/-/releases/6.3.0) you can choose from rain, snow, or dust
weather effects to stylize your minigame arena. You can also change the saturation of the screen inside a minigame to
mute colors or create a black-and-white effect.

## Art and Builds

{% include figure.html src="/static/blog/2023_MayJune/bamboocave.png" caption='"Bamboo Cave with Pool" by Heather' %}

{% include figure.html src="/static/blog/2023_MayJune/carved_land.png" caption='"Carved Landscape from Mapgen with
Rivers" by Lemente' %}

## Education

### Minestory

{% include figure.html src="/static/blog/2023_MayJune/minestory.png" caption="Students creating Lascaux-inspired cave
    paintings in Minetest during Minestory" %}

Every year, hundreds of students from schools across France participate in
[Minestory](http://minetest.wp.ac-dijon.fr/minestory-frise-immersive-de-sites-du-patrimoine-architectural/), an event
created by French teacher Julien Crémoux in 2019. Students are tasked to replicate a heritage site from their local area
such as Notre-Dame or the Louvre castle on a Minetest server, and then give a virtual tour of their creation.

This year's Minestory event was hosted in Terrasson-Lavilledieu in France on May 31st, 2023. 150 of the 413 participants
visited the nearby [Lascaux cave](https://en.wikipedia.org/wiki/Lascaux), which is known for its prehistoric cave
paintings. Thomate, Riwad and Lemente were present to discuss the future possibilities of Minetest as an educational
ecosystem and how to facilitate its adoption by educators. The next day, they organised a 10-minute workshop (one of 14
other workshops) in which students decorated a Minetest cave with recreations of paintings they saw previously using the
[ggraffiti](https://content.luanti.org/packages/grorp/ggraffiti/) and
[cave_painting](https://github.com/Lemente/cave_painting) mods.

## Server News

### Open Survival
<sub>minetest.skiscratcher.com:30000</sub>

{% include figure.html src="/static/blog/2023_MayJune/opensurvival.png" caption="A Fresh Start" %}

On June 14, 2023, Open Survival had a total reset. To remedy increasing management complexity and provide a new
experience for long-time players, the Open Survival team removed several mods and completely reset the world and the
players.

## In Other News

Better late than never, right?
