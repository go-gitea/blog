---
date: "2018-12-08T12:00:00+03:00"
author: "techknowlogick"
title: "Gitea 1.6.1 is released"
tags: ["release"]
---

We are happy to announce version 1.6.1 of Gitea has now been released. This
is a smaller release, with 7 merged PRs. You can download one of our pre-built
binaries from our [downloads page](https://dl.gitea.io/gitea/1.6.1/) - make
sure to select the correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our supporters on
[Open Collective](https://opencollective.com/gitea) who are also helping us
with financial sustainment.

<!--more-->

## Changelog
* BUGFIXES
  * Fix dependent issue searching when gitea is run in subpath ([#5392](https://github.com/go-gitea/gitea/pull/5392)) ([#5400](https://github.com/go-gitea/gitea/pull/5400))
  * API: '/orgs/:org/repos': return private repos with read access ([#5393](https://github.com/go-gitea/gitea/pull/5393))
  * Fix repository deletion when there is large number of issues in it ([#5426](https://github.com/go-gitea/gitea/pull/5426)) ([#5434](https://github.com/go-gitea/gitea/pull/5434))
  * Word-break the WebHook url to prevent a ui-break ([#5445](https://github.com/go-gitea/gitea/pull/5445))
  * Admin should be able to delete repos via the API even if they are not a member of the organization ([#5443](https://github.com/go-gitea/gitea/pull/5443)) ([#5447](https://github.com/go-gitea/gitea/pull/5447))
  * Ensure that the `closed_at` is set for closed ([#5450](https://github.com/go-gitea/gitea/pull/5450))
  * Fix topic name length on database ([#5493](https://github.com/go-gitea/gitea/pull/5493)) ([#5495](https://github.com/go-gitea/gitea/pull/5495))

