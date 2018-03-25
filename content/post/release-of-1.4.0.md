---
date: "2018-03-25T12:00:00+00:00"
author: "thehowl"
title: "Gitea 1.4.0 is released"
tags: ["release"]
draft: false
---

The Gitea 1.4.0 release is done, with a total of [236 merged pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.4.0+is%3Amerged). We made sure to deliver as many new features as possible in this version—you're going to love it!

You can download one of pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.4.0/). For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

Starting this release, we'll walk you through the most important changes. We've got a lot to talk about for Gitea 1.4.0.

<!--more-->

## Reactions ([#2856](https://github.com/go-gitea/gitea/pull/2856))

![Screenshot of Reactions](/demos/2856/1.png)

![Screenshot of Reactions](/demos/2856/2.png)

Gitea now features reactions for pull requests and issues. Quickly share your thoughts or lighten up the mood of technical discussions.

_Thanks to **[@lafriks](https://github.com/lafriks)**_

## Responsive UI ([#2750](https://github.com/go-gitea/gitea/pull/2750))

![Responsive UI screenshot](/demos/2750/1.png)

![Responsive UI screenshot](/demos/2750/2.png)

![Responsive UI screenshot](/demos/2750/3.png)

In Gitea 1.4 we've updated the web interface to a responsive layout. This makes Gitea easier to read and use on phones and tablets. Please [file an issue](https://github.com/go-gitea/gitea/issues) with screenshots if you encounter parts that do not adapt correctly to smaller displays - while we did our best to test it thoroughly, we may have missed some spots!

_Thanks to **[@thehowl](https://github.com/thehowl)**_

## Merge options in Pull Requests ([#3188](https://github.com/go-gitea/gitea/pull/3188))

![Screenshot of merge options](/demos/3188/1.png)

We've added support for 'Rebase and Merge' and 'Squash and Merge', which should allow you to keep your git history tidier. Rebase and Merge will not create a merge commit, whereas Squash and Merge will squash all the commits of the PR into one, so that in the repository's history it looks like a single commit was added.

_Thanks to **[@lafriks](https://github.com/lafriks)**_

## Mention completion in issue editor ([#3136](https://github.com/go-gitea/gitea/pull/3136))

![Mention completion demo](/demos/3136/1.gif)

Gitea now understands the @-syntax when typing a comment and will pop up a username auto-completion dialog. This makes selecting the right username a breeze.

_Thanks to **[@harryxu](https://github.com/harryxu)**_

## Progress bar for issues with checkboxes ([#3171](https://github.com/go-gitea/gitea/pull/3171))

![Progress bar demo](/demos/3171/1.png)

Issue lists in Gitea 1.4 show progress bars for issues that include checkboxes. Add checkboxes to your issue by typing `- [ ]` (unchecked state) or `- [X]` (checked state). This way, you can easily keep track of the progress you've made towards closing the issue.

_Thanks to **[@modmew8](https://github.com/modmew8)**_

## Long commits now have an expandable body ([#2980](https://github.com/go-gitea/gitea/pull/2980))

![Commit body expansion demo](/demos/2980/1.gif)

You can now quickly expand long commit messages inline using the ellipsis next to it.

_Thanks to **[@sondr3](https://github.com/sondr3)**_

## Mark all notifications as read ([#3097](https://github.com/go-gitea/gitea/pull/3097))

![Mark notifications as read demo](/demos/3097/1.png)

Gitea 1.4 adds a button to the notifications list to easily dismiss all unread notifications.

_Thanks to **[@svarmalov](https://github.com/svarmalov)**_

## Write access for deploy keys ([#3225](https://github.com/go-gitea/gitea/pull/3225))

![Screenshot showing a Read/Write deploy key and a Read deploy key](/demos/3225/1.png)

Deploy keys can now also be allowed to write to repositories. This is useful in cases where a tool automatically generates and commits code.

_Thanks to **[@vtemian](https://github.com/vtemian)**_

## Customize Gitea ([#3051](https://github.com/go-gitea/gitea/pull/3051), [#3286](https://github.com/go-gitea/gitea/pull/3286))

Gitea's `custom` folder already allowed you to customize parts of Gitea to your needs. In Gitea 1.4, we added templates allowing you to also customize JavaScript and CSS. Read all about this in the [documentation](https://docs.gitea.io/en-us/customizing-gitea/#customizing-gitea-pages).

_Thanks to **[@techknowlogick](https://github.com/techknowlogick)** and **[@tboerger](https://github.com/tboerger)**_

# Other changes

- **BREAKING:** if you used `GOGS_WORK_DIR` to change the working directory of Gitea, that won't work anymore - you'll need to use `GITEA_WORK_DIR`. ([#2946](https://github.com/go-gitea/gitea/pull/2946))
- Is your Gitea server running on HTTPS? Now you can tweak your settings to create an HTTP server which will redirect all its requests to the HTTPS server. ([#1928](https://github.com/go-gitea/gitea/pull/1928))
- We now serve .patch and .diff files for pull requests, just like GitHub does. ([#3239](https://github.com/go-gitea/gitea/pull/3293), [#3305](https://github.com/go-gitea/gitea/pull/3305))
- The default app.ini now resides in `custom/conf/app.ini.sample` - this should make it slightly less confusing for new users to find where the default configuration is. ([#1522](https://github.com/go-gitea/gitea/pull/1522))
- If you're a [Dingtalk](https://www.dingtalk.com/en) user, you'll be happy to know webhooks now support it starting from 1.4.0. Hooray! ([#2777](https://github.com/go-gitea/gitea/pull/2777))
  - As a reminder, we currently support webhooks for Slack, Discord and Gitea's own format, as well as a version for Gogs, to keep backwards compatibility. Also, Gitea and Gogs are mostly compatible with GitHub's webhooks!
- Git LFS aficionados: we added support for the [File Locking API](https://github.com/git-lfs/git-lfs/blob/master/docs/api/locking.md). ([#2938](https://github.com/go-gitea/gitea/pull/2938))
- Parlez-vous français? The Gitea docs are now also available in [French](https://docs.gitea.io/fr-fr/). Keep in mind that the only language that is guaranteed to be kept up-to-date on the documentation is English; all other languages may have information that is inaccurate, so please stick to english if you want to make sure everything works in the latest gitea version. ([#3030](https://github.com/go-gitea/gitea/pull/3030))
- Shoutout to [@silverwind](https://github.com/silverwind) for making various minor improvements to the UI, you can see all of them [here](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+author%3Asilverwind+milestone%3A1.4.0).
- If you run the `gitea` executable with no commands, it will now run the default webserver. Which means, unless you want to specify any flag, you can run gitea just by typing `./gitea`. ([#3331](https://github.com/go-gitea/gitea/pull/3331))

# Help us out!

Gitea is focused on community input and contributions. To keep a project like Gitea going we need people. **_LOTS_** of people. Feel free to help in the following areas:

## Programming

If you know Go or HTML/CSS/JavaScript, you may be interested in working on the code. It may seem scary, but the best way is to try! Read the [Gitea contribution guide](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md), and then [find an itch to scratch](https://github.com/go-gitea/gitea/issues), or scratch your own!

## Translating

Want to translate Gitea in your own language? Awesome! Join the Gitea project on [Crowdin](https://crowdin.com/project/gitea). As soon as your translation is approved, it will be pushed to the Gitea project to be used in future releases!

## Documentation

Documentation is important, but also time consuming. If you enjoy writing and have a pretty good knowledge of English, or you would like to translate the English version to your native language, you're very welcome to do so. Find our documentation on the main git repository [here](https://github.com/go-gitea/gitea/tree/master/docs). Just fork, update the documentation and then create a pull request!

## Support

Do you like people? Can you give calm and thought-out responses to users needing help? Then you can spend some time providing support to those who need it. Most answers can really be found in the documentation, so make sure to take some time to read it. Then, either join our chat or forums (linked below), or simply answer question issues on the [Gitea repository](https://github.com/go-gitea/gitea/issues).

## … or reporting bugs

If you lack the time or knowledge to do any of the above, just using Gitea and sharing the word is enough to make us happy! One thing you can always do is to report any bugs you find on the [Gitea issue tracker](https://github.com/go-gitea/gitea/issues).

Before opening an issue, read the [contribution guidelines about reporting bugs](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md#bug-reports). After opening an issue, try to stick around a while to answer any questions we might have. Replies greatly help us find the root cause of an issue.

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
