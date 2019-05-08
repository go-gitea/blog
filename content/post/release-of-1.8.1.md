---
date: "2019-05-08T10:50:00+01:00" 
author: "jolheiser"
title: "Gitea 1.8.1 is released"
tags: ["release"]
draft: false
---

We are proud to present the release of Gitea version 1.8.1. 

We have merged [24](https://github.com/go-gitea/gitea/pulls?q=is%3Apr+milestone%3A1.8.1+is%3Aclosed) pull requests to release this version. 

You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.8.1/) - make sure to select the correct platform! For further details on how to install, follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our supporters on [Open Collective](https://opencollective.com/gitea) who are helping us with financial sustainment.

<!--more-->

## Changelog

* BUGFIXES
  * Fix 404 when sending pull requests in some situations ([#6871](https://github.com/go-gitea/gitea/pull/6871)) ([#6873](https://github.com/go-gitea/gitea/pull/6873))
  * Enforce osusergo build tag for releases ([#6862](https://github.com/go-gitea/gitea/pull/6862)) ([#6869](https://github.com/go-gitea/gitea/pull/6869))
  * Don't post process commit summary in templates ([#6842](https://github.com/go-gitea/gitea/pull/6842)) ([#6868](https://github.com/go-gitea/gitea/pull/6868))
  * Fix 500 when reviewer is deleted ([#6856](https://github.com/go-gitea/gitea/pull/6856)) ([#6860](https://github.com/go-gitea/gitea/pull/6860))
  * Fix v78 migration for MSSQL ([#6823](https://github.com/go-gitea/gitea/pull/6823)) ([#6854](https://github.com/go-gitea/gitea/pull/6854))
  * Added tags pull step to drone config to show correct version hashes ([#6836](https://github.com/go-gitea/gitea/pull/6836)) ([#6839](https://github.com/go-gitea/gitea/pull/6839))
  * Fix double-generation of scratch token ([#6833](https://github.com/go-gitea/gitea/pull/6833)) ([#6835](https://github.com/go-gitea/gitea/pull/6835))
  * When mirroring we should set the remote to mirror ([#6824](https://github.com/go-gitea/gitea/pull/6824)) ([#6834](https://github.com/go-gitea/gitea/pull/6834))
  * Show scrollbar only when needed ([#6802](https://github.com/go-gitea/gitea/pull/6802)) ([#6803](https://github.com/go-gitea/gitea/pull/6803))
  * Service worker js is missing a comma ([#6788](https://github.com/go-gitea/gitea/pull/6788)) ([#6795](https://github.com/go-gitea/gitea/pull/6795))
  * Set user search base field optional in LDAP (simple auth) edit page ([#6779](https://github.com/go-gitea/gitea/pull/6779)) ([#6789](https://github.com/go-gitea/gitea/pull/6789))
  * Fix team edit API panic ([#6780](https://github.com/go-gitea/gitea/pull/6780)) ([#6785](https://github.com/go-gitea/gitea/pull/6785))
  * Minor CSS cleanup for the navbar ([#6553](https://github.com/go-gitea/gitea/pull/6553)) ([#6781](https://github.com/go-gitea/gitea/pull/6781))
  * Stricter domain name pattern in email regex ([#6739](https://github.com/go-gitea/gitea/pull/6739)) ([#6768](https://github.com/go-gitea/gitea/pull/6768))
  * Detect and restore encoding and BOM in content ([#6727](https://github.com/go-gitea/gitea/pull/6727)) ([#6765](https://github.com/go-gitea/gitea/pull/6765))
  * Fix org visibility bug when git cloning ([#6743](https://github.com/go-gitea/gitea/pull/6743)) ([#6762](https://github.com/go-gitea/gitea/pull/6762))
  * OAuth2 token can be used in basic auth ([#6747](https://github.com/go-gitea/gitea/pull/6747)) ([#6761](https://github.com/go-gitea/gitea/pull/6761))
  * Fix missing return ([#6751](https://github.com/go-gitea/gitea/pull/6751)) ([#6756](https://github.com/go-gitea/gitea/pull/6756))
  * Fix sorting repos on org home page with non-admin login ([#6741](https://github.com/go-gitea/gitea/pull/6741)) ([#6746](https://github.com/go-gitea/gitea/pull/6746))
  * Drop is_bare IDX only when it exists for MySQL and MariaDB ([#6736](https://github.com/go-gitea/gitea/pull/6736)) ([#6744](https://github.com/go-gitea/gitea/pull/6744))
  * Fix team members API ([#6714](https://github.com/go-gitea/gitea/pull/6714)) ([#6729](https://github.com/go-gitea/gitea/pull/6729))
  * Load issue attributes when editing an issue with API ([#6723](https://github.com/go-gitea/gitea/pull/6723)) ([#6725](https://github.com/go-gitea/gitea/pull/6725))
  * Fix config ui error about cache ttl ([#6861](https://github.com/go-gitea/gitea/pull/6861)) ([#6865](https://github.com/go-gitea/gitea/pull/6865))
