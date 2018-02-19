---
date: "2018-02-19T13:30:00+02:00"
author: "lafriks"
title: "Release of 1.3.3"
tags: ["release"]
draft: false
---

We proudly present the bugfix release of Gitea version 1.3.3. This release contains important
security fixes so it is highly recomended to update to latest release.
We have merged [5 pull requests](https://github.com/go-gitea/gitea/milestone/20?closed=1) to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.3.3/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* SECURITY
  * Fix escaping changed title in comments (#3530) (#3535)
  * Escape search query display (#3486) (#3489)
* BUGFIXES
  * Fix repo-transfer-and-team-repo-count bug (#3241) (#3244)
  * Open external tracker in blank window, consistently with wiki (#3227) (#3228)
  * Change SSL Mode from checkbox to string in admin page (#3208) (#3211)
