---
date: "2017-08-07T10:53:30+08:00"
author: "lunny"
title: "Release of 1.1.3"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.1.3. We have merged [6](https://github.com/go-gitea/gitea/milestone/12?closed=1) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.1.3/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Fix PR template error (#2008)
  * Fix markdown rendering (fix #1530) (#2043)
  * Fix missing less sources for oauth (backport #1288) (#2135)
  * Don't ignore gravatar error (#2138)
  * Fix diff of renamed and modified file (#2136)
  * Fix fast-forward PR bug (#2137)
  * Fix some security bugs