---
date: "2019-01-04T01:00:00+02:00"
author: "jonasfranz"
title: "Release of 1.6.3"
tags: ["release"]
draft: false
---

We proudly present the security release of Gitea version 1.6.3. **This release contains a very important
security fix so it is highly recommended to update to latest release.**
We have merged 2 pull requests to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.6.3/),
you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to [zeripath](https://github.com/zeripath) who reported and fixed the security issue fixed in this release.

Another thank you goes to all of our supporters on [Open Collective](https://opencollective.com/gitea)
who are also helping us with financial sustainment.

<!--more-->

## Changelog
* SECURITY
  * Prevent DeleteFilePost doing arbitrary deletion (#5631)
* BUGFIX
  * Fix wrong text getting saved on editing second comment on an issue (#5608)
