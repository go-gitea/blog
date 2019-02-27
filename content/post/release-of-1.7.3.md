---
date: "2019-02-27T12:00:00-05:00" 
author: "jolheiser"
title: "Release of 1.7.3"
tags: ["release"]
draft: false
---

We proudly present the minor release of Gitea version 1.7.3.
We have merged 11 pull requests to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.7.3/),
you just need to select the correct platform. For further installation details, follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

Another thank you goes to all of our supporters on [Open Collective](https://opencollective.com/gitea)
who are also helping us with financial sustainment.

<!--more-->

## Changelog

* BUGFIXES
  * Fix server 500 when trying to migrate to an already existing repository ([#6188](https://github.com/go-gitea/gitea/pull/6188)) ([#6197](https://github.com/go-gitea/gitea/pull/6197))
  * Load Issue attributes for API /repos/{owner}/{repo}/issues/{index} ([#6122](https://github.com/go-gitea/gitea/pull/6122)) ([#6185](https://github.com/go-gitea/gitea/pull/6185))
  * Fix bug whereby user could change private repository to public when force private enabled. ([#6156](https://github.com/go-gitea/gitea/pull/6156)) ([#6165](https://github.com/go-gitea/gitea/pull/6165))
  * Fix bug when update owner team then visit team's repo return 404 ([#6119](https://github.com/go-gitea/gitea/pull/6119)) ([#6166](https://github.com/go-gitea/gitea/pull/6166))
  * Fix heatmap and repository menu display in Internet Explorer 9+ ([#6117](https://github.com/go-gitea/gitea/pull/6117)) ([#6137](https://github.com/go-gitea/gitea/pull/6137))
  * Fix prohibit login check on authorization ([#6106](https://github.com/go-gitea/gitea/pull/6106)) ([#6115](https://github.com/go-gitea/gitea/pull/6115))
  * Fix LDAP protocol error regression by moving to ldap.v3 ([#6105](https://github.com/go-gitea/gitea/pull/6105)) ([#6107](https://github.com/go-gitea/gitea/pull/6107))
  * Fix deadlock in webhook PullRequest ([#6102](https://github.com/go-gitea/gitea/pull/6102)) ([#6104](https://github.com/go-gitea/gitea/pull/6104))
  * Fix redirect loop when password change is required and Gitea is installed as a suburl ([#5965](https://github.com/go-gitea/gitea/pull/5965)) ([#6101](https://github.com/go-gitea/gitea/pull/6101))
  * Fix compare button regression ([#5929](https://github.com/go-gitea/gitea/pull/5929)) ([#6098](https://github.com/go-gitea/gitea/pull/6098))
  * Recover panic in orgmode.Render if bad orgfile ([#4982](https://github.com/go-gitea/gitea/pull/4982)) ([#5903](https://github.com/go-gitea/gitea/pull/5903)) ([#6097](https://github.com/go-gitea/gitea/pull/6097))
