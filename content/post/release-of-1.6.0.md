---
date: "2018-11-22T21:23:00+08:00"
author: "lunny"
title: "Gitea 1.6.0 is released"
tags: ["release"]
---

The time has come for another major release! We are proudly to present Gitea
1.6.0 to the world. In this release, we merged
[178 pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.6.0+is%3Amerged)
-- it's less than last time (258).

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.6.0/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our backers on
[Open Collective](https://opencollective.com/gitea), who are helping us deliver
a better piece of software.

With that out of the way, here's what's new in 1.6.0:

<!--more-->

## Code Review and Approval ([#3748](https://github.com/go-gitea/gitea/pull/3748))

![Code Review demo](/demos/3748/1.gif)

You can now review the code on pull requests and place comments on the code lines. You can also approve or reject the pull requests.

_Thanks to [**@JonasFranzDEV**](https://github.com/JonasFranzDEV) and [**@lafriks**](https://github.com/lafriks)_

## Issue Dependencies ([#2531](https://github.com/go-gitea/gitea/pull/2531))

![Issue Dependencies](/demos/2531/1.png)

You can add dependencies for issues, if an issue is blocked by another it can not be closed until all block issues are closed.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Theme Support and Dark Theme ([#4198](https://github.com/go-gitea/gitea/pull/4198))

![Theme Support](/demos/4198/1.png)

Gitea deprecated third-party theme to add the ability to have built in themes in Gitea and provide dark theme arc-green.

_Thanks to [**@techknowlogick**](https://github.com/techknowlogick)_

## CSV Render ([#4105](https://github.com/go-gitea/gitea/pull/4105))

![CSV Render](/demos/4105/1.png)

CSV files are now also rendered as table.

_Thanks to [**@lunny**](https://github.com/lunny)_

## Add sudo functionality to the API ([#4809](https://github.com/go-gitea/gitea/pull/4809))

Now administrator users could sudo as other user to call API as that user. It similar to [https://docs.gitlab.com/ee/api/#sudo](https://docs.gitlab.com/ee/api/#sudo) 

_Thanks to [**@zeripath**](https://github.com/zeripath)_

## Gitea command line adds oauth commands ([#4591](https://github.com/go-gitea/gitea/pull/4591))

You can manage OAuth2 providers via command line. See [https://docs.gitea.io/en-us/command-line](https://docs.gitea.io/en-us/command-line)

_Thanks to [**@techknowlogick**](https://github.com/techknowlogick)_

## Do not allow merging of a WIP Pull requests ([#4529](https://github.com/go-gitea/gitea/pull/4529))

![WIP Pull Request demo](/demos/4529/1.png)

When the title of the pull requests starts with [wip] or wip: or prefix configured on app.ini, the pull request cannot be merged by anyone until prefix is removed.

_Thanks to [**@JulienTant**](https://github.com/JulienTant)_

## Force user to change password ([#4489](https://github.com/go-gitea/gitea/pull/4489))

When an account was created by administrator, it can now be forced to change password after authorization.

_Thanks to [**@adelowo**](https://github.com/adelowo)_

## Add letsencrypt to Gitea ([#4189](https://github.com/go-gitea/gitea/pull/4189))

It is now possibe to enable automatic Let's Encrypt certificates for easier HTTPS configuration.

_Thanks to [**@Fluf**](fluf@warpmail.net)_

## Add push webhook support for mirrored repositories ([#4127](https://github.com/go-gitea/gitea/pull/4127))

Now push webhook of mirrored repositories will be fired.

_Thanks to [**@lafriks**](https://github.com/lafriks)_

## Add Recaptcha functionality to Gitea ([#4044](https://github.com/go-gitea/gitea/pull/4044))

![Recaptcha demo](/demos/4044/1.png)

You can enable recaptcha when registering in Gitea.

_Thanks to [**@Fluf**](fluf@warpmail.net)_

## Other changes

* BREAKING
  * Respect email privacy option in user search via API (#4512)
  * Simply remove embedded tidb and deps (#3993)
  * Swagger.v1.json template (#3572)

* BUGFIXES
  * dont' send assign webhooks when creating issue (#5365)
  * Fix create team, update team missing units (#5188)
  * Fix file edit change preview functionality (#5300)
  * *ix bug when users have serval teams with different units on different repositories (#5307)
  * Fix U2F if gitea is configured in subpath (#5302)
  * Fix markdown image with link (#4675)
  * Remove maxlines option for file logger (#5282)
  * Fix wrong api request url for instances running in subfolders (#5261) (#5247)
  * Accept web-command cli flags if web-command is commited (#5245) (#5200)
  * Reduce join star, repo_topic, topic tables on repo search, to resolve extra columns problem on MSSQL (#5136) (#5229)
  * Fix data race on migrate repository (#5224) (#5230)
  * Add secret to all webhook's payload where it has been missing (#5208) (#5199)
  * Fix sqlite and MSSQL lock (#5210) (#5223) (#5214) (#5218) (#5176) (#5179)
  * Fix race on updatesize (#5190) (#5215)
  * Fix filtering issues by tags on main screen issues (#5219) (#3824)
  * Fix SQL quoting (#5137) (#5117)
  * Fix regex to support optional end line of old section in diff hunk (#5097) (#5096)
  * Fix release creation via API (#5076)
  * Remove links from topics in edit mode  (#5026)
  * Fix missing AppSubUrl in few more templates (fixup) (#5020 #5021)
  * Disable debug routes unless PPROF is enabled in configuration (#4995)
  * Fix user menu item styling (#4985)
  * Fix layout of the topics editing form (#4971)
  * Fix null pointer dereference in ParseCommitWithSignature (#4962)
  * Fix url in discord webhook (#4953)
  * Detect charset and convert non UTF-8 files for display (#4950)
  * Make sure to catch the right error so it is displayed on the UI (#4945)
  * Fix(topics): don't redirect to explore page. (#4938)
  * Fix bug forget to remove Stopwatch when remove repository (#4928)
  * Fix bug when repo remained bare if multiple branches pushed in single push (#4923)
  * Fix: Crippled diff (#4726) (#4900)
  * Fix trimming of markup section names (#4863)
  * Issues api allow pulls and fix #4832 (#4852)
  * Do not autocreate directory for new users/orgs (#4828) (#4849)
  * Fix redirect with non-ascii branch names (#4764) (#4810)
  * Fix missing release title in webhook (#4783) (#4796)
  * Make sure to reset commit count in the cache on mirror syncing (#4720)
  * Fixed bug where team with admin privelege type doesn't get any unit  (#4719)
  * Fix incorrect caption of webhook setting (#4701) (#4717)
  * Hide org/create menu item in Dashboard if user has no rights (#4678) (#4680)
  * Site admin could create repos even MAX_CREATION_LIMIT=0 (#4645)
  * Fix custom templates being ignored (#4638)
  * Fix starring icon after semantic ui update (#4628)
  * Fix Split-View line adjustment (#4622)
  * Fix integer constant overflows in tests (#4616)
  * Push whitelist now doesn't apply to branch deletion (#4601) (#4607)
  * Fix bugs when too many IN variables (#4594)
  * Fix failure on creating pull request with assignees (#4419) (#4583)
  * Fix panic issue on update avatar email (#4580) (#4581)
  * Fix status code label for a successful webhook (#4540)
  * An inactive user shouldn't be able to be added as a collaborator (#4535)
  * Don't fail silently if trying to add a collaborator twice (#4533)
  * Fix incorrect MergeWhitelistTeamIDs check in CanUserMerge function (#4519) (#4525)
  * Fix out-of-transaction query in removeOrgUser (#4521) (#4522)
  * Fix migration from older releases (#4495)
  * Accept 'Data:' in commit graph (#4487)
  * Update xorm to latest version and fix correct `user` table referencing in sql (#4473)
  * Relative URLs for LibreJS page (#4460)
  * Redirect to correct page after using scratch token (#4458)
  * Fix column droping for MSSQL that need new transaction for that (#4440)
  * Replace src with raw to fix image paths (#4377)
  * Add default merge options when creating new repository (#4369)
  * Fix docker build (#4358)
  * Fixes repo membership check in API (#4341)
  * Fix some issues with special chars in branch names (#3767)
  * Responsive design fixes (#4508)
  * Fix milestones sorted wrongly (#4987)
* ENHANCEMENT
  * Allow api to create tags for releases if they don't exist (#4890)
  * Fix #4877 to follow the OpenID Connect Audiences spec (#4878)
  * Enforce token on api routes [fixed critical security issue #4357] (#4840)
  * Update legacy branch and tag URLs in dashboard to new format (#4812)
  * Slack webhook channel name cannot be empty or just contain an hashtag (#4786)
  * Add whitespace handling to PR-comparsion (#4683)
  * Make reverse proxy auth optional (#4643)
  * MySQL TLS support(#4642)
  * Make sure to set PR split view when creating/previewing a pull request  (#4617)
  * Log user in after a successful sign up (#4615)
  * Update jQuery to v1.12.4 (#4551)
  * Env var GITEA_PUSHER_EMAIL (#4516)
  * Feat(repo): support search repository by topic name (#4505)
  * Small improvements to dependency UI (#4503)
  * Make max commits in graph configurable (#4498)
  * Add valid for lfs oid (#4461)
  * Add shortcut to save wiki page (#4452)
  * Allow administrator to create repository for any organization (#4368)
  * Fix repository last updated time update when delete a user who watched the repo (#4363)
  * Switch plaintext scratch tokens to use hash instead (#4331)
  * Increase default TOTP secret size to 320 bits (#4287)
  * Keep preseeded database password (#4284)
  * Implemented hover text showing user FullName (#4261)
  * Add ability to delete a token (#4235)
  * Fix typos in i18n variable names. (#4080)
  * Api: repos/search: add parameters to control the sort order (#3964)
  * Add missing path in the Docker app.ini template (#2181)
  * Add file name and branch to page title (#4902)
  * Offline use of google fonts (#4872)
  * Add missing History link to directory listings v2 (#4829)
  * Locale for Edit and Remove due date issue (#4802)
  * Disable 'May Import Local Repository' when is disabled by setting (Is… (#4780)
  * API /admin/users/{username} missing parameter (#4775)
  * Display error when adding a user to a team twice (#4746)
  * Remove UsePrivilegeSeparation from the Docker sshd_config, see #2876 (#4722)
  * Focus title input when clicking helper link (#4696)
  * Add vendor to user reserved words and format words list according alphabet (#4685)
  * Add gitea/issues link to 500 page (#4654)
  * Hide home button when landing page is not set to home (#4651)
  * Remove link to GitHub issues in 404 template (#4639)
  * Cmd/serve: pprof cpu and memory profile dumps to disk (#4560)
  * Add flash message after an account has been successfully activated (#4510)
  * Prevent html entity escaping on delete branch (#4471)
  * Locale for button Edit on protected branch (#4442)
  * Update notification icon (#4343)
  * Added front-end topics validation (#4316)
  * Don't display buttons if there are no system notifications (#4280)
  * Issue due date api (#3890)
* SECURITY
  * Improve URL validation for external wiki  and external issues (#4710)
  * Make cookies HttpOnly and obey COOKIE_SECURE flag (#4706)
  * Don't disclose emails of all users when sending out emails (#4664)
  * Check that repositories can only be migrated to own user or organizations (#4366)


To see all user-facing changes that went into the release, check out our
<!-- CHANGEME: change this whenever the full changelog is ready! -->
[full changelog](https://github.com/go-gitea/gitea/blob/master/CHANGELOG.md#140---2018-11-22).

A shoutout goes to those who reported and/or fixed security issues in this
release:

* [@cezar97](https://github.com/cezar97) ([#3878](https://github.com/go-gitea/gitea/pull/3878))

**Deprecation notice:** in this release we are dropping
support for Go 1.8 and also embedded TiDB.

# Help us out!

Gitea is focused on community input and contributions. To keep a project like
Gitea going we need people. **_LOTS_** of people. You can help in the
following areas:

## Programming

If you know Go or HTML/CSS/JavaScript, you may be interested in working on the
code. Working on OSS may seem scary, but the best way is to try! Read the
[Gitea contribution guide](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md),
and then [find an itch to scratch](https://github.com/go-gitea/gitea/issues),
or scratch your own!

## Translating

Want to translate Gitea in your own language? Awesome! Join the Gitea project
on [Crowdin](https://crowdin.com/project/gitea). As soon as your translation is
approved, it will be pushed to the Gitea project to be used in future releases!

## Documentation

Documentation is important, but also time consuming. If you enjoy writing and
have a pretty good knowledge of English, or you would like to translate the
English version to your native language, you're very welcome to do so. Find our
documentation on the main git repository
[here](https://github.com/go-gitea/gitea/tree/master/docs). Just fork, update
the documentation and then create a pull request!

## Support

Do you like people? Can you give calm and thought-out responses to users needing
help? Then you can spend some time providing support to those who need it. Most
answers can really be found in the documentation, so make sure to take some time
to read it. Then, either join our chat or forums (linked below), or simply
help us sort out issues and answer questions on the
[Gitea repository](https://github.com/go-gitea/gitea/issues).

## Donations

If you, or your company, want to help us out sustain our financial expenses, you
can do so by donating on [Open Collective](https://opencollective.com/gitea#).

<a href="https://opencollective.com/gitea#backers" target="_blank"><img src="https://opencollective.com/gitea/backers.svg?width=890"></a>

<a href="https://opencollective.com/gitea/sponsor/0/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/1/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/2/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/3/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/4/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/5/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/6/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/7/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/8/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/gitea/sponsor/9/website" target="_blank"><img src="https://opencollective.com/gitea/sponsor/9/avatar.svg"></a>

## … or reporting bugs

If you lack the time or knowledge to do any of the above, just using Gitea and sharing the word is enough to make us happy! One thing you can always do is to report any bugs you find on the [Gitea issue tracker](https://github.com/go-gitea/gitea/issues).

Before opening an issue, read the [contribution guidelines about reporting bugs](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md#bug-reports). After opening an issue, try to stick around a while to answer any questions we might have. Replies greatly help us find the root cause of an issue.

# Thanks

This release would not have been possible without the pull requests from the following people:

* [@0rzech](https://github.com/0rzech)
* [@Bobonium](https://github.com/Bobonium)
* [@Eisfunke](https://github.com/Eisfunke)
* [@EnricoFerro](https://github.com/EnricoFerro)
* [@HoffmannP](https://github.com/HoffmannP)
* [@JonasFranzDEV](https://github.com/JonasFranzDEV)
* [@JulienTant](https://github.com/JulienTant)
* [@OvermindDL1](https://github.com/OvermindDL1)
* [@Pofilo](https://github.com/Pofilo)
* [@SagePtr](https://github.com/SagePtr)
* [@adelowo](https://github.com/adelowo)
* [@appleboy](https://github.com/appleboy)
* [@aswild](https://github.com/aswild)
* [@aunger](https://github.com/aunger)
* [@axifive](https://github.com/axifive)
* [@beeonthego](https://github.com/beeonthego)
* [@bkcsoft](https://github.com/bkcsoft)
* [@bkroll](https://github.com/bkroll)
* [@bugreport0](https://github.com/bugreport0)
* [@clarcharr](https://github.com/clarcharr)
* [@cleverer](https://github.com/cleverer)
* [@decke](https://github.com/decke)
* [@deoren](https://github.com/deoren)
* [@drewbowering](https://github.com/drewbowering)
* [@esno](https://github.com/esno)
* [@fangdingjun](https://github.com/fangdingjun)
* [@filipnavara](https://github.com/filipnavara)
* [@gdiepen](https://github.com/gdiepen)
* [@ghost](https://github.com/ghost)
* [@kjellkvinge](https://github.com/kjellkvinge)
* [@kolaente](https://github.com/kolaente)
* [@kzmi](https://github.com/kzmi)
* [@lafriks](https://github.com/lafriks)
* [@linweijie2012](https://github.com/linweijie2012)
* [@lukasbestle](https://github.com/lukasbestle)
* [@lunny](https://github.com/lunny)
* [@menschel-d](https://github.com/menschel-d)
* [@michaelkuhn](https://github.com/michaelkuhn)
* [@mqudsi](https://github.com/mqudsi)
* [@mrichar1](https://github.com/mrichar1)
* [@nemoinho](https://github.com/nemoinho)
* [@nidrissi](https://github.com/nidrissi)
* [@nougad](https://github.com/nougad)
* [@nubenum](https://github.com/nubenum)
* [@rvillablanca](https://github.com/rvillablanca)
* [@sapk](https://github.com/sapk)
* [@silverwind](https://github.com/silverwind)
* [@tarelda](https://github.com/tarelda)
* [@techknowlogick](https://github.com/techknowlogick)
* [@theasp](https://github.com/theasp)
* [@treyerl](https://github.com/treyerl)
* [@twang2218](https://github.com/twang2218)
* [@typeless](https://github.com/typeless)
* [@ucodi](https://github.com/ucodi)
* [@webjoel](https://github.com/webjoel)
* [@xor-gate](https://github.com/xor-gate)
* [@xxxtonixxx](https://github.com/xxxtonixxx)
* [@yan12125](https://github.com/yan12125)
* [@zeripath](https://github.com/zeripath)

[PRs](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+milestone%3A1.6.0)
and [issues](https://github.com/go-gitea/gitea/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+milestone%3A1.6.0)
merged in 1.6.0.

# Get in touch

Need help with anything?
You can come on our [Discord server,](https://discord.gg/NsatcWJ) or if you're
more old-fashioned you can also use our [forums](https://discourse.gitea.io/).
