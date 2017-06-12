---
date: "2017-06-12T17:21:30+08:00"
author: "appleboy"
title: "Release of 1.1.2"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.1.2. We have merged [5](https://github.com/go-gitea/gitea/milestone/11?closed=1) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.1.2/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * fix bug not to trim space of login username [#1806](https://github.com/go-gitea/gitea/pull/1806)
  * Backport bugfixes #1220 and #1393 to v1.1 [#1758](https://github.com/go-gitea/gitea/pull/1758)
  * Enforce netgo build tag while cross-compilation (backport #1690) [#1731](https://github.com/go-gitea/gitea/pull/1731)
  * fix delete user failed on sqlite (#1321) [#1737](https://github.com/go-gitea/gitea/pull/1737)
  * fix update avatar [#1724](https://github.com/go-gitea/gitea/pull/1724)
