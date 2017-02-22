---
date: "2017-02-22T13:57:00+08:00"
author: "lunny"
title: "Release of 1.0.2"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.0.2. We have merged [9](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20milestone%3A1.0.2) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.0.2/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Fixed issue counter [#882](https://github.com/go-gitea/gitea/pull/882)
  * Fixed XSS vulnerability on wiki page [#955](https://github.com/go-gitea/gitea/pull/955)
  * Add data dir without session to dump [#587](https://github.com/go-gitea/gitea/pull/587)
  * Fixed wiki page renaming [#958](https://github.com/go-gitea/gitea/pull/958)
  * Drop default console logger if not required [#960](https://github.com/go-gitea/gitea/pull/960)
  * Fixed docker docs link on install page [#972](https://github.com/go-gitea/gitea/pull/972)
  * Handle SetModel errors [#957](https://github.com/go-gitea/gitea/pull/957)
  * Fixed XSS vulnerability on milestones [#977](https://github.com/go-gitea/gitea/pull/977)
  * Fixed XSS vulnerability on alerts [#981](https://github.com/go-gitea/gitea/pull/981)