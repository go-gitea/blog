---
date: "2019-05-30T10:50:00+01:00" 
author: "jolheiser"
title: "Gitea 1.8.2 is released"
tags: ["release"]
draft: false
---

We are proud to present the release of Gitea version 1.8.2. 

We have merged [13](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+milestone%3A1.8.2+is%3Aclosed) pull requests to release this version. 

You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.8.2/) - make sure to select the correct platform! For further details on how to install, follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our supporters on [Open Collective](https://opencollective.com/gitea) who are helping to sustain us financially.

<!--more-->

## Changelog

* BUGFIXES
  * Fix possible mysql invalid connnection error ([#7051](https://github.com/go-gitea/gitea/pull/7051)) ([#7071](https://github.com/go-gitea/gitea/pull/7071))
  * Handle invalid administrator username on install page ([#7060](https://github.com/go-gitea/gitea/pull/7060)) ([#7063](https://github.com/go-gitea/gitea/pull/7063))
  * Disable arm7 builds ([#7037](https://github.com/go-gitea/gitea/pull/7037)) ([#7042](https://github.com/go-gitea/gitea/pull/7042))
  * Fix default for allowing new organization creation for new users ([#7017](https://github.com/go-gitea/gitea/pull/7017)) ([#7034](https://github.com/go-gitea/gitea/pull/7034))
  * SearchRepositoryByName improvements and unification ([#6897](https://github.com/go-gitea/gitea/pull/6897)) ([#7002](https://github.com/go-gitea/gitea/pull/7002))
  * Fix u2f registrationlist ToRegistrations() method ([#6980](https://github.com/go-gitea/gitea/pull/6980)) ([#6982](https://github.com/go-gitea/gitea/pull/6982))
  * Allow collaborators to view repo owned by private org ([#6965](https://github.com/go-gitea/gitea/pull/6965)) ([#6968](https://github.com/go-gitea/gitea/pull/6968))
  * Use AppURL for Oauth user link ([#6894](https://github.com/go-gitea/gitea/pull/6894)) ([#6925](https://github.com/go-gitea/gitea/pull/6925))
  * Escape the commit message on issues update ([#6901](https://github.com/go-gitea/gitea/pull/6901)) ([#6902](https://github.com/go-gitea/gitea/pull/6902))
  * Fix regression for API users search ([#6882](https://github.com/go-gitea/gitea/pull/6882)) ([#6885](https://github.com/go-gitea/gitea/pull/6885))
  * Handle early git version's lack of get-url ([#7065](https://github.com/go-gitea/gitea/pull/7065)) ([#7076](https://github.com/go-gitea/gitea/pull/7076))
  * Fix wrong init dependency on markup extensions ([#7038](https://github.com/go-gitea/gitea/pull/7038)) ([#7074](https://github.com/go-gitea/gitea/pull/7074))
