---
date: "2018-10-09T23:00:00+03:00"
author: "lafriks"
title: "Gitea 1.5.2 is released"
tags: ["release"]
---

We are happy to announce version 1.5.2 of Gitea has now been released. This
is a smaller release, with only 12 merged PRs, but it contains several
security related fixes and so we recommend upgrading whenever possible.

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.5.2/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank beeonthego for reporting the security issue that have been patched
in this release. Another thank you goes to all of our supporters on
[Open Collective](https://opencollective.com/gitea) who are also helping us
with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Enforce token on api routes ([#4840](https://github.com/go-gitea/gitea/pull/4840)) ([#4905](https://github.com/go-gitea/gitea/pull/4905))
* BUGFIXES
  * Remove links from topics in edit mode ([#5030](https://github.com/go-gitea/gitea/pull/5030))
  * Detect charset and convert non UTF-8 files for display ([#4950](https://github.com/go-gitea/gitea/pull/4950)) ([#4994](https://github.com/go-gitea/gitea/pull/4994))
  * Fix layout of the topics editing form ([#4971](https://github.com/go-gitea/gitea/pull/4971)) ([#4993](https://github.com/go-gitea/gitea/pull/4993))
  * Fix null pointer dereference in ParseCommitWithSignature ([#4964](https://github.com/go-gitea/gitea/pull/4964))
  * Fix url in discord webhook ([#4951](https://github.com/go-gitea/gitea/pull/4951))
  * Fix font-cropping UI bug in diff ([#4726](https://github.com/go-gitea/gitea/pull/4726)) ([#4929](https://github.com/go-gitea/gitea/pull/4929))
  * Fix bug forget to remove Stopwatch when remove repository ([#4933](https://github.com/go-gitea/gitea/pull/4933))
  * Fix bug when repo remained bare if multiple branches pushed ([#4927](https://github.com/go-gitea/gitea/pull/4927))
  * Fix redirect with non-ascii branch names ([#4764](https://github.com/go-gitea/gitea/pull/4764)) ([#4887](https://github.com/go-gitea/gitea/pull/4887))
  * Fix issues api allow pulls ([#4852](https://github.com/go-gitea/gitea/pull/4852)) ([#4862](https://github.com/go-gitea/gitea/pull/4862))
  * Fix trimming of markup section names ([#4864](https://github.com/go-gitea/gitea/pull/4864))
