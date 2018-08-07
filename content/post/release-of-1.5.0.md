---
date: "2018-07-07T10:00:00+00:00"
author: "thehowl"
title: "Gitea 1.5.0 is released"
tags: ["release"]
---

The time has come for another major release! We are happy to present Gitea
1.5.0 to the world. In this release, we merged
[258 pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.5.0+is%3Amerged)
-- just a bit more than last time (236).

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.5.0/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our backers on
[Open Collective](https://opencollective.com/gitea), who are helping us deliver
a better piece of software.

With that out of the way, here's what's new in 1.5.0:

<!--more-->

## Topics ([#3711](https://github.com/go-gitea/gitea/pull/3711))

![Topics demo](/demos/3711/1.gif)

You can now neatly organise your repositories using topics, similar to those
on GitHub.

_Thanks to [**@lunny**](https://github.com/lunny)_

## Emoji Completion ([#3433](https://github.com/go-gitea/gitea/pull/3433))

![Demo of emoji completion](/demos/3433/1.gif)

The issue editor will now provide suggestions for completing emojis when
starting to type an emoji shortcode - in a similar fashion to mention
autocompletion, which we added in 1.4.0.

_Thanks to [**@modmew8**](https://github.com/modmew8)_

## Global Code Search ([#3664](https://github.com/go-gitea/gitea/pull/3664))

![Screenshot of Global Code Search](/demos/3664/1.png)

We expanded our repo code search to allow for searching even MORE stuff - which
is to say, your entire Gitea instance! If you go on Explore, you will now be
able to search everywhere, **if you have code search enabled.**

_Thanks to [**@lunny**](https://github.com/lunny)_

## FIDO U2F Authentication ([#3971](https://github.com/go-gitea/gitea/pull/3971))

![](/demos/3971/1.gif)

Boost your security by adding FIDO U2F for authentication. 🚀

_Thanks to [**@JonasFranzDEV**](https://github.com/JonasFranzDEV)_

## Issue Due Date ([#3794](https://github.com/go-gitea/gitea/pull/3794))

![Screenshot of issue due dates in the issue listing](/demos/3794/1.png)
![Form to add a due date](/demos/3794/2.png)
![Added issue date](/demos/3794/3.png)

Deadlines: following them is both the Project Manager's dream and the
Developer's nightmare. But, time and again it has been proven that they are,
indeed, very useful, so now you can select due dates on issues to mark when they
_should_ be finished. Emphasis on the _should_ there.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Multiple Assignees ([#3705](https://github.com/go-gitea/gitea/pull/3705))

![Screenshot of 2 people being assigned to an issue.](/demos/3705/1.png)

In Gitea 1.5.0, you'll be able to assign multiple people to a single issue.
For cases where you'll need more manpower in order to understand the cryptic
code left by old developers of the legacy codebase.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Label Descriptions ([#3662](https://github.com/go-gitea/gitea/pull/3662))

![Label descriptions on the labels page](/demos/3662/1.png)

![Tooltip when hovering over a label](/demos/3662/2.png)
![Description is shown on the label picker as well](/demos/3662/3.png)

_Enhancement_ is a funny word, isn't it? It's sort of like a feature but it's
not as big as a feature. It might not be instantly clear to everyone who reads
it, but you can help them understand through the use of the new descriptions!

_Thanks to [**@lafriks**](https://github.com/lafriks)_

## Total Tracked Time ([#3341](https://github.com/go-gitea/gitea/pull/3341))

![Demo on a milestone](/demos/3341/1.png)

You can now track the total amount of time you spent on a single issue - or even
an entire milestone.

_Thanks to [**@JonasFranzDEV**](https://github.com/JonasFranzDEV)_

## Other changes

* You can now specify a second whitelist for protected branches, allowing you
  to select users who are able to merge PRs.
  ([#3689](https://github.com/go-gitea/gitea/pull/3689))
* We did some optimisations on the repository search feature - users report up
  to a 3x reduction in disk usage by the indexer.
  ([#3452](https://github.com/go-gitea/gitea/pull/3452))
* Power to webhooks! We added support for delete, fork, issues, issue\_comment,
  and release webhooks, which have long been a requested feature ever since
  webhooks first came to Gogs.
  ([#3929](https://github.com/go-gitea/gitea/pull/3929))
* Some changes were made to how Gitea handles messages with custom markup, such
  as commit messages and issue comments. Mentions, emails, links and so on
  should now be correctly handled.
  ([#3354](https://github.com/go-gitea/gitea/pull/3354))
* If your team is used to placing issue references in square brackes
  (ie. `[JIRA-123]`), we now correctly parse that!
  ([#3408](https://github.com/go-gitea/gitea/pull/3408))
* From the admin panel, you can now run `git fsck` (health check) on all your
  repositories, as well as disable it entirely if desired.
  ([#3606](https://github.com/go-gitea/gitea/pull/3606),
  [#3607](https://github.com/go-gitea/gitea/pull/3607))
* We added some new features to Gitea's API, such as issue search and
  attachments. ([#3478](https://github.com/go-gitea/gitea/pull/3478),
  [#3612](https://github.com/go-gitea/gitea/pull/3612))
* Symlinks in a repository are now marked by a distinctive icon.
  ([#3826](https://github.com/go-gitea/gitea/pull/3826))
* We'll remember your preferred language so that you don't have to change it for
  each browser that you use.
  ([#3875](https://github.com/go-gitea/gitea/pull/3875))
* If you want to disable time tracking entirely, you can now do so from the app
  settings. ([#3719](https://github.com/go-gitea/gitea/pull/3719))
* Various changes to improve consistency and grammar in the English
  localisation.
  ([Various](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+author%3Abugreport0+is%3Aclosed+milestone%3A1.5.0))
* You can now sort repos in Explore and the admin panel by stars or forks.
  ([#3969](https://github.com/go-gitea/gitea/pull/3969))
* If you use drone, there is now a handy plugin to create releases and
  attachments: <http://plugins.drone.io/drone-plugins/drone-gitea-release/>
* Starting from 1.5.0, we'll sign all our releases with our
  [GPG Key,](http://pool.sks-keyservers.net/pks/lookup?op=get&hash=on&fingerprint=on&search=0x2D9AE806EC1592E2)
  so you can be sure it's us.

To see all user-facing changes that went into the release, check out our
<!-- CHANGEME: change this whenever the full changelog is ready! -->
[full changelog](https://github.com/go-gitea/gitea/blob/master/CHANGELOG.md#140---2018-03-25).

A shoutout goes to those who reported and/or fixed security issues in this
release:

* [@cezar97](https://github.com/cezar97) ([#3878](https://github.com/go-gitea/gitea/pull/3878))

**Deprecation notice:** in the upcoming major release (1.6.0) we will drop
support for Go 1.8 and also embedded TiDB.

# Help us out!

Gitea is focused on community input and contributions. To keep a project like
Gitea going we need people. **_LOTS_** of people. You can help in the
following areas:

## Programming

If you know Go or HTML/CSS/JavaScript, you may be interested in working on the
code. Working on OSS may seem scary, but the best way is to try! Read the
[Gitea contribution guide](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md),
and then [find an itch to scratch](https://github.com/go-gitea/gitea/issues),
or scratch your own!

## Translating

Want to translate Gitea in your own language? Awesome! Join the Gitea project
on [Crowdin](https://crowdin.com/project/gitea). As soon as your translation is
approved, it will be pushed to the Gitea project to be used in future releases!

## Documentation

Documentation is important, but also time consuming. If you enjoy writing and
have a pretty good knowledge of English, or you would like to translate the
English version to your native language, you're very welcome to do so. Find our
documentation on the main git repository
[here](https://github.com/go-gitea/gitea/tree/master/docs). Just fork, update
the documentation and then create a pull request!

## Support

Do you like people? Can you give calm and thought-out responses to users needing
help? Then you can spend some time providing support to those who need it. Most
answers can really be found in the documentation, so make sure to take some time
to read it. Then, either join our chat or forums (linked below), or simply
help us sort out issues and answer questions on the
[Gitea repository](https://github.com/go-gitea/gitea/issues).

## Donations

If you, or your company, want to help us out sustain our financial expenses, you
can do so by donating on [Open Collective](https://opencollective.com/gitea#).

<a href="https://opencollective.com/gitea#backers" target="_blank"><img src="https://opencollective.com/gitea/backers.svg?width=890"></a>

<a href="https://opencollective.com/gitea/sponsor/0/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/1/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/2/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/3/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/4/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/5/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/6/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/7/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/8/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/9/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/9/avatar.svg"></a>

## … or reporting bugs

If you lack the time or knowledge to do any of the above, just using Gitea and sharing the word is enough to make us happy! One thing you can always do is to report any bugs you find on the [Gitea issue tracker](https://github.com/go-gitea/gitea/issues).

Before opening an issue, read the [contribution guidelines about reporting bugs](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md#bug-reports). After opening an issue, try to stick around a while to answer any questions we might have. Replies greatly help us find the root cause of an issue.

# Thanks

This release would not have been possible without the pull requests from the following people:

* [@0rzech](https://github.com/0rzech)
* [@AleksandrBulyshchenko](https://github.com/AleksandrBulyshchenko)
* [@alxwrd](https://github.com/alxwrd)
* [@andruwa13](https://github.com/andruwa13)
* [@appleboy](https://github.com/appleboy)
* [@aswild](https://github.com/aswild)
* [@aunger](https://github.com/aunger)
* [@axifive](https://github.com/axifive)
* [@bkcsoft](https://github.com/bkcsoft)
* [@BNolet](https://github.com/BNolet)
* [@bugreport0](https://github.com/bugreport0)
* [@Bwko](https://github.com/Bwko)
* [@cez81](https://github.com/cez81)
* [@charlesreid1](https://github.com/charlesreid1)
* [@Chri-s](https://github.com/Chri-s)
* [@christopherjmedlin](https://github.com/christopherjmedlin)
* [@cleverer](https://github.com/cleverer)
* [@coolaj86](https://github.com/coolaj86)
* [@daviian](https://github.com/daviian)
* [@derkoe](https://github.com/derkoe)
* [@devil418](https://github.com/devil418)
* [@dnmgns](https://github.com/dnmgns)
* [@domrim](https://github.com/domrim)
* [@dpeukert](https://github.com/dpeukert)
* [@ethantkoenig](https://github.com/ethantkoenig)
* [@FabioFortini](https://github.com/FabioFortini)
* [@flufmonster](https://github.com/flufmonster)
* [@francoism90](https://github.com/francoism90)
* [@funkyfuture](https://github.com/funkyfuture)
* [@harryxu](https://github.com/harryxu)
* [@HoffmannP](https://github.com/HoffmannP)
* [@inful](https://github.com/inful)
* [@InonS](https://github.com/InonS)
* [@jesselucas](https://github.com/jesselucas)
* [@JonasFranzDEV](https://github.com/JonasFranzDEV)
* [@kolaente](https://github.com/kolaente)
* [@lafriks](https://github.com/lafriks)
* [@liamcottam](https://github.com/liamcottam)
* [@lunny](https://github.com/lunny)
* [@marcinkuzminski](https://github.com/marcinkuzminski)
* [@michaelkuhn](https://github.com/michaelkuhn)
* [@microbug](https://github.com/microbug)
* [@modmew8](https://github.com/modmew8)
* [@monkeywithacupcake](https://github.com/monkeywithacupcake)
* [@mqudsi](https://github.com/mqudsi)
* [@naiba](https://github.com/naiba)
* [@neezer](https://github.com/neezer)
* [@nickolas360](https://github.com/nickolas360)
* [@phtan](https://github.com/phtan)
* [@pjeby](https://github.com/pjeby)
* [@qianlei90](https://github.com/qianlei90)
* [@rvillablanca](https://github.com/rvillablanca)
* [@sapk](https://github.com/sapk)
* [@sdwolfz](https://github.com/sdwolfz)
* [@serverwentdown](https://github.com/serverwentdown)
* [@Siosm](https://github.com/Siosm)
* [@stevegt](https://github.com/stevegt)
* [@tbraeutigam](https://github.com/tbraeutigam)
* [@techknowlogick](https://github.com/techknowlogick)
* [@teepark](https://github.com/teepark)
* [@tf198](https://github.com/tf198)
* [@thehowl](https://github.com/thehowl)
* [@Treora](https://github.com/Treora)
* [@tuxillo](https://github.com/tuxillo)
* [@vityafx](https://github.com/vityafx)
* [@xwjdsh](https://github.com/xwjdsh)

[PRs](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+milestone%3A1.5.0)
and [issues](https://github.com/go-gitea/gitea/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+milestone%3A1.5.0)
merged in 1.5.0.

# Get in touch

Need help with anything?
You can come on our [Discord server,](https://discord.gg/NsatcWJ) or if you're
more old-fashioned you can also use our [forums](https://discourse.gitea.io/).
