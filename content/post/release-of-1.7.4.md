---
date: "2019-03-12T12:00:00-05:00" 
author: "techknowlogick"
title: "Gitea 1.7.4 is released"
tags: ["release"]
draft: false
---

We are happy to announce version 1.7.4 of Gitea has now been released. This
is a smaller release, with only 4 merged PRs, but it contains an important
security related fix and so we recommend upgrading whenever possible.

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.7.4/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank [Anti Räis](https://bitflipper.eu) for reporting the security issue that have been patched
in this release. Another thank you goes to all of our supporters on
[Open Collective](https://opencollective.com/gitea) who are also helping us
with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Fix potential XSS vulnerability in repository description. ([#6306](https://github.com/go-gitea/gitea/pull/6306)) ([#6308](https://github.com/go-gitea/gitea/pull/6308))
* BUGFIXES
  * Fix wrong release commit id ([#6224](https://github.com/go-gitea/gitea/pull/6300)) ([#6300](https://github.com/go-gitea/gitea/pull/6300))
  * Fix panic on empty signed commits ([#6292](https://github.com/go-gitea/gitea/pull/6292)) ([#6300](https://github.com/go-gitea/gitea/pull/6300))
  * Fix organization dropdown not being scrollable when using mouse wheel ([#5988](https://github.com/go-gitea/gitea/pull/5988)) ([#6246](https://github.com/go-gitea/gitea/pull/6246))
  * Fix displaying dashboard even if required to change password ([#6214](https://github.com/go-gitea/gitea/pull/6214)) ([#6215](https://github.com/go-gitea/gitea/pull/6215))
