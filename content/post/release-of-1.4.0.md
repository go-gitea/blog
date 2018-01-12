---
date: "2018-01-25T12:00:00+00:00"
author: "thehowl"
title: "Gitea 1.4 is released"
tags: ["release"]
draft: true
---

<style>
/* TEMPORARY: need to update theme. see https://github.com/go-gitea/theme/issues/48 */
img {
	max-width: 100%;
}
</style>

Hello! Yet another release cycle is over; this time around we merged [X pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.4.0+is%3Amerged) - we made sure to deliver as much as we could in this new Gitea version, and we're sure you're going to like it.

Starting from this release, we'll also make sure to walk you through the most important changes we made - instead of just dumping the PRs closed in this release and their category. And boy have we got a lot of stuff to talk about.

<!--more-->

## Reactions ([#2856](https://github.com/go-gitea/gitea/pull/2856))

![Screenshot of Reactions](/demos/2856/1.png)

![Screenshot of Reactions](/demos/2856/2.png)

Yes. Yes! YES!!! Gitea now has reactions on pull requests and issues. Now hopefully your collaborators will shut up with their "+1" comments on the issue and will instead just press the 👍 button. Oh yeah 😎.

_Thanks to **[@lafriks](https://github.com/lafriks)**_

## Responsive UI ([#2750](https://github.com/go-gitea/gitea/pull/2750))

![Responsive UI screenshot](/demos/2750/1.png)

![Responsive UI screenshot](/demos/2750/2.png)

![Responsive UI screenshot](/demos/2750/3.png)

Starting from version 1.4.0, Gitea's web interface is finally responsive; this means it can be properly used from your phone without having to pinch everywhere to see what is on the screen! There may be some places where the interface is still not completely responsive, in which case we ask you kindly to [file an issue](https://github.com/go-gitea/gitea/issues) if there isn't one already, posting screenshots of what does not work.

_Thanks to **[@thehowl](https://github.com/thehowl)**_

## Mention completion in issue editor ([#3136](https://github.com/go-gitea/gitea/pull/3136))

![Mention completion demo](/demos/3136/1.gif)

"Is this the right username?" is no more. With our shiny new mention completion, you can now start typing an username or a name of someone on your Gitea instance, and results will start popping up as you type.

_Thanks to **[@harryxu](https://github.com/harryxu)**_

## Long commits now have an expandable body ([#2980](https://github.com/go-gitea/gitea/pull/2980))

![Commit body expansion demo](/demos/2980/1.gif)

Making a long commit? Now you can view the entire contents of it without changing the page; you will only need to press on the ellipsis button, similar to what you can see on GitHub and GitLab.

_Thanks to **[@sondr3](https://github.com/sondr3)**_

## Mark all notifications as read ([#3097](https://github.com/go-gitea/gitea/pull/3097))

TODO: screenshot. Would do that but I need to mock two notifications, and I can't be bothered just yet.

Woah. You just came back from your holidays, and you should probably catch up on everything that happened at work... but should you? You can always sneakily dismiss all notifications. This tiny little button will also make that much easier for you ;).

_Thanks to **[@svarmalov](https://github.com/svarmalov)**_

## Customize Gitea

TODO: set of PRs that enable better customizability

* https://github.com/go-gitea/gitea/pull/3051
* https://github.com/go-gitea/gitea/pull/3286
* https://github.com/go-gitea/gitea/issues/2115
* https://github.com/go-gitea/gitea/pull/3345
* https://docs.gitea.io/en-us/customizing-gitea/#customizing-gitea-pages

TODO: quick guide on how to customize gitea, and tell users about the custom
folder.

# Other changes

- **BREAKING:** if you used `GOGS_WORK_DIR` to change the working directory of Gitea, that won't work anymore - you'll need to use `GITEA_WORK_DIR`. ([#2946](https://github.com/go-gitea/gitea/pull/2946))
- The default app.ini now resides in `custom/conf/app.ini.sample` - this should make it slightly less confusing for new users to find where the default configuration is. ([#1522](https://github.com/go-gitea/gitea/pull/1522))
- Is your Gitea server running on HTTPS? Now you can tweak your settings to create an HTTP server which will redirect all its requests to the HTTPS server! ([#1928](https://github.com/go-gitea/gitea/pull/1928))
- If you're a [Dingtalk](https://www.dingtalk.com/en) user, you'll be happy to know webhooks now support it starting from 1.4.0. Hooray! ([#2777](https://github.com/go-gitea/gitea/pull/2777))
  - As a reminder, we currently support webhooks for Slack, Discord and Gitea's own format, as well as a version for Gogs, to keep backwards compatibility. Also, Gitea and Gogs are mostly compatible with GitHub's webhooks!
- Parlez-vous français? The Gitea docs now feature [French](https://docs.gitea.io/fr-fr/). Keep in mind that the only language that is guaranteed to be kept up-to-date on the documentation is English; all other languages may have information that is inaccurate, so please stick to english if you want to make sure everything works in the latest gitea version. ([#3030](https://github.com/go-gitea/gitea/pull/3030))
- Shoutout to [@silverwind](https://github.com/silverwind) for making various minor improvements to the UI, you can see all of them [here](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+author%3Asilverwind+milestone%3A1.4.0).
- We now serve .patch and .diff files for pull requests, just like GitHub does. ([#3239](https://github.com/go-gitea/gitea/pull/3293), [#3305](https://github.com/go-gitea/gitea/pull/3305))
- If you run the `gitea` executable with no commands, it will now run the default webserver. Which means, unless you want to specify any flag, you can run gitea just by typing `./gitea`. ([#3331](https://github.com/go-gitea/gitea/pull/3331))

# Help us out!

Gitea is a Gogs fork that focuses especially on community input and contributions - and to keep a project like this going we need people. **_LOTS_** of people. Not for feeding, of course, but to help us in the following areas:

## Programming

If you know Go, or HTML/CSS/JS, then you may be interested in working TODO

## Translating

TODO

## Documentation

TODO

## Support

TODO

## ... or just reporting bugs

TODO

# Thanks

TODO: List of usernames of merged PRs

# Full changelog

TODO: Changelog like the previous versions.

# Get in touch

Our public chat, relayed across all the following systems, is available here:

- [Discord](https://discord.gg/NsatcWJ)
- [Matrix](https://matrix.to/#/#gitea:matrix.org)
- [IRC](http://webchat.freenode.net/?channels=%23gitea) (#gitea @ chat.freenode.net)

If you're more into forums, [we have one as well](https://discourse.gitea.io/).
