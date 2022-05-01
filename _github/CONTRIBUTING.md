# Contributing to the blog

## What you can contribute

Are you working with Minetest? We'd love to know what's new with you! We're
looking for news about engine/mod/game development, servers, art and builds,
and more.

Submission inclusion is up to the discretion of the editors; their decision
should be guided by the submission guidelines. If you disagree with a
decision, you can ask another editor, but as a whole, the editors' say is final.
Editors will edit submissions to fit the style and voice of a post; they might
not include some information you submit (e.g: excessive advertisement) and they
might or might not give warning about the changes made.


## Submission Guidelines

We ask that you follow these guidelines when making issues to submit post content:

Required:

* In the issue, format the issue title like: `[content] content description`.
Replace `content description` with a very brief title/description of your submission.
* Include who is working on the project.
* Include a brief description. Keep it short. Links to further details are encouraged.
* Do not post about extremely trivial updates. Actually share project status updates, news or something new. While shills are allowed/encouraged to a degree, you need a good excuse to shill your project. No "hey check out my project that I made last year". New projects, major updates, and events are all good "excuses".
* No NSFW content or projects allowed.

Highly recommended:

* One or two screenshots or GIFs that *effectively* communicates your message. The screenshot may or may not be included in the final post depending on how important your update is deemed to be by the editors, and how well the screenshot adds to understanding the message. Don't expect to have a screenshot of Minetest Game included in a post about a general API update, for example.
* Include who took the screenshot.

IMPORTANT:

The blog editors will consider the content submitted for each post. They will
build the upcoming post using the content provided. The issues for each content
submission will be closed when the content is included in the upcoming post, or
when the post occurs. You submission will not be included if it doesn't meet the
basic requirements. The editors may choose to respond to the issue to give you a
chance to fix any problems. Regardless, at each post release, all outstanding
content submission issues will be closed to make way for the next release.
Please only submit content for current updates.

### Cover screenshots, Build screenshots, and Art

Each post should have a cover screenshot that will be the background for the
title. We may also include a "Minetest at its best" screenshot, showing players
having fun, and show some cool builds.

Please make submissions each month for these! When you make the issue, format
the title like: `[Screenshot] ` Include who took the screenshot, and any
descriptive caption you think fits well.

## New post guidelines

Use <../_drafts/YYYYY-MM-DD-template.md> as a template when creating new
posts.

Each post should have a folder in static/blog contains images and other
resources. Each post should have a cover image, as described above.

### Release procedure

* Open a pull request with the post to the minetest/blog repository.
* Editors are in charge of reviewing the post. If an editor wrote the post, then
  at least one other editor should proofread/review.
* When ready to release, merge into `master`.

### Post-release procedure

- [ ] Tell rubenwardy to post on Twitter and Mastodon.
- [ ] Create new post on Reddit and the forums.
- [ ] Edit post to add link to the forums in front matter
      (`forum_topic: https://...`).
- [ ] Post in Discord, IRC, and Matrix.
