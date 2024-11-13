---
layout: post
title: "August and September in Minetest (15)"
contributors:
  - 56independent
  - erlehmann
  - Niklp
  - rubenwardy
  - MisterE
authors:
  - GreenXenith
description: >
  The main menu gets more love in preparation for the 5.8.0 release, developers come and go, and new shaders are in the works. CTF celebrates its 10th anniversary, and new API mods make their way to ContentDB.
tags:
  - last_month
image: /static/blog/2023_AugustSeptember/header.jpg

forum_topic: https://forum.luanti.org/viewtopic.php?f=18&t=29889

pulls: https://github.com/minetest/minetest/pull
gallery_shaders:
- src: /static/blog/2023_AugustSeptember/godrays.jpg
  caption: Godrays through the trees
- src: /static/blog/2023_AugustSeptember/reflections.jpg
  caption: Screen-space water reflections
gallery_ctf:
- src: /static/blog/2023_AugustSeptember/ctf1.jpg
  caption: Party hats and fireworks
- src: /static/blog/2023_AugustSeptember/ctf2.jpg
  caption: Fireworks in the sky
gallery_httpblocks:
- src: /static/blog/2023_AugustSeptember/httpblock1.jpg
  caption: Downloaded HTML
- src: /static/blog/2023_AugustSeptember/httpblock2.jpg
  caption: HTTP Statuses
gallery_unicodetext:
- src: /static/blog/2023_AugustSeptember/unicodetext1.jpg
  caption: Unicode text test
- src: /static/blog/2023_AugustSeptember/unicodetext2.jpg
  caption: Signs with unicode
gallery_archtec:
- src: /static/blog/2023_AugustSeptember/archtec1.jpg
- src: /static/blog/2023_AugustSeptember/archtec2.jpg
---

The main menu gets more love in preparation for the 5.8.0 release, developers come and go, and new shaders are in the
works. CTF celebrates its 10th anniversary, and new API mods make their way to ContentDB.

<!-- more -->

- [Engine News](#engine-news)
- [Games News](#games-news)
- [Mods News](#mods-news)
- [Art and Builds](#art-and-builds)
- [Server News](#server-news)
- [Other News](#other-news)

## Engine News
As the 5.8.0 release marches closer, more work has been done to improve the main menu. It [now uses the latest version
of formspec]({{page.pulls}}/13761), [properly supports hypertext]({{page.pulls}}/13731), and uses [a button in place of the settings tab]({{page.pulls}}/13762). The user experience has been improved with [better game bar
scrolling]({{page.pulls}}/13768), [persisting text fields]({{page.pulls}}/13685), and [asynchronous package
loading]({{page.pulls}}/13551) on the ContentDB page.

Minetest's newest core developer, [grorp](https://github.com/grorp), has been hard at work fixing various GUI and
rendering issues, improving the user experience, and squashing lots of bugs. [41 commits and
counting!](https://github.com/minetest/minetest/commits?author=grorp)

Desour has [been
busy](https://github.com/minetest/minetest/commits?author=Desour&before=c90c545d3395dc22f1ec43ca4f8a95e0f6fa5a14+35)
cleaning up GUI elements, the sound manager, and compiler warnings.

We extend a heartfelt farewell to x2048 as he steps down from engine development, and thank him for his work on
[bloom]({{page.pulls}}/12791), [shadow
maps](https://github.com/search?q=repo%3Aminetest%2Fminetest+shadow+author%3Ax2048&type=commits&s=committer-date&o=asc),
[mesh rendering](https://github.com/search?q=repo%3Aminetest%2Fminetest+mesh+author%3Ax2048&type=commits), and numerous
[other improvements](https://github.com/minetest/minetest/commits?author=x2048). His [sky color]({{page.pulls}}/12654),
[cascaded shadow maps]({{page.pulls}}/13833), and [batched particle rendering]({{page.pulls}}/13833) PRs are looking for
adopters.

Even more shaders are in development as well. Godrays developed by x2048 (now [adopted and in
testing]({{page.pulls}}/13881)) complement bloom and shadows wonderfully. GreenXenith has been working on a [highly
experimental screen-space reflection shader](https://github.com/GreenXenith/minetest/tree/bfs_ssr) for water and other
materials. It has a long way to go but adds another layer of beauty to the Minetest world.

{% include figure_gallery.html items=page.gallery_shaders %}

## Games News

### Capture the Flag
August 16th, 2023 was [Capture the Flag](https://content.luanti.org/packages/rubenwardy/capturetheflag/)'s 10th
anniversary. Capture the Flag is a multiplayer game where two teams of players battle to claim the other team's flag
while defending their own. It is played in a destructible voxel environment, allowing players to build defenses and
place traps.

You can find out more about CTF's history and development in [the 10th anniversary blog
post](https://blog.rubenwardy.com/2023/08/16/minetest-ctf-is-10/).

The game anniversary and 8th anniversary of the official server (`ctf.rubenwardy.com:30001`) were celebrated from August
16th to September 1st, with fireworks and party hats as cosmetics on the server.

{% include figure_gallery.html items=page.gallery_ctf %}

### Glitch
[The winner of the 2022 Minetest GAME JAM](https://content.luanti.org/packages/Wuzzy/glitch/) has continued
development since then. [As of August](https://forum.luanti.org/viewtopic.php?p=428292#p428292), Glitch (by Wuzzy) has
[a weblate](https://translate.codeberg.org/projects/glitch/) where the community can contribute game translations. You
can read about the development history of Glitch on [Wuzzy's
website](https://wuzzy.codeberg.page/games/makingof_glitch/).

## Mods News

### HTTP Blocks
You can send `POST` and `GET` requests directly from Minetest using the new [HTTPBlocks mod by
56independent](https://content.luanti.org/packages/56independent/httpblock/)! This
[Digilines](https://content.luanti.org/packages/Jeija/digilines/) device allows you to construct complex systems that
can talk to web endpoints and request plaintext files, records, and any other raw web data.

The mod, of course, requires HTTP trust to use Minetest's HTTP API. Future plans include HTML querying using selector
blocks, blocks to convert JSON to Lua tables, and maybe websocket support in the distant future.

{% include figure_gallery.html items=page.gallery_httpblocks %}

### Unicode Text Rendering
The [Unicode Text library by erlehmann](https://content.luanti.org/packages/erlehmann/unicode_text/) is built to
render fixed-width and variable-width [GNU Unifont fonts](http://savannah.gnu.org/projects/unifont/) (`.hex`). UTF-8
text input is converted to a table of pixels that can be written to an image file (such as a
[PNG](https://github.com/minetest/minetest/blob/5.7.0/doc/lua_api.txt#L5089-L5102) or
[TGA](https://content.luanti.org/packages/erlehmann/tga_encoder/)). Non-Unicode text can also be written using the
Unifont CSUR font.

By rendering text to a single image server-side, the full range of Unicode can be supported by servers without sending
thousands or tens of thousands of textures to Minetest clients. The [Unicode Signs mod by
cora](https://content.luanti.org/packages/cora/ucsigns/) provides signs that use the Unicode Text library to draw
text.

{% include figure_gallery.html items=page.gallery_unicodetext %}

## Art and Builds

{% include figure.html src="/static/blog/2023_AugustSeptember/build_camper.jpg" caption='"Who wants to cook?" by
1.1.8.4' %}

{% include figure.html src="/static/blog/2023_AugustSeptember/build_cityhall.jpg" caption='"City hall, German Creative
Server" by Toadie' %}

{% include figure.html src="/static/blog/2023_AugustSeptember/build_computer.jpg" caption='"Mesecon-only (without
Luacontrollers) computer" by 1F616EMO' %}

## Server News

### Archtec
<sub>archtec.niklp.net:30803</sub>

{% include figure_gallery.html items=page.gallery_archtec %}

The [Arctech server](https://archtec.niklp.net/) recently added chat bridges to Matrix and IRC
for more flexible communication while in-game. Their building team has also been working on some cool new creations!

## Other News
Keep an eye out for the 2023 Minetest GAME JAM later this year!
