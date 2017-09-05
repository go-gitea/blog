---
date: "2017-09-05T11:53:30+08:00"
author: "lunny"
title: "Release of 1.1.4"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.1.4. We have merged [6](https://github.com/go-gitea/gitea/milestone/13?closed=1) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.1.4/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Fix rendering of external links (#2292) (#2315)
  * Fix deleted milestone bug (#1942) (#2300)
  * fix 500 error when view an issue which's milestone deleted (#2297) (#2299)
  * Fix SHA1 hash linking (#2143) (#2293)
  * Fix rendering of issue checkboxes (#2291)
  * Fix some security bugs