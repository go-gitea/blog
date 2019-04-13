---
date: "2019-04-13T10:50:00+01:00" 
author: "zeripath"
title: "Gitea 1.7.6 is released"
tags: ["release"]
draft: false
---

We proudly present the security release of Gitea version 1.7.6. **This release contains a very important security fix so it is highly recommended to update to this version.** Users running our version 1.8 release candidates should also update.

We have merged 2 pull requests to release this version.

You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.7.6/) - make sure to select the correct platform! For further details on how to install, follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to [zeripath](https://github.com/zeripath) who reported and fixed the security issue fixed in this release, and [mrsdizzie](https://github.com/mrsdizzie) who confirmed and produced a minimal exploitable testcase for the security issue.

We'd like to thank all of our supporters on [Open Collective](https://opencollective.com/gitea) who are helping us with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Prevent remote code execution vulnerability with mirror repo URL settings ([#6593](https://github.com/go-gitea/gitea/pull/6593)) ([#6595](https://github.com/go-gitea/gitea/pull/6595))

* BUGFIXES
  * Allow resend of confirmation email when logged in ([#6482](https://github.com/go-gitea/gitea/pull/6482)) ([#6487](https://github.com/go-gitea/gitea/pull/6487))
