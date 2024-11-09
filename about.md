---
title: About
description: About the Luanti blog
layout: page
---

# About

## What is Luanti?

[Luanti](https://www.minetest.net) is an open source voxel game engine. See
the website for more information.

<a href="https://www.minetest.net/" class="button is-primary">
	Luanti Website
</a>

## What is the Luanti blog?

We post updates about once per month (subject to change) to let you know what's
new with Luanti. We cover everything about Luanti, from engine development,
to mod and game progress, to server news and community events. Even
Luanti-related artwork has a place here. Posts are subdivided by general
topic.

We can also do special posts about important events or updates important to the
general Luanti community.

## Who is behind the Luanti Blog?

<div class="columns">
	{% for pair in site.data.authors %}
		<div class="column is-one-quarter">
			<div class="media">
				<div class="media-left">
					<figure class="image is-48x48 mx-0">
						<img src="{{ pair[1].avatar }}" alt="{{ pair[0] }}">
					</figure>
				</div>
				<div class="media-content">
					<p class="title is-5 m-0">
						<a href="{{ pair[1].url }}">
							{{ pair[0] }}
						</a>
					</p>
					<p class="subtitle is-6 m-0 mt-1">
						{{ pair[1].role }}
					</p>
				</div>
			</div>
		</div>
	{% endfor %}
</div>

## Contributing to Posts

Are you working with Luanti? We'd love to know what's new with you! We're
looking for news about engine/mod/game development, servers, art and builds,
and more.

If you have something great to share:

1. Read the [submission guidelines](https://github.com/minetest/blog/blob/master/.github/CONTRIBUTING.md).

2. Make an issue on the
   [GitHub issue tracker](https://github.com/minetest/blog/issues).

   Alternatively, you can contact an editor on the forums
   ([MisterE](https://forum.luanti.org/memberlist.php?mode=viewprofile&u=26284))
   or post an issue on [GitLab](https://gitlab.com/minetest/blog/-/issues).
