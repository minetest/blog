---
layout: post
title: "September - This Month in Minetest (08)"
contributors:
  - MisterE
  - Rubenwardy
  - Peppermint Patty
  - Warr1024
  - BuckarooBanzai
  - Wsor
  - x2048
description: >
  This month, we get a new Core Dev, Post Processing comes to minetest, the bloom shader gets added, Minefall is released on Content Database, BlockExchange gets a graphical rework, there is a new texturepack, and more!
image: /static/blog/2022_September/temple_peppermint_patty.png
# forum_topic:
tags:
  - this_month
wsortrains:
  - src: /static/blog/2022_September/trains1.png
    caption: a pair of sw1500's tie down at the station as the morning sun rises, by Wsor

  - src: /static/blog/2022_September/trains2.png
    caption: a pair of sw1500's tie down at the station as the morning sun rises, by Wsor
---

  This month, we get a new Core Dev, Post Processing comes to minetest, the
  bloom shader gets added, Minefall is released on Content Database,
  BlockExchange gets a graphical rework, there is a new texturepack, and more!

<!-- more -->

*  [Engine](#engine-news)
*  [Games](#games-news)
*  [Mods](#mods)
*  [Textures](#textures)
*  [Art/Builds](#art)
*  [Server News](#s-news)
*  [In Other News](#o-news)


## Engine News

jwmhjwmh, aka TurkeyMcMac, was added as a core developer this month. He has been
contrtibuting to Minetest for a while and has demonstrated a high level of
technical ability.

x2048's Postprocessing Pull Request was merged, as well as a draft version of a
bloom shader. For now, bloom is client-side only — mod control will come soon.
Bloom lets light bleed into dark areas and creates a glow around bright objects.
You can try out the bloom shader by building minetest from source, enabling
shaders, and then entering `All Settings`. Search for bloom, enable it, and
experiment with the other two bloom settings, `bloom intensity` and `bloom
radius`. More shaders will be forthcoming!

Crosshair support for android has been merged. It was often difficult to
determine where one was pointing on android devices. There was even a mod that
added a crosshair to android. It is finally part of the default android
experience.

Desour is working on a [refactor of minetest's sound system](https://github.com/minetest/minetest/pull/12764). It will make sounds load faster, add a doppler effect, and fix many sound bugs such as fading not working on positional sounds and sounds not 
pausing during the pause menu.

## Games News

### Nodecore

[Nodecore](https://content.minetest.net/packages/Warr1024/nodecore/) recieved a significant performance update. Warr1024 found that [TurkeyMcMac's LuaJIT Profiler](https://forum.minetest.net/viewtopic.php?t=28135) was particularly
useful in finding the cause of performance issues — much more useful than the
built-in profiler. That helped him locate functions that were being called each
globalstep that were more expensive than is ideal, such as
`minetest.check_player_privs()`. 


### Cave Game

{% include figure.html src="/static/blog/2022_September/cave_game.png"
    caption="Cave Game" %}

[Olive](https://content.minetest.net/users/GoodClover/) made [Cave Game](https://content.minetest.net/packages/GoodClover/cavegame/), a recreation of Notch's first implementation of Minecraft. It has Stone and Grass. Yeah, that's about it. 

### Minefall

[Minefall](https://content.minetest.net/packages/Astrobe/minefall/) was released
on content database. It is a new take on the Minetest-Game concept. Its main
feature is the ability of players to levitate if they have enough stamina. Also,
it has hostile mobs and flying whales.

## Mods News

### BlockExchange

[BuckarooBanzai](https://content.minetest.net/users/BuckarooBanzay/) rewrote most of the frontend part of the [blockexchange project](https://content.minetest.net/packages/BuckarooBanzay/blockexchange/) - it should now be fairly usable/stable.  Also, it has moved to a new home/address: https://blockexchange.minetest.ch/ instead of the .land domain).

### Mese Trains

{% include figure.html src="/static/blog/2022_September/mesejet_train.png"
    caption="MeseJets in a Railyard" %}

[Xenon](ttps://content.minetest.net/users/xenonca/) released the first version
of another Advanced Trains expansion pack. So far it only includes the MeseJet,
a bullet train that has color-coded line numbers displayed on its side.

### TNT Tag

[debiankaios](https://content.minetest.net/users/debiankaios/) released
[TNTtag](https://content.minetest.net/packages/debiankaios/tnttag/), a port of
the classic Minecraft minigame. Don't get tagged with tnt, and if you do get
tagged, be sure to tag someone else before the time runs out and the tnt on your
head explodes!

## Textures

### OhCeeDee Texture Pack

{% include figure.html src="/static/blog/2022_September/ocd.png"
    caption="The OCD texture pack" %}

[ROllerozxa](https://content.minetest.net/users/ROllerozxa/) released the [OhCeeDee texture pack](https://content.minetest.net/packages/ROllerozxa/ohceedee/), inspired by FVDisco's oCd Minecraft resource pack. 

## Art and Builds

{% include figure.html src="/static/blog/2022_September/temple_peppermint_patty.png"
    caption="Temple by Peppermint Patty" %}

{% include figure.html src="/static/blog/2022_September/super_sam.png"
    caption="Banner for the Super Sam game, art by Temhotaokeaha" %}

{% include figure_gallery.html items=page.wsortrains %}

{% include figure.html src="/static/blog/2022_September/castleprop.png"
    caption="One of x2048's props for testing lighting effects" %}

## Server News

### Nodecore Community Server
<sub>nodecore.mine.nu:30000</sub>

Nodecore was updated with the performance updates in the games section above.
That makes the performance of the Nodecore Community Server better than ever.

### A.E.S. Minigames
<sub>minetest.eticadigitale.org:30010</sub>

A.E.S. has a new beta minigame: Tnttag! Also, there are 2 new skins for you to
find and unlock by completing their parkours. 

BlockLeague has 

The November Block League tournament is coming up! BlockLeague is a shooter
minigame that is best described as "Soccer with guns". It now has passive
skills, and a menu for choosing them. Check out the pads to the side of the
Blockleague island to choose your skill. There will be up to 8 teams of 3
players each for the tournament. See the details
[here](https://forum.minetest.net/viewtopic.php?p=415626#p415626) for how to
sign up.

## In Other News

### Mindustry3d

GeneralBaker began a project to recreate Mindustry in 3d in Minetest. The first
stable release is still a long way off, but the project is looking for
contributers. Check it out here:
[Forum](https://forum.minetest.net/viewtopic.php?f=49&t=28685) and
[Git](https://gitlab.com/ReallyBasicGames/mindustry_3d)

### Blog Content

Its been more 7 months since the blog released. So far, content for the blog has
been collected on an ad-hoc basis - The blog editors see something interesting,
and put it in the blog. Other times, content creators approach editors about the
blog. It is much better for people to use the issue tracker
[here](https://github.com/minetest/blog/issues) or
[here](https://gitlab.com/minetest/blog/-/issues), to make it easy for your
content to get into the blog, and so we do not forget about your content. Thank
you to those who have used the issue tracker, it would be great if we can get
more people to use it!