---
date: "2018-01-25T12:00:00+00:00"
author: "thehowl"
title: "Gitea 1.4 is released"
tags: ["release"]
draft: true
---

Hello! Yet another release cycle is over; this time around we merged [X pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.4.0+is%3Amerged) - we made sure to deliver as much as we could in this new Gitea version, and we're sure you're going to like it.

Starting from this release, we'll also make sure to walk you through the most important changes we made - instead of just dumping the PRs closed in this release and their category. And boy have we got a lot of stuff to talk about.

<!--more-->

## Reactions ([#2856](https://github.com/go-gitea/gitea/pull/2856))

![Screenshot of Reactions](/demos/2856/1.png)

![Screenshot of Reactions](/demos/2856/2.png)

Yes. Yes! YES!!! Gitea now has reactions on pull requests and issues. Maybe now your inbox won't be crammed with "+1" emails from your collaborators. Oh yeah 😎.

_Thanks to **[@lafriks](https://github.com/lafriks)**_

## Responsive UI ([#2750](https://github.com/go-gitea/gitea/pull/2750))

![Responsive UI screenshot](/demos/2750/1.png)

![Responsive UI screenshot](/demos/2750/2.png)

![Responsive UI screenshot](/demos/2750/3.png)

Starting from version 1.4.0, Gitea's web interface is finally responsive; this means it can be properly used from your phone without having to pinch everywhere to see what is on the screen! There may be some places where the interface is still not completely responsive, in which case we ask you kindly to [file an issue](https://github.com/go-gitea/gitea/issues) if there isn't one already, posting screenshots of what does not work.

_Thanks to **[@thehowl](https://github.com/thehowl)**_

## Merge options in Pull Requests ([#3188](https://github.com/go-gitea/gitea/pull/3188))

![Screenshot of merge options](/demos/3188/1.png)

Hey, look! Someone submitted a pull request to your repo. Awesome. Except... it needs some work. And some more work. And some more. Just a tiny little bit... Done. Add also a few thousand merge-from-master commits along the way. And so you know that after the merge, your git history will never be the same again... that is, until today! Thanks to Squash and Merge, you can squash all the commits into a single one, and leave your git history stainless! We also added support for Rebase and Merge, similar to GitHub's merge options.

_Thanks to **[@lafriks](https://github.com/lafriks)**_

## Mention completion in issue editor ([#3136](https://github.com/go-gitea/gitea/pull/3136))

![Mention completion demo](/demos/3136/1.gif)

"Is this the right username?" is no more. With our shiny new mention completion, you can now start typing an username or a name of someone on your Gitea instance, and results will start popping up as you type.

_Thanks to **[@harryxu](https://github.com/harryxu)**_

## Progress bar for issues with checkboxes ([#3171](https://github.com/go-gitea/gitea/pull/3171))

![Progress bar demo](/demos/3171/1.png)

Did you know that Gitea has, like GitHub, support for checkboxes in markdown? If you write a bulletpoint in the following format: `- [ ]` you will get a nice HTML textbox. And what does this have to do with checkboxes? Everything, of course! The issue list will now show the percentage of checked items in the top issue post. So you always know how far you've gotten on the roadmap.

_Thanks to **[@modmew8](https://github.com/modmew8)**_

## Long commits now have an expandable body ([#2980](https://github.com/go-gitea/gitea/pull/2980))

![Commit body expansion demo](/demos/2980/1.gif)

Did someone write an entire essay in the commit message? Now you can view the entire contents of it without changing the page; you will only need to press on the ellipsis button, similar to what you can see on GitHub and GitLab.

_Thanks to **[@sondr3](https://github.com/sondr3)**_

## Mark all notifications as read ([#3097](https://github.com/go-gitea/gitea/pull/3097))

![Mark notifications as read demo](/demos/3097/1.png)

Woah. You just came back from your holidays, and you should probably catch up on everything that happened at work... but should you? You can always sneakily dismiss all notifications. This tiny little button will also make that much easier for you ;).

_Thanks to **[@svarmalov](https://github.com/svarmalov)**_

## Write access for deploy keys ([#3225](https://github.com/go-gitea/gitea/pull/3225))

![Screenshot showing a Read/Write deploy key and a Read deploy key](/demos/3225/1.png)

In some cases, you may need to grant your server write access to the repository. Who knows, perhaps because of a tool that automatically generates and commits code? Either way, starting today, deploy keys can now be set to also have the ability to "write" to a repository. Power to the servers!

_Thanks to **[@vtemian](https://github.com/vtemian)**_

## Customize Gitea ([#3051](https://github.com/go-gitea/gitea/pull/3051), [#3286](https://github.com/go-gitea/gitea/pull/3286))

Did you know that you can modify templates without fearing merge conflicts by re-creating them inside the `custom` folder of your Gitea instance? This has always allowed you to change parts of Gitea to suit your own needs and make it your own. From this release, we also added a few templates which will allow you to place custom JS/CSS. You can find all of this on the [documentation](https://docs.gitea.io/en-us/customizing-gitea/#customizing-gitea-pages).

_Thanks to **[@bkcsoft](https://github.com/bkcsoft)** and **[@lafriks](https://github.com/lafriks)**_

# Other changes

- **BREAKING:** if you used `GOGS_WORK_DIR` to change the working directory of Gitea, that won't work anymore - you'll need to use `GITEA_WORK_DIR`. ([#2946](https://github.com/go-gitea/gitea/pull/2946))
- Is your Gitea server running on HTTPS? Now you can tweak your settings to create an HTTP server which will redirect all its requests to the HTTPS server! ([#1928](https://github.com/go-gitea/gitea/pull/1928))
- We now serve .patch and .diff files for pull requests, just like GitHub does. ([#3239](https://github.com/go-gitea/gitea/pull/3293), [#3305](https://github.com/go-gitea/gitea/pull/3305))
- The default app.ini now resides in `custom/conf/app.ini.sample` - this should make it slightly less confusing for new users to find where the default configuration is. ([#1522](https://github.com/go-gitea/gitea/pull/1522))
- If you're a [Dingtalk](https://www.dingtalk.com/en) user, you'll be happy to know webhooks now support it starting from 1.4.0. Hooray! ([#2777](https://github.com/go-gitea/gitea/pull/2777))
  - As a reminder, we currently support webhooks for Slack, Discord and Gitea's own format, as well as a version for Gogs, to keep backwards compatibility. Also, Gitea and Gogs are mostly compatible with GitHub's webhooks!
- Git LFS aficionados: we added support for the [File Locking API](https://github.com/git-lfs/git-lfs/blob/master/docs/api/locking.md). ([#2938](https://github.com/go-gitea/gitea/pull/2938))
- Parlez-vous français? The Gitea docs are now also available in [French](https://docs.gitea.io/fr-fr/). Keep in mind that the only language that is guaranteed to be kept up-to-date on the documentation is English; all other languages may have information that is inaccurate, so please stick to english if you want to make sure everything works in the latest gitea version. ([#3030](https://github.com/go-gitea/gitea/pull/3030))
- Shoutout to [@silverwind](https://github.com/silverwind) for making various minor improvements to the UI, you can see all of them [here](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+author%3Asilverwind+milestone%3A1.4.0).
- If you run the `gitea` executable with no commands, it will now run the default webserver. Which means, unless you want to specify any flag, you can run gitea just by typing `./gitea`. ([#3331](https://github.com/go-gitea/gitea/pull/3331))

# Help us out!

Gitea is a Gogs fork that focuses especially on community input and contributions - and to keep a project like this going we need people. **_LOTS_** of people. Not for feeding, of course, but to help us in the following areas:

## Programming

If you know Go, or HTML/CSS/JS, then you may be interested in working directly on the code. It may seem scary. It may seem like you know nothing about this and you're probably best off not doing anything - but the best way is to try. Give a good read to the [contribution guide,](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md) and then [find an itch to scratch,](https://github.com/go-gitea/gitea/issues) unless you have your own.

## Translating

Feeling like helping to translate Gitea in your own language? Awesome! You can join the Gitea project on [Crowdin.](https://crowdin.com/project/gitea) As soon as your translation is approved, it will be pushed to the Gitea project, in order to be used for future releases!

## Documentation

Documentation is important, but unfortunately often overlooked and time-consuming. Nevertheless, if you enjoy writing and have a pretty good knowledge of English, or you would like to translate the English version to your native language, then you're very welcome to do so. You can find our documentation on the main git repository [here.](https://github.com/go-gitea/gitea/tree/master/docs) Just fork, change the documentation, then create a pull request!

## Support

Do you like humans? Can you give calm and thought-out responses to users needing help? Then you can spend some time providing support to those who need it. Most answers can really be found in the documentation, so make sure to take some time to read it through. Then, either join our chat or forums (linked below), or simply answer question issues on the [Gitea repository.](https://github.com/go-gitea/gitea/issues)

## ... or just reporting bugs

Finally, if you lack the time or knowledge to do any of the above, it's completely fine. Just using Gitea and sharing the word is enough to make us happy :) Although, one thing you could always do is that to report the bugs you find on the [Gitea repository](https://github.com/go-gitea/gitea/issues) - if you don't, we may never be able to find them!

Before opening a new issue, remember to read the [contribution guidelines about reporting bugs](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md#bug-reports) - it's pretty important that you also try at least to find some time to eventually answer the issues you report - otherwise, we'd be just talking to a wall and the problem would never get fixed :(.

# Thanks

This release would not have been possible without the pull requests from the following people:

<!-- I hacked together a quick python script: in case I disappear, you can just change the release ID on this: https://gist.github.com/thehowl/e10b1526517a8436ec83fe8e15cf9edf -->
* [@0rzech](https://github.com/0rzech)
* [@AlbertoGP](https://github.com/AlbertoGP)
* [@appleboy](https://github.com/appleboy)
* [@bibaijin](https://github.com/bibaijin)
* [@bkcsoft](https://github.com/bkcsoft)
* [@cez81](https://github.com/cez81)
* [@ethantkoenig](https://github.com/ethantkoenig)
* [@Exagone313](https://github.com/Exagone313)
* [@harryxu](https://github.com/harryxu)
* [@haytona](https://github.com/haytona)
* [@jsstrn](https://github.com/jsstrn)
* [@lafriks](https://github.com/lafriks)
* [@lunny](https://github.com/lunny)
* [@M2shad0w](https://github.com/M2shad0w)
* [@makarchuk](https://github.com/makarchuk)
* [@MCF](https://github.com/MCF)
* [@michaelkuhn](https://github.com/michaelkuhn)
* [@modmew8](https://github.com/modmew8)
* [@mrexodia](https://github.com/mrexodia)
* [@MTecknology](https://github.com/MTecknology)
* [@pluehne](https://github.com/pluehne)
* [@romanegunkov](https://github.com/romanegunkov)
* [@sapk](https://github.com/sapk)
* [@schaffman5](https://github.com/schaffman5)
* [@silverwind](https://github.com/silverwind)
* [@sondr3](https://github.com/sondr3)
* [@stesachse](https://github.com/stesachse)
* [@strk](https://github.com/strk)
* [@svarlamov](https://github.com/svarlamov)
* [@tboerger](https://github.com/tboerger)
* [@techknowlogick](https://github.com/techknowlogick)
* [@thehowl](https://github.com/thehowl)
* [@uncled1023](https://github.com/uncled1023)
* [@vtemian](https://github.com/vtemian)
* [@wmantly](https://github.com/wmantly)
* [@znegva](https://github.com/znegva)

[PRs](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+milestone%3A1.4.0) and [issues](https://github.com/go-gitea/gitea/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+milestone%3A1.4.0) merged in 1.4.0.

# Get in touch

Our public chat, relayed across all the following systems, is available here:

- [Discord](https://discord.gg/NsatcWJ)
- [Matrix](https://matrix.to/#/#gitea:matrix.org)
- [IRC](http://webchat.freenode.net/?channels=%23gitea) (#gitea @ chat.freenode.net)

If you're more into forums, [we have one as well](https://discourse.gitea.io/).
