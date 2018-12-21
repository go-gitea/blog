---
date: "2018-12-21T01:00:00+02:00"
author: "techknowlogick"
title: "Release of 1.6.2"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.6.2. This release contains important
security fixes so it is highly recommended to update to latest release.
We have merged 10 pull requests to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.6.2/),
you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to those who reported security issues fixed in this release.

* [Louis from @PentesterLab](https://github.com/PentesterLab) ([#5571](https://github.com/go-gitea/gitea/pull/5571))
* [@simia-zaru ](https://github.com/simia-zaru ) ([#5570](https://github.com/go-gitea/gitea/pull/5570))

Another thank you goes to all of our supporters on [Open Collective](https://opencollective.com/gitea)
who are also helping us with financial sustainment.

<!--more-->

## Changelog
* SECURITY
  * Sanitize uploaded file names ([#5571](https://github.com/go-gitea/gitea/pull/5571)) ([#5573](https://github.com/go-gitea/gitea/pull/5573))
  * HTMLEncode user added text ([#5570](https://github.com/go-gitea/gitea/pull/5570)) ([#5575](https://github.com/go-gitea/gitea/pull/5575))
* BUGFIXES
  * Fix indexer reindex bug when gitea restart ([#5563](https://github.com/go-gitea/gitea/pull/5563)) ([#5564](https://github.com/go-gitea/gitea/pull/5564))
  * Remove a double slash in the HTTPS redirect with Let's Encrypt ([#5537](https://github.com/go-gitea/gitea/pull/5537)) ([#5539](https://github.com/go-gitea/gitea/pull/5539))
  * Fix bug when a read perm user to edit his issue ([#5516](https://github.com/go-gitea/gitea/pull/5516)) ([#5534](https://github.com/go-gitea/gitea/pull/5534))
  * Detect force push failure on deletion of protected branches ([#5522](https://github.com/go-gitea/gitea/pull/5522)) ([#5531](https://github.com/go-gitea/gitea/pull/5531))
  * Let's Encrypt handler listens on correct port for certificate validation ([#5525](https://github.com/go-gitea/gitea/pull/5525)) ([#5527](https://github.com/go-gitea/gitea/pull/5527))
  * Fix forgot deletion of notification when delete repository ([#5506](https://github.com/go-gitea/gitea/pull/5506)) ([#5514](https://github.com/go-gitea/gitea/pull/5514))
  * Fix undeleted content when deleting user ([#5429](https://github.com/go-gitea/gitea/pull/5429)) ([#5509](https://github.com/go-gitea/gitea/pull/5509))
  * Fix empty wiki ([#5504](https://github.com/go-gitea/gitea/pull/5504)) ([#5508](https://github.com/go-gitea/gitea/pull/5508))
