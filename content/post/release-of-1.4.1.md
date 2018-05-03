---
date: "2018-05-03T09:30:00+02:00"
author: "techknowlogick"
title: "Release of 1.4.1"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.4.1. This release contains important
security fixes so it is highly recommended to update to latest release.
We have merged [17 pull requests](https://github.com/go-gitea/gitea/milestone/22?closed=1) to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.4.1/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to those who reported security issues fixed in this release.

* [@nubenum](https://github.com/nubenum) ([#3778](https://github.com/go-gitea/gitea/pull/3778))
* Bernd Ziegenbalg ([#3721](https://github.com/go-gitea/gitea/pull/3721))
* [Kacper Szurek](https://security.szurek.pl/) ([#3871](https://github.com/go-gitea/gitea/pull/3871))
* shannara (IRC) ([#3887](https://github.com/go-gitea/gitea/pull/3887))

<!--more-->

## Changelog

* BREAKING
  * Add "error" as reserved username (#3882) (#3886)
* SECURITY
  * Do not allow inactive users to access repositories using private key (#3887) (#3889)
  * Fix path cleanup in file editor, when initilizing new repository and LFS oids  (#3871) (#3873)
  * Remove unnecessary allowed safe HTML (#3778) (#3779)
  * Correctly check http git access rights for reverse proxy authorized users (#3721) (#3743)
* BUGFIXES
  * Fix to use only needed columns from tables to get repository git paths (#3870) (#3883)
  * Fix GPG expire time display when time is zero (#3584) (#3884)
  * Fix to update only issue last update time when adding a comment (#3855) (#3860)
  * Fix repository star count after deleting user (#3781) (#3783)
  * Use the active branch for the code tab (#3720) (#3776)
  * Set default branch name on first push (#3715) (#3723)
  * Show clipboard button if disable HTTP of git protocol (#3773) (#3774)
