---
date: "2018-06-26T09:30:00-05:00"
author: "techknowlogick"
title: "Release of 1.4.3"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.4.3. This release contains important
security fixes so it is highly recommended to update to latest release.
We have merged [9 pull requests](https://github.com/go-gitea/gitea/milestone/25?closed=1) to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.4.3/), you just need to select the correct platform.
For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to those who reported security issues fixed in this release.

* [@nickolas360](https://github.com/nickolas360) [#4192](https://github.com/go-gitea/gitea/pull/4192)
* [@glitch003](https://github.com/glitch003) and INSERT OTHER RESEARCHER HERE [#4307](https://github.com/go-gitea/gitea/issues/4307)

<!--more-->

## Changelog

* SECURITY
  * HTML-escape plain-text READMEs (#4192) (#4214)
  * Fix open redirect vulnerability on login screen (#4312) (#4312)
* BUGFIXES
  * Fix broken monitoring page when running processes are shown (#4203) (#4208)
  * Fix delete comment bug (#4216) (#4228)
  * Delete reactions added to issues and comments when deleting repository (#4232) (#4237)
  * Fix wiki URL encoding bug (#4091) (#4254)
  * Fix code tab link when viewing tags (#3908) (#4263)
  * Fix webhook type conflation (#4285) (#4285)
