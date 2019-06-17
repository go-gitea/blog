---
date: "2019-06-17T10:50:00+01:00" 
author: "jolheiser"
title: "Gitea 1.8.3 is released"
tags: ["release"]
draft: false
---

We are proud to present the release of Gitea version 1.8.3. 

We have merged [8](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+milestone%3A1.8.3+is%3Aclosed) pull requests to release this version. 

You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.8.3/) - make sure to select the correct platform! For further details on how to install, follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our supporters on [Open Collective](https://opencollective.com/gitea) who are helping to sustain us financially.

<!--more-->

## Changelog

* BUGFIXES
  * Always set userID on LFS authentication ([#7224](https://github.com/go-gitea/gitea/pull/7224))
  * Fix LFS Locks over SSH ([#6999](https://github.com/go-gitea/gitea/pull/6999)) ([#7223](https://github.com/go-gitea/gitea/pull/7223))
  * Fix duplicated file on pull request conflicted files ([#7211](https://github.com/go-gitea/gitea/pull/7211)) ([#7214](https://github.com/go-gitea/gitea/pull/7214))
  * Detect noreply email address as user ([#7133](https://github.com/go-gitea/gitea/pull/7133)) ([#7195](https://github.com/go-gitea/gitea/pull/7195))
  * Don't get milestone from DB if ID is zero ([#7169](https://github.com/go-gitea/gitea/pull/7169)) ([#7174](https://github.com/go-gitea/gitea/pull/7174))
  * Allow archived repos to be (un)starred and (un)watched ([#7163](https://github.com/go-gitea/gitea/pull/7163)) ([#7168](https://github.com/go-gitea/gitea/pull/7168))
  * Fix GCArgs load from ini ([#7156](https://github.com/go-gitea/gitea/pull/7156)) ([#7157](https://github.com/go-gitea/gitea/pull/7157))
