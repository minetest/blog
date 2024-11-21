---
layout: post
title: "Introducing Our New Name"
description: >-
  After more than a year of public and internal discussions, we're ready to
  announce our new name!
authors: [Zughy, GreenXenith]
contributors: [FreshReplicant, grorp]
image: /static/blog/New_Name/cover.jpg
image_credit: Zughy
forum_topic: https://forum.luanti.org/viewtopic.php?t=31048
---

"Is this a Minecraft clone? Is it like Minecraft Alpha?" If you've been a member of our community for some time, you are
probably aware of how often these questions remind us of what people think of when they hear the name "Minetest": a
rip-off of a similar genre-defining game. Truth be told, that was celeron55's initial plan. But things change, and
Minetest evolved. Now, the time has come for Minetest to assume a new identity and prove it has moved beyond its
original purpose.

<!-- more -->

## A Bit of History

After seeing Minecraft's alpha debut, celeron55 "took it as a challenge" to explore "the mystery of how a game world
like this works under the hood"[^wikinews]. The name wasn't very important; it was a test after all— an experiment to
see what it could do differently. An experiment that began attracting more users and contributors throughout the years
until Minetest eventually evolved from a game to what it is today: a game platform.

Through the efforts of the community over the past decade, Minetest has developed a unique identity with an approachable
API and easy scripting language, support for community-created games and mods, a central library to easily find
community content, and more recently a shift to promoting community creations instead of the original Minetest Game.
Despite these advancements, one anachronistic holdover has remained to remind us of the past: an idea that no longer
describes the purpose of this project and community— its name.

After more than a year of public and internal discussions, that era is over. "Minetest" is no more; the "Minecraft
clone" is no more. With great thanks to the community for their input, we wave goodbye to Minetest and introduce a new
era. Welcome 🥁 ... **Luanti!**

## Luanwhat?

"Luanti" is a wordplay on the Finnish word *luonti* ("creation") and the programming language ~~Minetest~~ Luanti employs
for games and mods, *Lua*. The goal was to avoid yet another plain English word (good luck finding something unique...)
and highlight the core principles of the project. The fusion of celeron55's Finnish nationality and the platform's focus
on content creation resulted in the birth of "Luanti".

We decided to avoid using "free" or "libre" in the name because we don't think it does the project justice. Luanti will
always be free software, but that core principle is not everything it has to offer. Projects like Blender, Krita, or
Godot are awesome, and they don't need to convince you about their libre nature by putting it in their names. They are
libre, but they're also much, much more!

Luanti is a lot of things. Many of us are familiar with the voxel nature of the engine and the library of content it
supports, and name suggestions related to that idea were certainly plentiful. But describing that in the new name would
limit the platform in the same way as the original: users and developers would come to expect it to be an engine
exclusive to cube games when it can be more than that. Luanti is a platform that is built to help you create. It's a
platform where anyone can make something. It's a platform that will keep evolving to support your creations.

## Moving Forward

With the new name, a few changes will be made in the engine and community. Obviously, all the repositories and community
hubs will adopt the Luanti name in some form. You'll be able to find the website at luanti.org and repositories at
[github.com/luanti-org](https://github.com/luanti-org) (many old links will redirect). Our social platforms will change
similarly. The logo will be staying, and you'll probably still hear "Minetest" occasionally in reference to [Minetest
Game](https://content.luanti.org/packages/Minetest/minetest_game/) which will remain a testament to the project's
roots. Otherwise, Luanti now represents the future of the platform.

For developers, the engine won't actually change much. For those who aren't aware, `core` is actually the real Lua
namespace used internally, `minetest` is just an alias (which we will keep for compatibility). Rather than rename all
the namespaces to `luanti`, `core` will be the official namespace to use. It's shorter to type, easier to remember, and
backwards-compatible. It's also friendlier to forks and future name changes (which we don't plan to do, promise!)

We hope that, free from the ghost of its past, Luanti can bloom into something more and bring life to adventures and
experiences for years to come. It can now live and breathe on its own, explore its nature and potential, and overcome
its limits. At the very least, we can finally say to those who once asked "Is this a Minecraft clone?": No, not anymore.
It came from humble beginnings and has grown into a powerful game platform where you, and anyone else, can start
creating. And with your help, it will continue to grow into something even better.

What do you think about the new name? Let us know in the forum thread or on any of our community platforms!

---

##### Sources:

[^wikinews]: [Open source game developer Perttu Ahola talks about Minetest with Wikinews](https://en.wikinews.org/wiki/Open_source_game_developer_Perttu_Ahola_talks_about_Minetest_with_Wikinews)
