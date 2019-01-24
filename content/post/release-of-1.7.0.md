---
date: "2019-01-24T11:38:00+08:00"
author: "lunny"
title: "Gitea 1.7.0 is released"
tags: ["release"]
draft: false
---

The time has come for another major release! We are proud to present Gitea
1.7.0 to the world. In this release, we merged
[157 pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+milestone%3A1.7.0+is%3Amerged)
-- it's less than last time (178).

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.7.0/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our backers on
[Open Collective](https://opencollective.com/gitea), who are helping us deliver
a better piece of software.

With that out of the way, here's what's new in Gitea version 1.7.0:

<!--more-->

## User action heatmap ([#5131](https://github.com/go-gitea/gitea/pull/5131))

![User action heatmap](/demos/5131/1.png)

Now user's action heatmap will be shown on your first login page and user's profile page.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Show review summary in pull requests ([#5132](https://github.com/go-gitea/gitea/pull/5132))

![Review summary in pull requests](/demos/5132/1.png)

A review summary now will be shown on the bottom of a pull request.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Approvals at Branch Protection ([#5350](https://github.com/go-gitea/gitea/pull/5350))

![approvals limitation](/demos/5350/1.png)

This PR adds approvals limitations to branch protection. A pull request could only be merged after serval approvals.

_Thanks to [**@jonasfranz**](https://github.com/jonasfranz)_

## Milestone issues and pull requests ([#5293](https://github.com/go-gitea/gitea/pull/5293))

![milestone issues and pulls](/demos/5293/1.png)

This PR adds milestone issues and pulls page.

_Thanks to [**@lunny**](https://github.com/lunny)_

## Implement pasting image from clipboard for browsers that supports that ([#5317](https://github.com/go-gitea/gitea/pull/5317))

![pasting image from clipboard](/demos/5317/1.gif)

Implemented pasting image from clipboard in new issue text area or adding issue/pr comments.

_Thanks to [**@lafriks**](https://github.com/lafriks)_

## Create Progressive Web App ([#4730](https://github.com/go-gitea/gitea/pull/4730))

![progressive web app](/demos/4730/1.png)

This will allow users (especially on Android) to add the gitea website to the home-screen and use it like a native app.

_Thanks to [**@SohnyBohny**](https://github.com/SohnyBohny)_

## Give user a link to create PR after push ([#4716](https://github.com/go-gitea/gitea/pull/4716))

When push to a remote non-default branch. It will display a useful link. Output of a push when no active PR exists:

```
[branch2/test be40717] test
 1 file changed, 1 deletion(-)
Counting objects: 3, done.
Writing objects: 100% (3/3), 255 bytes | 255.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a new pull request for 'branch2/test':
remote:   http://localhost:3000/test1/test/compare/master...branch2%2Ftest
remote:
To http://localhost:3000/test1/test.git
   0c5683f..be40717  branch2/test -> branch2/test
```

Output of a push when an active PR exists:

```
[branch2/test 453d638] test
 1 file changed, 1 insertion(+)
Counting objects: 3, done.
Writing objects: 100% (3/3), 255 bytes | 255.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Visit the existing pull request:
remote:   http://localhost:3000/test1/test/pulls/6
remote:
To http://localhost:3000/test1/test.git
   be40717..453d638  branch2/test -> branch2/test
```

_Thanks to [**@JulienTant**](https://github.com/JulienTant)_

## Add rebase with merge commit merge style ([#4052](https://github.com/go-gitea/gitea/pull/4052))

![rebase with merge commit](/demos/4052/1.png)

This PR adds the Rebase and Merge (--no-ff) merge style.

_Thanks to [**@apricote**](https://github.com/apricote)_

## Other changes

* SECURITY
  * Do not display the raw OpenID error in the UI (#5705) (#5712)
  * When redirecting clean the path to avoid redirecting to external site (#5669) (#5679)
  * Prevent DeleteFilePost doing arbitrary deletion (#5631)
* BREAKING
  * Restrict permission check on repositories and fix some problems (#5314)
  * Show only opened milestones on issues page milestone filter (#5051)
* FEATURES
  * Implement git refs API for listing references (branches, tags and other) (#5354)
  * Approvals at Branch Protection (#5350)
  * Add raw blob endpoint to get objects by SHA ID (#5334)
  * Add api for user to create org (#5268)
  * Create AuthorizedKeysCommand (#5236)
  * User action heatmap (#5131)
  * Refactor heatmap to vue component (#5401)
  * Webhook for Pull Request approval/rejection (#5027)
  * Add command for migrating database (#4954)
  * Search keyword by splitting provided values by , (#4939)
  * Give user a link to create PR after push (#4716)
  * Add rebase with merge commit merge style (#3844) (#4052)
* BUGFIXES
  * Disallow empty titles (#5785) (#5794) 
  * Fix sqlite deadlock when assigning to a PR (#5640) (#5642)
  * Don't close issues via commits on non-default branch. (#5622) (#5643)
  * Fix commit page showing status for current default branch (#5650) (#5653)
  * Only count users own actions for heatmap contributions (#5647) (#5655)
  * Update xorm to fix issue postgresql dumping issues (#5680) (#5692)
  * Use correct value for "MSpan Structures Obtained" (#5706) (#5716)
  * Fix bug on modifying sshd username (#5624)
  * Delete tags in mirror which are removed for original repo. (#5609)
  * Fix wrong text getting saved on editing second comment on an issue. (#5608)
  * Fix nil pointer when adding a due date  (#5587)
  * Fix type mismatch of format string (#5574)
  * Fix bug on upload file name (#5571)
  * Issue is not overdue when it is on the same date #5566 (#5568)
  * Fix indexer reindex bug when gitea restart (#5563)
  * Fix table name typo on SQL (#5562)
  * Synchronize SSH keys on login with LDAP + Fix SQLite deadlock on ldap ssh key deletion (#5557)
  * Fix makefile generate buildstep (#5556)
  * Fix nil pointer base branch bug (#5555)
  * Fix permission check on api create org (#5523)
  * Fix detect force push failure on deletion of protected branches (#5522)
  * Fix approvals limitation (#5521)
  * Fix bug when a read perm user to edit his issue (#5516)
  * Fix adding reaction fail for read permission user (#5515)
  * Fixing MSSQL timestamp type (#5511)
  * Fix forgot deletion of notification when delete repository (#5506)
  * Fix empty wiki (#5504)
  * Fix clone wiki failed via ssh (#5503)
  * Fix code review on mssql (#5502)
  * Fix lfs version check warning log when using ssh protocol (#5501)
  * Fix topic name length on database (#5493)
  * Ensure that the `closed_at` is set for closed issues (#5449)
  * Admin should be able to delete repos via the API even if he is not a member of the organization (#5443)
  * Word-Break the WebHook url to prevent a ui-break (#5432)
  * Fix forgot removed records when deleting user (#5429)
  * Fix repository deletion when there is large number of issues in it (#5426)
  * Fix heatmap colors for Chrome/Safari (#5421)
  * Fix password variable shadowing (#5405)
  * Fix dependent issue searching when gitea is run in subpath (#5392)
  * Don't force a password change for the admin user when creating an account via cli (#5391)
  * API: '/orgs/:org/repos': return private repos with read access (#5383)
  * Don't send assign webhooks when creating issue (#5365)
  * Removing Labels via EditPullRequest API (#5348)
  * Migration fixes for gogs (0.11.66) to gitea (1.6.0) #5318 (#5341)
  * Fix bug when users have serval teams with different units on different repositories (#5307)
  * Fix U2F if gitea is configured in subpath (#5302)
  * Fix file edit change preview functionality (#5300)
  * Update gitignore list (#5258)
  * Fixed heatmap not working in mssql (#5248)
  * Fixed wrong api request url for instances running in subfolders (#5247)
  * Fix compatibility heatmap with mysql 8 (#5232)
  * Fix data race on migrate repository (#5224)
  * Fix sqlite and mssql lock (#5214)
  * Fix sqlite lock (#5210)
  * Fix: Accept web-command cli flags if web-command is commited (#5200)
  * Fix: Add secret to all webhook's payload where it has been missing (#5199)
  * Fix race on updatesize (#5190)
  * Fix create team, update team missing units (#5188)
  * Fix sqlite lock (#5184 & #5176)
  * Fix showing pull request link when delete a branch (#5166)
  * Fix JSON result of empty array in heatmap data array (#5154)
  * Update build tags for sqlite_unlock notify (#5144)
  * This commit will reduce join star, repo_topic, topic tables on repo search, so that fix extra columns problem on mssql (#5136)
  * Fix deadlock when sqlite (#5118)
  * Add comment replies (#5104)
  * Fix home page template regression (#5102)
  * Fix regex to support optional end line of old section in diff hunk (#5096)
  * LDAP via simple auth separate bind user and search base (#5055)
  * Fix markdown image with link (#4675)
  * Fix to 3819 - Filtering issues by tags on main screen issues (#3824)
* ENHANCEMENT
  * Delete organization endpoint added (#5601)
  * Update Licenses (#5558)
  * Support reverse proxy providing email (#5554)
  * Add git protocol v2 support via SSH on Docker image (#5520)
  * Add tests for api user orgs (#5494)
  * Allow link verification for services like Mastodon (#5481)
  * Improve team members and repositories settings UI (#5457)
  * Remove the required class from optional ssh port in installation page (#5428)
  * Explicitly disable Git credential helper (#5367)
  * Setting Labels via EditPullRequest API (#5347)
  * Implement pasting image from clipboard for browsers that supports that (#5317)
  * Milestone issues and pull requests (#5293)
  * Support envs on external render commands (#5278)
  * Add option to disable automatic mirror syncing. (#5242)
  * Remove unused db init on commands serv, update, hooks (#5225)
  * Serve audio files using HTML5 audio tag (#5221)
  * Pass link prefixes to external markup parsers (#5201)
  * Add AutoHead functionality. (#5186)
  * Fix emojis not showing in commit messages (#5168)
  * Block registration based on email domain (#5157)
  * Update vendor/go-sqlite3 (#5133 & #5162)
  * Update x/net lib (#5169)
  * Show review summary in pull requests (#5132)
  * Use type switch (#5122)
  * Remove duplicated if bodies (#5121)
  * Remove check for negative length (#5120)
  * Make switch more clear (#5119)
  * Use named const instead of a raw string (#5115)
  * Fix issue where ecdsa and other key types are not synced from LDAP (#5092) (#5094)
  * Refactor: err != nil check, just return error instead (#5093)
  * Add notification interface and refactor UI notifications (#5085)
  * Use APP_NAME on home page (#5048)
  * Explicitly decide whether to  use TLS in mailer's configuration (#5024)
  * Generate random password (#5023)
  * UX of link account (Step 1) (#5006)
  * Make sure argsSet verifies string isn't empty too (#4980)
  * Improve performance of dashboard (#4977)
  * Keys API changes (#4960)
  * Add must-change-password flag to cli for creating a user (#4955)
  * Use native go method to get current user rather than environment variable (#4930)
  * Make gitea serv use api/internal (#4886)
  * Add support for search by uid (#4876)
  * Allow to add organization members as collaborators on organization owned repositories (#4748)
* BUILD
  * Replace lint to revive (#5422)
  * Update golang version in Dockerfile (#5246)
* DOCS
  * Typo in routers/api/v1/org/org.go fixed. (#5598)
  * Update the docs for sqlite_unlock_notify (#5145)
  * CN translation of docs part (#5049)
  * Kubernetes deployment file (#5046)
* MISC
  * Upgrade alpine to 3.8 (#5423)
  * Git-Trees API (#5403)
  * Only chown directories during docker setup if necessary. Fix #4425 (#5064)


To see all user-facing changes that went into the release, check out our
<!-- CHANGEME: change this whenever the full changelog is ready! -->
[full changelog](https://github.com/go-gitea/gitea/blob/master/CHANGELOG.md#170---2019-01-22).

A shoutout goes to those who reported and/or fixed security issues in this
release:

* [@cezar97](https://github.com/cezar97) ([#4973](https://github.com/go-gitea/gitea/issues/4973))
* [@zeripath](https://github.com/zeripath) ([#5705](https://github.com/go-gitea/gitea/pull/5705) [#5669](https://github.com/go-gitea/gitea/pull/5669) [#5631](https://github.com/go-gitea/gitea/pull/5631))
* [@misterpoesy](https://github.com/misterpoesy) ([#5627](https://github.com/go-gitea/gitea/issues/5627))

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

* [@BetaCat0](https://github.com/BetaCat0)
* [@Eisfunke](https://github.com/Eisfunke)
* [@HarshitOnGitHub](https://github.com/HarshitOnGitHub)
* [@HoffmannP](https://github.com/HoffmannP)
* [@JulienTant](https://github.com/JulienTant)
* [@Kasi-R](https://github.com/Kasi-R)
* [@LER0ever](https://github.com/LER0ever)
* [@MoshiBin](https://github.com/MoshiBin)
* [@SagePtr](https://github.com/SagePtr)
* [@SohnyBohny](https://github.com/SohnyBohny)
* [@adelowo](https://github.com/adelowo)
* [@appleboy](https://github.com/appleboy)
* [@apricote](https://github.com/apricote)
* [@bkcsoft](https://github.com/bkcsoft)
* [@cez81](https://github.com/cez81)
* [@chdxD1](https://github.com/chdxD1)
* [@coolaj86](https://github.com/coolaj86)
* [@cristaloleg](https://github.com/cristaloleg)
* [@darktohka](https://github.com/darktohka)
* [@fabian-braun](https://github.com/fabian-braun)
* [@gaydin](https://github.com/gaydin)
* [@gregkare](https://github.com/gregkare)
* [@gzsombor](https://github.com/gzsombor)
* [@inxonic](https://github.com/inxonic)
* [@jamesa](https://github.com/jamesa)
* [@jonasfranz](https://github.com/jonasfranz)
* [@kolaente](https://github.com/kolaente)
* [@koyuawsmbrtn](https://github.com/koyuawsmbrtn)
* [@lafriks](https://github.com/lafriks)
* [@lucienkerl](https://github.com/lucienkerl)
* [@lunny](https://github.com/lunny)
* [@mcnesium](https://github.com/mcnesium)
* [@michaelkuhn](https://github.com/michaelkuhn)
* [@nougad](https://github.com/nougad)
* [@romankl](https://github.com/romankl)
* [@rstefan1](https://github.com/rstefan1)
* [@rvillablanca](https://github.com/rvillablanca)
* [@sapk](https://github.com/sapk)
* [@sd1998](https://github.com/sd1998)
* [@techknowlogick](https://github.com/techknowlogick)
* [@tenacubus](https://github.com/tenacubus)
* [@typeless](https://github.com/typeless)
* [@xor-gate](https://github.com/xor-gate)
* [@zeripath](https://github.com/zeripath)

[PRs](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+milestone%3A1.7.0)
and [issues](https://github.com/go-gitea/gitea/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+milestone%3A1.7.0)
merged in 1.7.0.

# Get in touch

Need help with anything?
You can come on our [Discord server,](https://discord.gg/NsatcWJ) or if you're
more old-fashioned you can also use our [forums](https://discourse.gitea.io/).
