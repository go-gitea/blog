---
date: "2017-12-09T23:26:00+08:00"
author: "Lunny"
title: "Release of 1.3.1"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.3.1. We have merged [7 pull requests](https://github.com/go-gitea/gitea/milestone/18?closed=1) to release this version. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.3.1/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Sanitize logs for mirror sync (#3057, #3082) (#3078)
  * Fix missing branch in release bug (#3108) (#3117)
  * Fix repo indexer and submodule bug (#3107) (#3110)
  * Fix legacy URL redirects (#3100) (#3106)
  * Fix redis session failed (#3086) (#3089)
  * Fix issue list branch link broken (#3061) (#3070)
  * Fix missing password length check when change password (#3039) (#3071)
