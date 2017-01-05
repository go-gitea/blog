---
date: "2017-01-05T15:00:00+02:00"
author: "tboerger"
title: "Release of 1.0.1"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.0.1. We have merged [9](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20milestone%3A1.0.1) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.0.1/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Fixed localized MIN_PASSWORD_LENGTH [#501](https://github.com/go-gitea/gitea/pull/501)
  * Fixed 500 error on organization delete [#507](https://github.com/go-gitea/gitea/pull/507)
  * Ignore empty wiki repo on migrate [#544](https://github.com/go-gitea/gitea/pull/544)
  * Proper check access for forking [#563](https://github.com/go-gitea/gitea/pull/563)
  * Fix SSH domain on installer [#506](https://github.com/go-gitea/gitea/pull/506)
  * Fix missing data rows on admin UI [#580](https://github.com/go-gitea/gitea/pull/580)
  * Do not delete tags with releases by default [#579](https://github.com/go-gitea/gitea/pull/579)
  * Fix missing session config data on admin UI [#578](https://github.com/go-gitea/gitea/pull/578)
  * Properly show the version within footer on the UI [#593](https://github.com/go-gitea/gitea/pull/593)
