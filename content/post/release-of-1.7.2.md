---
date: "2019-02-14T09:12:00+08:00"
author: "jolheiser"
title: "Release of 1.7.2"
tags: ["release"]
draft: false
---

We proudly present the minor release of Gitea version 1.7.2.
We have merged 24 pull requests to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.7.1/),
you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

Another thank you goes to all of our supporters on [Open Collective](https://opencollective.com/gitea)
who are also helping us with financial sustainment.

<!--more-->

## Changelog

* BUGFIXES
  * Remove all CommitStatus when a repo is deleted ([#5940](https://github.com/go-gitea/gitea/pull/5940)) ([#5941](https://github.com/go-gitea/gitea/pull/5941))
  * Fix notifications on pushing with deploy keys by setting hook environment variables ([#5935](https://github.com/go-gitea/gitea/pull/5935)) ([#5944](https://github.com/go-gitea/gitea/pull/5944))
  * Silence console logger in gitea serv ([#5887](https://github.com/go-gitea/gitea/pull/5887)) ([#5943](https://github.com/go-gitea/gitea/pull/5943)) 
  * Handle milestone webhook events for issues and PR ([#5947](https://github.com/go-gitea/gitea/pull/5947)) ([#5955](https://github.com/go-gitea/gitea/pull/5955))
  * Show user who created the repository instead of the organization in action feed ([#5948](https://github.com/go-gitea/gitea/pull/5948)) ([#5956](https://github.com/go-gitea/gitea/pull/5956))
  * Fix ssh deploy and user key constraints ([#1357](https://github.com/go-gitea/gitea/pull/1357)) ([#5939](https://github.com/go-gitea/gitea/pull/5939)) ([#5966](https://github.com/go-gitea/gitea/pull/5966))
  * Fix bug when deleting a linked account will removed all ([#5989](https://github.com/go-gitea/gitea/pull/5989)) ([#5990](https://github.com/go-gitea/gitea/pull/5990))
  * Fix empty ssh key importing in ldap ([#5984](https://github.com/go-gitea/gitea/pull/5984)) ([#6009](https://github.com/go-gitea/gitea/pull/6009))
  * Fix metrics auth token detection ([#6006](https://github.com/go-gitea/gitea/pull/6006)) ([#6017](https://github.com/go-gitea/gitea/pull/6017))
  * Create repository on organisation by default on its dashboard ([#6026](https://github.com/go-gitea/gitea/pull/6026)) ([#6048](https://github.com/go-gitea/gitea/pull/6048))
  * Make sure labels are actually returned in API ([#6053](https://github.com/go-gitea/gitea/pull/6053)) ([#6059](https://github.com/go-gitea/gitea/pull/6059))
  * Switch to more recent build of xgo ([#6070](https://github.com/go-gitea/gitea/pull/6070)) ([#6072](https://github.com/go-gitea/gitea/pull/6072))
  * In basic auth check for tokens before call UserSignIn ([#5725](https://github.com/go-gitea/gitea/pull/5725)) ([#6083](https://github.com/go-gitea/gitea/pull/6083))
