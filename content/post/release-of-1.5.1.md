---
date: "2018-09-03T10:00:00+00:00"
author: "techknowlogick"
title: "Gitea 1.5.1 is released"
tags: ["release"]
---

We are happy to announce version 1.5.1 of Gitea has now been released. This
is a smaller release, with only 9 merged PRs, but it contains several
security related fixes and so we recommend upgrading whenever possible.

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.5.1/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank Cezar97 for reporting the security issues that have been patched
in this release. Another thank you goes to all of our supporters on
[Open Collective](https://opencollective.com/gitea) who are also helping us
with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Don't disclose emails of all users when sending out emails ([#4784](https://github.com/go-gitea/gitea/pull/4784))
  * Improve URL validation for external wiki and external issues ([#4710](https://github.com/go-gitea/gitea/pull/4710)) ([#4740](https://github.com/go-gitea/gitea/pull/4740))
  * Make cookies HttpOnly and obey COOKIE_SECURE flag ([#4706](https://github.com/go-gitea/gitea/pull/4706)) ([#4707](https://github.com/go-gitea/gitea/pull/4707))
* BUGFIXES
  * Fix missing release title in webhook ([#4783](https://github.com/go-gitea/gitea/pull/4783)) ([#4800](https://github.com/go-gitea/gitea/pull/4800))
  * Make sure to reset commit count in the cache on mirror syncing ([#4770](https://github.com/go-gitea/gitea/pull/4770))
  * Fixed bug where team with admin privelege type doesn't get any unit ([#4759](https://github.com/go-gitea/gitea/pull/4759))
  * Fix failure on creating pull request with assignees ([#4583](https://github.com/go-gitea/gitea/pull/4583)) ([#4727](https://github.com/go-gitea/gitea/pull/4727))
  * Hide org/create menu item in Dashboard if user has no rights ([#4678](https://github.com/go-gitea/gitea/pull/4678)) ([#4686](https://github.com/go-gitea/gitea/pull/4686))
* TRANSLATION
  * Fix incorrect caption of webhook setting ([#4701](https://github.com/go-gitea/gitea/pull/4701)) ([#4718](https://github.com/go-gitea/gitea/pull/4718))

