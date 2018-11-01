---
date: "2018-10-31T12:00:00+03:00"
author: "lafriks"
title: "Gitea 1.5.3 is released"
tags: ["release"]
---

We are happy to announce version 1.5.3 of Gitea has now been released. This
is a smaller release, with only 1 merged PRs, but it contains critcal
security fix for vulnerability that could potentially allow for authorized
users to do remote code excution.

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.5.3/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank [5alt](https://github.com/5alt) for reporting security issue
that have been patched in this release. Another thank you goes to all of our
supporters on [Open Collective](https://opencollective.com/gitea) who are also
helping us with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Fix remote command execution vulnerability in upstream library ([#5177](https://github.com/go-gitea/gitea/pull/5177)) ([#5196](https://github.com/go-gitea/gitea/pull/5196))
