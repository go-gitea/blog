---
date: "2017-10-26T17:21:30+02:00"
author: "Lafriks"
title: "Release of 1.2.2"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.2.2. We have merged [5 pull requests](https://github.com/go-gitea/gitea/milestone/16?closed=1) to release this version. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.2.2/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Add checks for commits with missing author and time (#2771) (#2785)
  * Fix sending mail with a non-latin display name (#2559) (#2783)
  * Sync MaxGitDiffLineCharacters with conf/app.ini (#2779) (#2780)
  * Update vendor git (#2765) (#2772)
  * Fix emojify image URL (#2769) (#2773)
