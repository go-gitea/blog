---
date: "2017-03-09T20:15:00+01:00"
author: "tboerger"
title: "Release of 1.1.0"
tags: ["release"]
draft: false
---

We proudly present the release of Gitea version 1.1.0. We have closed [126](https://github.com/go-gitea/gitea/issues?q=is%3Aissue+is%3Aclosed+milestone%3A1.1.0) issues and we also merged [348](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Amerged%20milestone%3A1.1.0) pull requests to release this version of Gitea. You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.1.0/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BREAKING
  * The SSH keys can potentially break, make sure to regenerate the authorized keys
* FEATURE
  * Git LFSv2 support [#122](https://github.com/go-gitea/gitea/pull/122)
  * API endpoints for repo watching [#191](https://github.com/go-gitea/gitea/pull/191)
  * Search within private repos [#222](https://github.com/go-gitea/gitea/pull/222)
  * Hide user email address on explore page [#336](https://github.com/go-gitea/gitea/pull/336)
  * Protected branch system [#339](https://github.com/go-gitea/gitea/pull/339)
  * Sendmail for mail delivery [#355](https://github.com/go-gitea/gitea/pull/355)
  * API endpoints for org webhooks [#372](https://github.com/go-gitea/gitea/pull/372)
  * Enabled MSSQL support [#383](https://github.com/go-gitea/gitea/pull/383)
  * API endpoints for org teams [#370](https://github.com/go-gitea/gitea/pull/370)
  * API endpoints for collaborators [#375](https://github.com/go-gitea/gitea/pull/375)
  * Graceful server restart [#416](https://github.com/go-gitea/gitea/pull/416)
  * Commitgraph / timeline on commits page [#428](https://github.com/go-gitea/gitea/pull/428)
  * API endpoints for repo forks [#509](https://github.com/go-gitea/gitea/pull/509)
  * API endpoints for releases [#510](https://github.com/go-gitea/gitea/pull/510)
  * Folder jumping [#511](https://github.com/go-gitea/gitea/pull/511)
  * Stars tab on profile page [#519](https://github.com/go-gitea/gitea/pull/519)
  * Notification system [#523](https://github.com/go-gitea/gitea/pull/523)
  * Push and pull through reverse proxy basic auth [#524](https://github.com/go-gitea/gitea/pull/524)
  * Search for issues and pull requests [#530](https://github.com/go-gitea/gitea/pull/530)
  * API endpoint for stargazers [#597](https://github.com/go-gitea/gitea/pull/597)
  * API endpoints for subscribers [#598](https://github.com/go-gitea/gitea/pull/598)
  * PID file support [#610](https://github.com/go-gitea/gitea/pull/610)
  * Two factor authentication (2FA) [#630](https://github.com/go-gitea/gitea/pull/630)
  * API endpoints for org users [#645](https://github.com/go-gitea/gitea/pull/645)
  * Release attachments [#673](https://github.com/go-gitea/gitea/pull/673)
  * OAuth2 consumer [#679](https://github.com/go-gitea/gitea/pull/679)
  * Add ability to fork your own repos [#761](https://github.com/go-gitea/gitea/pull/761)
  * Search repository on dashboard [#773](https://github.com/go-gitea/gitea/pull/773)
  * Search bar on user profile [#787](https://github.com/go-gitea/gitea/pull/787)
  * Track label changes on issue view [#788](https://github.com/go-gitea/gitea/pull/788)
  * Allow using custom time format [#798](https://github.com/go-gitea/gitea/pull/798)
  * Redirects for renamed repos [#807](https://github.com/go-gitea/gitea/pull/807)
  * Track assignee changes on issue view [#808](https://github.com/go-gitea/gitea/pull/808)
  * Track title changes on issue view [#841](https://github.com/go-gitea/gitea/pull/841)
  * Archive cleanup action [#885](https://github.com/go-gitea/gitea/pull/885)
  * Basic Open Graph support [#901](https://github.com/go-gitea/gitea/pull/901)
  * Take back control of Git hooks [#1006](https://github.com/go-gitea/gitea/pull/1006)
  * API endpoints for user repos [#1059](https://github.com/go-gitea/gitea/pull/1059)
* BUGFIXES
  * Fixed counting issues for issue filters [#413](https://github.com/go-gitea/gitea/pull/413)
  * Added back default settings for SSH [#500](https://github.com/go-gitea/gitea/pull/500)
  * Fixed repo permissions [#513](https://github.com/go-gitea/gitea/pull/513)
  * Issues cannot be created with labels [#622](https://github.com/go-gitea/gitea/pull/622)
  * Add a reserved wiki paths check to the wiki [#720](https://github.com/go-gitea/gitea/pull/720)
  * Update website binding MaxSize to 255 [#722](https://github.com/go-gitea/gitea/pull/722)
  * User can see the private activity on public history [#818](https://github.com/go-gitea/gitea/pull/818)
  * Wrong pages number which includes private repositories [#844](https://github.com/go-gitea/gitea/pull/844)
  * Trim whitespaces for search keyword [#893](https://github.com/go-gitea/gitea/pull/893)
  * Don't rewrite non-gitea public keys [#906](https://github.com/go-gitea/gitea/pull/906)
  * Use fingerprint to check instead content for public key [#911](https://github.com/go-gitea/gitea/pull/911)
  * Fix random avatars [#1147](https://github.com/go-gitea/gitea/pull/1147)
* ENHANCEMENT
  * Refactored process manager [#75](https://github.com/go-gitea/gitea/pull/75)
  * Restrict rights to create new orgs [#193](https://github.com/go-gitea/gitea/pull/193)
  * Added label and milestone sorting [#199](https://github.com/go-gitea/gitea/pull/199)
  * Make minimum password length configurable [#223](https://github.com/go-gitea/gitea/pull/223)
  * Speedup conflict checking on pull requests [#276](https://github.com/go-gitea/gitea/pull/276)
  * Added button to delete merged pull request branches [#441](https://github.com/go-gitea/gitea/pull/441)
  * Improved issue references within markdown [#471](https://github.com/go-gitea/gitea/pull/471)
  * Dutch translation for the landingpage [#487](https://github.com/go-gitea/gitea/pull/487)
  * Added Gogs migration script [#532](https://github.com/go-gitea/gitea/pull/532)
  * Support a .gitea folder for issue templates [#582](https://github.com/go-gitea/gitea/pull/582)
  * Enhanced diff-view coloring [#584](https://github.com/go-gitea/gitea/pull/584)
  * Added ETag header to avatars [#721](https://github.com/go-gitea/gitea/pull/721)
  * Added option to config to disable local path imports [#724](https://github.com/go-gitea/gitea/pull/724)
  * Allow custom public files [#782](https://github.com/go-gitea/gitea/pull/782)
  * Added pprof endpoint for debugging [#801](https://github.com/go-gitea/gitea/pull/801)
  * Added X-GitHub-* headers [#809](https://github.com/go-gitea/gitea/pull/809)
  * Fill SSH key title automatically [#863](https://github.com/go-gitea/gitea/pull/863)
  * Display Git version on admin panel [#921](https://github.com/go-gitea/gitea/pull/921)
  * Expose URL field on issue API [#982](https://github.com/go-gitea/gitea/pull/982)
  * Statically compile the binaries [#985](https://github.com/go-gitea/gitea/pull/985)
  * Embed build tags into version string [#1051](https://github.com/go-gitea/gitea/pull/1051)
  * Gitignore support for FSharp and Clojure [#1072](https://github.com/go-gitea/gitea/pull/1072)
  * Custom templates for static builds [#1087](https://github.com/go-gitea/gitea/pull/1087)
  * Add ProxyFromEnvironment if none set [#1096](https://github.com/go-gitea/gitea/pull/1096)
* MISC
  * Replaced remaining Gogs references
  * Added more tests on various packages
  * Use Crowdin for translations again
  * Resolved some XSS attack vectors
  * Optimized and reduced number of database queries
