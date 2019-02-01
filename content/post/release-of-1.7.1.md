---
date: "2019-02-01T09:12:00+08:00"
author: "lunny"
title: "Release of 1.7.1"
tags: ["release"]
draft: false
---

We proudly present the minor release of Gitea version 1.7.1. **This release contains some
security fixes so it is highly recommended to update to latest release.**
We have merged 15 pull requests to release this version and built gitea with go1.11.5 to fix [a golang bug](https://github.com/golang/go/issues?q=milestone%3AGo1.11.5+label%3ACherryPickApproved).
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.7.1/),
you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We would like to say special thanks to those who reported security issues or sent patches fixed in this release.

* [Dor Tumarkin, Security Researcher at Checkmarx](https://checkmarx.com/) ([#5907](https://github.com/go-gitea/gitea/pull/5907) and [#5916](https://github.com/go-gitea/gitea/pull/5916))
* [Peter Colberg](https://peter.colberg.org/) ([#5908](https://github.com/go-gitea/gitea/pull/5908))

Another thank you goes to all of our supporters on [Open Collective](https://opencollective.com/gitea)
who are also helping us with financial sustainment.

<!--more-->

## Changelog

* SECURITY
  * Disable redirect for i18n ([#5910](https://github.com/go-gitea/gitea/pull/5910)) ([#5916](https://github.com/go-gitea/gitea/pull/5916))
  * Only allow local login if password is non-empty ([#5906](https://github.com/go-gitea/gitea/pull/5906)) ([#5908](https://github.com/go-gitea/gitea/pull/5908))
  * Fix go-get URL generation ([#5905](https://github.com/go-gitea/gitea/pull/5905)) ([#5907](https://github.com/go-gitea/gitea/pull/5907))
* BUGFIXES
  * Fix TLS errors when using acme/autocert for local connections ([#5820](https://github.com/go-gitea/gitea/pull/5820)) ([#5826](https://github.com/go-gitea/gitea/pull/5826))
  * Request for public keys only if LDAP attribute is set ([#5816](https://github.com/go-gitea/gitea/pull/5816)) ([#5819](https://github.com/go-gitea/gitea/pull/5819))
  * Fix delete correct temp directory ([#5840](https://github.com/go-gitea/gitea/pull/5840)) ([#5839](https://github.com/go-gitea/gitea/pull/5839))
  * Fix an error while adding a dependency via UI ([#5862](https://github.com/go-gitea/gitea/pull/5862)) ([#5876](https://github.com/go-gitea/gitea/pull/5876))
  * Fix null pointer in attempt to Sudo if not logged in ([#5872](https://github.com/go-gitea/gitea/pull/5872)) ([#5884](https://github.com/go-gitea/gitea/pull/5884))
  * When creating new repository fsck option should be enabled ([#5817](https://github.com/go-gitea/gitea/pull/5817)) ([#5885](https://github.com/go-gitea/gitea/pull/5885))
  * Prevent nil dereference in mailIssueCommentToParticipants ([#5891](https://github.com/go-gitea/gitea/pull/5891)) ([#5895](https://github.com/go-gitea/gitea/pull/5895)) ([#5894](https://github.com/go-gitea/gitea/pull/5894))
  * Fix bug when read public repo lfs file ([#5913](https://github.com/go-gitea/gitea/pull/5913)) ([#5912](https://github.com/go-gitea/gitea/pull/5912))
  * Respect value of REQUIRE_SIGNIN_VIEW ([#5901](https://github.com/go-gitea/gitea/pull/5901)) ([#5915](https://github.com/go-gitea/gitea/pull/5915))
  * Fix compare button on upstream repo leading to 404 ([#5877](https://github.com/go-gitea/gitea/pull/5877)) ([#5914](https://github.com/go-gitea/gitea/pull/5914))
* DOCS
  * Added docs for the tree api ([#5835](https://github.com/go-gitea/gitea/pull/5835))
* MISC
  * Include Go toolchain to --version ([#5832](https://github.com/go-gitea/gitea/pull/5832)) ([#5830](https://github.com/go-gitea/gitea/pull/5830))
