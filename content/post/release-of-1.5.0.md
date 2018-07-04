---
date: "2018-07-07T10:00:00+00:00"
author: "techknowlogick"
title: "Gitea 1.5.0 is released"
tags: ["release"]
draft: false
---

We are happy to release version 1.5.0 of Gitea.  We have merged [250 merged pull requests](https://github.com/go-gitea/gitea/milestone/21?closed=1) to release this version.
You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.5.0/), you just need to select the correct platform.
For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).
Thank you to all of our backers on [Open Collective](https://opencollective.com/gitea), you are helping us deliver a better piece of software.

To enhance security we are also signing all of our releases with the following [GPG Key]()

This release includes:
* FIDO U2F to enchance security protections of Gitea accounts
* Topic support for repos 
* Global code search
* Issue features/enhancements: Search for issues via API, multiple assignees for issues, label descriptions and more
* Performance enhancements such as: reducing sql query times, reducing repo indexer disk usage, and Enable caching on assets and avatars.
* UI enhancements: emoji autocomplete, symlink icons, user settings refactor, release page refactor and more

Please see full changelog below for more details.

We would also like to say special thanks to those who reported security issues fixed in this release.

* [@cezar97](https://github.com/cezar97) ([#3878](https://github.com/go-gitea/gitea/pull/3878))

Deprecation notice: In the upcoming major release (1.6.0) we will remove support for Go 1.8 and also embedded tidb.

<!--more-->

## Changelog

* SECURITY
  * Limit uploaded avatar image-size to 4096px x 3072px by default (#4353)
  * Do not allow to reuse TOTP passcode (#3878)
* FEATURE
  * Add cli commands to regen hooks & keys (#3979)
  * Add support for FIDO U2F (#3971)
  * Added user language setting (#3875)
  * LDAP Public SSH Keys synchronization (#1844)
  * Add topic support (#3711)
  * Multiple assignees (#3705)
  * Add protected branch whitelists for merging (#3689)
  * Global code search support (#3664)
  * Add label descriptions (#3662)
  * Add issue search via API (#3612)
  * Add repository setting to enable/disable health checks (#3607)
  * Emoji Autocomplete (#3433)
  * Implements generator cli for secrets (#3531)
* ENHANCEMENT
  * Add more webhooks support and refactor webhook templates directory (#3929)
  * Add new option to allow only OAuth2/OpenID user registration (#3910)
  * Add option to use paged LDAP search when synchronizing users (#3895)
  * Symlink icons (#1416)
  * Improve release page UI (#3693)
  * Add admin dashboard option to run health checks (#3606)
  * Add branch link in branch list (#3576)
  * Reduce sql query times in retrieveFeeds (#3547)
  * Option to enable or disable swagger endpoints (#3502)
  * Add missing licenses (#3497)
  * Reduce repo indexer disk usage (#3452)
  * Enable caching on assets and avatars (#3376)
  * Add repository search ordered by stars/forks. Forks column in admin repo list (#3969)
  * Add Environment Variables to Docker template (#4012)
  * LFS: make HTTP auth period configurable (#4035)
  * Add config path as an optionial flag when changing pass via CLI (#4184)
  * Refactor User Settings sections (#3900)
  * Allow square brackets in external issue patterns (#3408)
  * Add Attachment API (#3478)
  * Add EnableTimetracking option to app settings (#3719)
  * Add config option to enable or disable log executed SQL (#3726)
  * Shows total tracked time in issue and milestone list (#3341)
* TRANSLATION
  * Improve English grammar and consistency (#3614)
* DEPLOYMENT
  * Allow Gitea to run as different USER in Docker (#3961)
  * Provide compressed release binaries (#3991)
  * Sign release binaries (#4188)
