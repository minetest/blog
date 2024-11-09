---
layout: post
title: "September - This Month in Minetest (08)"
contributors:
  - MisterE
  - rubenwardy
  - Peppermint Patty
  - Warr1024
  - BuckarooBanzai
  - wsor
  - x2048
description: >
  This month, TurkeyMcMac joined the core dev team, post-processing and bloom were
  merged, and Android crosshair support was added. Minefall released on ContentDB,
  BlockExchange got a graphical rework, and more!
image: /static/blog/2022_September/castleprop.jpg
forum_topic: https://forum.minetest.net/viewtopic.php?f=18&t=28773
tags:
  - last_month
wsortrains:
  - src: /static/blog/2022_September/trains1.png
    caption: a pair of sw1500's tie down at the station as the morning sun rises, by Wsor

  - src: /static/blog/2022_September/trains2.png
    caption: a pair of sw1500's tie down at the station as the morning sun rises, by Wsor
---

This month, TurkeyMcMac joined the core dev team, post-processing and bloom were
merged, and Android crosshair support was added. Minefall released on ContentDB,
BlockExchange got a graphical rework, and more!

<!-- more -->

- [Engine News](#engine-news)
- [Games News](#games-news)
- [Mods News](#mods-news)
- [Textures](#textures)
- [Art and Builds](#art-and-builds)
- [Server News](#server-news)
- [In Other News](#in-other-news)


## Engine News

TurkeyMcMac was added as a core developer this month. He has been
[contributing](https://github.com/minetest/minetest/commits/?author=TurkeyMcMac)
to Minetest for a while and has demonstrated a high level of technical ability.

x2048's post-processing Pull Request was merged, as well as a work-in-progress
version of a bloom shader. Post-processing is a technique implemented as part of
the graphics modernization project, and will result in improved performance for
tone mapping. It also allows new graphical effects to be implemented in the
future, including depth-of-field and volumetric lighting (god rays).

 For now, bloom is a client-side setting only, but mods will be able to control
it in the future too. Bloom lets light bleed into dark areas and creates a glow
around bright objects. You can try out the bloom shader by building Minetest
from source, enabling shaders, and then entering `All Settings`. Search for
bloom, enable it, and experiment with the other two bloom settings, `bloom
intensity` and `bloom radius`. More shaders will be coming soon!

Crosshair support for android has been merged. Unlike desktop, Android defaults
to punching/placing/digging where you tap. With this new feature, users can
enable the crosshair to have an experience closer to desktop.

Desour is working on a
[refactor of Minetest's sound system](https://github.com/minetest/minetest/pull/12764).
It will make sounds load faster, add a doppler effect, and fix many sound bugs -
such as fading not working on positional sounds and sounds not pausing during
the pause menu.

## Games News

### Nodecore

[Nodecore](https://content.luanti.org/packages/Warr1024/nodecore/) received a
significant performance update. Warr1024 found that
[TurkeyMcMac's LuaJIT Profiler](https://forum.minetest.net/viewtopic.php?t=28135)
was particularly useful in finding the cause of performance issues - much more
useful than the built-in profiler. That helped him discover functions that were
more expensive than expected, such as `minetest.check_player_privs()`.

### Cave Game

{% include figure.html src="/static/blog/2022_September/cave_game.png"
    caption="Cave Game" %}

[Olive](https://content.luanti.org/users/GoodClover/) made
[Cave Game](https://content.luanti.org/packages/GoodClover/cavegame/), a
recreation of Notch's first implementation of Minecraft. It has Stone and Grass.
Yeah, that's about it.

### Minefall

[Minefall](https://content.luanti.org/packages/Astrobe/minefall/) was released
on ContentDB. It is a new take on the Minetest Game concept. Its main feature is
the ability of players to levitate if they have enough stamina. Also, it has
hostile mobs and flying whales.

## Mods News

### BlockExchange

[BuckarooBanzai](https://content.luanti.org/users/BuckarooBanzay/) rewrote
most of the frontend part of the
[BlockExchange project](https://content.luanti.org/packages/BuckarooBanzay/blockexchange/) -
it should now be fairly usable/stable.
Also, it has moved to a new home/address: https://blockexchange.minetest.ch/
instead of the .land domain).

### Mese Trains

{% include figure.html src="/static/blog/2022_September/mesejet_train.png"
    caption="MeseJets in a Railyard" %}

[Xenon](ttps://content.luanti.org/users/xenonca/) released the first version
of another Advanced Trains expansion pack. So far it only includes the MeseJet,
a bullet train that has color-coded line numbers displayed on its side.

### TNT Tag

[debiankaios](https://content.luanti.org/users/debiankaios/) released
[TNTtag](https://content.luanti.org/packages/debiankaios/tnttag/). Don't get tagged with TNT, and if you do get tagged, be sure to tag someone else before
the time runs out and the TNT on your head explodes!

## Textures

### OhCeeDee Texture Pack

{% include figure.html src="/static/blog/2022_September/ocd.png"
    caption="The OCD texture pack" %}

[ROllerozxa](https://content.luanti.org/users/ROllerozxa/) released the
[OhCeeDee texture pack](https://content.luanti.org/packages/ROllerozxa/ohceedee/),
inspired by FVDisco's oCd Minecraft resource pack.

## Art and Builds

{% include figure.html src="/static/blog/2022_September/temple_peppermint_patty.png"
    caption="Temple by Peppermint Patty" %}

{% include figure.html src="/static/blog/2022_September/super_sam.png"
    caption="Banner for the Super Sam game, art by Temhotaokeaha" %}

{% include figure_gallery.html items=page.wsortrains %}

{% include figure.html src="/static/blog/2022_September/castleprop.jpg"
    caption="One of x2048's props for testing lighting effects" %}

## Server News

### Nodecore Community Server
<sub>nodecore.mine.nu:30000</sub>

Nodecore was updated with the performance updates in the games section above.
That makes the performance of the Nodecore Community Server better than ever.

### A.E.S. Minigames
<sub>minetest.eticadigitale.org:30010</sub>

A.E.S. has a new beta minigame: Tnttag! There are also two new skins for you to
find and unlock by completing parkours.

The November Block League tournament is coming up! BlockLeague is a shooter
minigame that is best described as "Soccer with guns". It now has passive
skills and a menu for choosing them. Check out the pads to the side of the
Blockleague island to choose your skill. There will be up to 8 teams of 3
players each for the tournament. See the details
[here](https://forum.minetest.net/viewtopic.php?p=415626#p415626) for how to
sign up.

## In Other News

### Mindustry3d

GeneralBaker began a project to recreate Mindustry in 3d in Minetest. The first
stable release is still a long way off, but the project is looking for
contributors. Check it out here:
[Forum](https://forum.minetest.net/viewtopic.php?f=49&t=28685) and
[Git](https://gitlab.com/ReallyBasicGames/mindustry_3d)

### Blog Content

This is our 8th Minetest monthly update. So far, content for the blog has mostly
been collected on an ad-hoc basis - the blog editors see something interesting
and put it in the blog. We have had a few content creators approach editors
about the blog, but we'd like to see more people suggest content using the
[issue tracker](https://github.com/minetest/blog/issues)
([GitLab Mirror](https://gitlab.com/minetest/blog/-/issues)).
It prevents us from missing or forgetting about something.
Thank you to those who have used the issue tracker.
