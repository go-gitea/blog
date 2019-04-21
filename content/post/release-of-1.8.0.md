---
date: "2019-04-21T10:40:00+01:00" 
author: "zeripath"
title: "Gitea 1.8.0 is released"
tags: ["release"]
draft: false
---

The time has come for another major release! We are proud to present Gitea
1.8.0 to the world. **This release contains two new security fixes which cannot be backported to the 1.7.0 branch, so it is recommended to update to this version.**
In this release, we merged
[245 pull requests](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is:pr+milestone:1.8.0+is:merged)
-- This is more than 1.7.0 (157) and 1.6.0 (178).

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.8.0/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our backers on
[Open Collective](https://opencollective.com/gitea), who are helping us deliver
a better piece of software.

With that out of the way, here's what's new in Gitea version 1.8.0:

<!--more-->

## OAuth2 Provider [#5378](https://github.com/go-gitea/gitea/pull/5378)

Gitea is now an OAuth2 Provider. This fixes and closes issue [#27](https://github.com/go-gitea/gitea/issues/27)!

_Thanks to [**@jonasfranz**](https://github.com/jonasfranz)_

## Repositories can now be archived [#5009](https://github.com/go-gitea/gitea/pull/5009)

Repositories in Gitea can now be archived. This prevents the creation of new issues,
pull-requests or pushing to the git repository.

_Thanks to [**@kolaente**](https://github.com/kolaente)_

## Private and Internal Organizations [#1763](https://github.com/go-gitea/gitea/pull/1763)

Organizations can now be set to be Public, Internal or Private. Repositories created in
internal organizations will only be visible to logged-in users. Private organizations will
only be visible to those who are members.

_Thanks to [**@techknowlogick**](https://github.com/techknowlogick) &amp; [**@DblK**](https://github.com/dblk)_

## Changelog

* SECURITY
  * Prevent remote code execution vulnerability with mirror repo URL settings (#6593) (#6594)
  * Resolve 2FA bypass on API (#6676) (#6674)
  * Prevent the creation of empty sessions for non-logged in users (#6690) (#6677)
* BREAKING
  * Add "ghost" and "notifications" to list of reserved user names. (#6208)
  * Change sqlite DB path default to data directory (#6198)
  * Adds MustChangePassword to user create/edit API (#6193)
  * Disable redirect for i18n (#5910)
  * Releases API paging (#5831)
  * Allow Macaron to be set to log through to gitea.log (#5667)
  * Don't close issues via commits on non-default branch (#5622)
* FEATURE
  * Add regenerate secret feature for oauth2 (#6291)
  * Expose issue stopwatch toggling via API (#5970)
  * Add other session providers (#5963)
  * Pull request conflict files detection (#5951)
  * Integrate OAuth2 Provider (#5378)
  * Implement "conversation lock" for issue comments (#5073)
  * Feature: Archive repos (#5009)
  * Discord Oauth2 support (#4476)
  * Allow to set organization visibility (public, internal, private) (#1763)
  * Added URL mapping for Release attachments like on github.com (#1707)
* ENHANCEMENT
  * Add support for client basic auth for exchanging access tokens (#6293)
  * Add ability to sort issues by due date (#6206) (#6244)
  * Style tweaks to issue selection (#6196)
  * Increase Username and Orgname MaxSize 35 -> 40 (#6178)
  * Coverage profile with multiple packages (#6167)
  * Split setting.go to multiple files (#6154)
  * Allow labels to contain emoji (#6063)
  * Disable git fsck for mirrored repos by default (#6018)
  * Add default time out for git operations (#6015)
  * Make dashboard navbar and footer full-width (#6013)
  * Add lang specific font stacks for CJK (#6007)
  * Fix header menu misalignment (#6002)
  * Enhance closed PR and Issue status in the list (#6000)
  * Make navbar full width (#5998)
  * Add option to close issues via commit on a non master branch (#5992)
  * Support n as a line highlight prefix (#5987)
  * Search for org repos (#3031) (#5986)
  * Minor UI tweaks (#5980)
  * Use native golang SSH library but ssh-keygen when enable built-in SSH server to remove dependent on that command lines (#5976)
  * Dashboard tweaks (#5974)
  * Fixes for repo topic editor (#5971)
  * Display the branch name in the commit view (#5950)
  * handle milestone events for issues and PR (#5947)
  * Add label names as filter in issue search api (#5946)
  * Repo header tweaks (#5945)
  * Better support for long repo names (#5932)
  * Fix wrapping long code lines (#5927)
  * Change GPG Validation colors and remove inline CSS (#5404) (#5896)
  * Fix "pulls.blocked_by_approvals" text (#5879)
  * Rename reject to 'request changes' (#5858)
  * Move input fields to add members to a team and repos to a team (#5853)
  * Config option to disable automatic repo watching (#5852)
  * New Issue ?body= query (#5851)
  * Add API to list tags (#5850)
  * Pagination for git tree API (#5838)
  * Add InternalTokenURI to load InternalToken from an external file (#5812)
  * Allow markdown files to read from the LFS (#5787)
  * Add the ability to use multiple labels as filters (#5786)
  * Adjust log settings when a user is not found. (#5771)
  * Log IP of failed ssh connection (#5766)
  * Moved defaults in defaults.go to setting.go (#5764)
  * Make DB connect more robust (#5738)
  * Add Default Pull Request Title (#5735)
  * Refactor repo.isBare to repo.isEmpty #5629 (#5714)
  * Add flag to skip repository dumping (#5695)
  * Prioritize "readme.md" (#5691)
  * Improve "Fork button" for guests by showing a pop up asking them to log in before forking (#5690)
  * Allow for user specific themes (#5668)
  * Display branch name in delete branch confirmation modal. (#5654)
  * New API routes added (#5594)
  * Refactor notification for indexer (#5111)
  * Refactor mail notification (#5110)
  * Show email if the authenticated user owns the profile page being requested for (#4981)
  * Optimize pulls merging (#4921)
  * Sort Repositories widget by most recently updated (#3963) (#4599)
  * Allow markdown table to scroll (#4401)
  * Automatically clear stopwatch on merging a PR (#4327)
  * Add the Owner Name to differentiate when merging (#3807)
  * Add title attributes to all items in the repo list viewer (#6258) (#6650)
* BUGFIXES
  * Fix dropdown icon padding (#6651) (#6654)
  * Fix wrong GPG expire date (#6643) (#6644)
  * Fix forking an empty repository (#6637) (#6653)
  * Remove call to EscapePound .Link as it is already escaped (#6656) (#6666)
  * Properly escape on the redirect from the web editor (#6657) (#6667)
  * Allow resend of confirmation email when logged in (#6482) (#6486)
  * Fix mail notification when close/reopen issue (#6581) (#6588)
  * Change API commit summary to full message (#6591) (#6592)
  * Add option to disable refresh token invalidation (#6584) (#6587)
  * Fix bug user search API pagesize didn't obey ExplorePagingNum (#6579) (#6586)
  * Fix new repo alignment (#6583) (#6585)
  * Prevent server 500 on compare branches with no common history (#6555) (#6558)
  * Properly escape release attachment URL (#6512) (#6523)
  * Hacky fix for alignment of the create-organization dialog (#6455) (#6462)
  * Disable benchmarking during tag events on DroneIO (#6365) (#6366)
  * Make sure units of a team are returned (#6379) (#6381)
  * Don't Unescape redirect_to cookie value (#6399) (#6401)
  * Fix dump table name error and add some test for dump database (#6394) (#6402)
  * Fix migration v82 to ignore unsynced tags between database and git data; Add missing is_archived column on repository table (#6387) (#6403)
  * Display correct error for invalid mirror interval (#6414) (#6429)
  * Clean up ref name rules (#6437) (#6439)
  * Fix Hook & HookList in Swagger (#6432) (#6440)
  * Change order that PostProcess Processors are run (#6445) (#6447)
  * Clean up various use of escape/unescape functions for URL generation (#6334)
  * Return 409 when creating repo if it already exists. (#6330)
  * Add same changes from issues page to milestone->issues page (#6328)
  * Fix ParsePatch function to work with quoted diff --git strings (#6323)
  * Fix reported issue in repo description (#6306)
  * Use url.PathEscape to escape the branchname (#6304)
  * Add robots.txt as reserved username (#6272)
  * Replace linkRegex with xurls library (#6261)
  * Remove visitLinksForShortLinks features (#6257)
  * Add unit types to repo action URL to correctly show 404 when archived (#6247)
  * Check organization visibility before everything else (#6234) (#6235)
  * Prevent double-close of issues (#6233)
  * Override xorm type mapping for U2F counter (#6232)
  * Add isAdmin to user API response (#6231)
  * Update git vendor to fix wrong release commit id and add migrations (#6224)
  * Fix fork button (#6223)
  * Fix renames over redirects (#6216)
  * Fix display dashboard even if require to change password (#6214)
  * Create a repo redirect when transferring ownership (#6210) (#6211)
  * Fix issue update race condition (#6194)
  * Fix bug when migrate repository 500 when repo is existed (#6188)
  * Fix scrollbar always present on page body (#6177)
  * Fix bug when set indexer as db and add tests (#6173)
  * Modify linkRegex to require http|https (#6171)
  * Fix bug user could change private repository to public when force private enabled. (#6156)
  * Fix admin list user/org API (#6143)
  * Make repo creation for API similar to UI (#6142)
  * Make document body a flexbox (#6139)
  * Refactor issue indexer, add some testing and fix a bug (#6131)
  * Load Issue attributes for API call (#6122)
  * Fix bug when update owner team then visit team's repo return 404 (#6119)
  * Fix heatmap and repository menu display in Internet Explorer 9+ (#6117)
  * Show private organization for admin, fix #6111 (#6112)
  * Fix prohibit login check on authorization (#6106)
  * Move to ldap.v3 to fix #5928 (#6105)
  * Remove use MakeAssigneeList in webhooks to fix deadlock (#6102)
  * Allow display of LFS stored Readme.md on directory page (#6073) (#6099)
  * Make sure labels are actually returned (#6053)
  * Fix panic: template: repo/issue/list:210: unexpected "=" in operand (#6041)
  * After deleting a repo on admin panel, UI should remember the last sort type (#6033)
  * Default create repository on organisation on its dashboard (#6026)
  * Swagger: Remove spaces in MergePullRequestOption enum (#6016)
  * Fix metrics auth token detection (#6006)
  * Fix repo header issues (#5995)
  * Fix bug when deleting a linked account will removed all (#5989)
  * Make organization dropdown scrollable when using mouse wheel (#5988)
  * Fix empty ssh key importing in ldap (#5984)
  * Admin config page mailertype setting option update (#5973)
  * Fix redirect loop during forced password change (#5965)
  * Show user who created the repository instead of the organisation in action feed (#5948)
  * Remove all CommitStatus when a repo is deleted (#5940)
  * Fix ssh deploy and user key constraints (#1357) (#5939)
  * Fix log output (#5938)
  * Set PusherName and PusherID to owner on deploy key to fix pushing with deploy keys (#5935)
  * Fix compare button (#5929)
  * Fix bug when read public repo lfs file (#5912)
  * Only allow local login if password is non-empty (#5906)
  * Recover panic in orgmode.Render if bad orgfile (#4982) (#5903)
  * Provide better panic handling (#5902)
  * Respect value of REQUIRE_SIGNIN_VIEW (#5901)
  * Show a 404 not a 500 if a repo does not exist (#5900)
  * Ensure repo is loaded in mailer (Completely fix #5891) (#5895)
  * Ensure issue.Poster is loaded in mailIssueCommentToParticipants (#5891)
  * Correct footer height if screen-width is to small (fixes #5878) (#5889)
  * In gitea serv switch off console logger to fix #5866 (#5887)
  * Don't allow pull requests to be created on an archived repository (#5883)
  * Support reviews on a deleted file path (#5880)
  * Fix compare button on upstream repo leading to 404 (#5877)
  * Fix null pointer on not logged in attempt to Sudo (#5872)
  * Fix new release creation API to allow empty target (#5870)
  * Fix an error while adding a dependency via UI. (#5862)
  * Fix failing migration v67 (#5849)
  * Fix delete correct temp directory (#5839)
  * Make sure .git/info is created before generating .git/info/sparse-che… (#5825)
  * Fix topics saving internal error and disable for archived repos (#5821)
  * Fix TLS errors when using acme/autocert for local connections (#5820)
  * When creating new repository fsck option should be enabled (#5817)
  * Request for public keys only if LDAP attribute is set  (#5816)
  * Fix serving of raw wiki files other than .md (#5814)
  * Fix migration 78 error mssql (#5791)
  * Disallow empty titles (#5785)
  * Fix the v78 migration script (#5776)
  * Ensure valid git author names passed in signatures (#5774)
  * Fix wrong assumption where a user is always said to have unassigned (her)himself (#5769)
  * Upgrade go-sql-driver/mysql to fix invalid connection error (#5748)
  * Fixing PostgreSQL dump creation (#5747)
  * Add proper CORS preflight origin validation (#5740)
  * Disable auto-migrate in docker container (#5730)
  * In basic auth check for tokens before call UserSignIn (#5725)
  * Pooled and buffered gzip implementation (#5722)
  * Ensure that sessions are passed into queries that could use the database to prevent deadlocks (#5718)
  * Keep file permissions during database migration (#5707)
  * Use correct value for "MSpan Structures Obtained" #4742 (#5706)
  * Refactor editor upload, update and delete to use git plumbing and add LFS support (#5702)
  * Update xorm to fix issue #5659 and #5651 (#5680)
  * Fix public will not be reused as public key after deleting as deploy key (#5671)
  * When redirecting, clean the path (#5669)
  * Don't list an issue on its own dependency list UI. (#5658)
  * Fix commit page showing status for current default branch (#5649) (#5650)
  * Only count users own actions for heatmap contributions (#5647)
  * Fix sqlite deadlock when assigning to a PR (#5640)
  * Refactor issue indexer (#5363)
* TESTING
  * Run benchmark at tag to track performances (#6035)
  * Add test environment for MySQL8 (#5234)
* BUILD
  * Use go 1.12 for tests and deprecate go 1.9 (#6186)
  * Makefile changes for Windows and easier development (#6103)
  * Update bleve dependency to latest master revision (#6100)
  * Switch to more recent build of xgo (#6070)
  * Add autoprefixer to css build (#6029)
  * Update the version of less (#6010)
  * Make log mailer for testing (#5893)
* DOCS
  * Add more tests and docs for issue indexer, add db indexer type for searching from database (#6144)
  * update default value of `--must-change-password` cli flag (#6032)
  * Update and expand information about building Gitea (#6019)
  * Update U2F Section of app.ini.sample (#5994)
  * Update swagger for release API pagination (#5841)
  * Added docs for the tree api (#5834)
* MISC
  * Add single commit API support (#5843)
  * Add missing GET teams endpoints (#5382)
  * Migrate database if app.ini found (#5290)

To see all user-facing changes that went into the release, check out our
[full changelog](https://github.com/go-gitea/gitea/blob/master/CHANGELOG.md#180---2019-04-20).

A shoutout goes to those who reported and/or fixed security issues in this
release:

* [@techknowlogick](https://github.com/techknowlogick) ([#6674](https://github.com/go-gitea/gitea/pulls/6674))
  * With special thanks to [@jonasfranz](https://github.com/jonasfranz) for making Gitea an OAuth2 provider
and to [0x5c](https://github.com/0x5c), Nils Sandmann, [Max Mehl](https://fsfe.org/about/mehl), and Andreas Shimokawa who all independently reported the API 2FA bypass security loophole.
* [@zeripath](https://github.com/zeripath) ([#6594](https://github.com/go-gitea/gitea/pull/6594) [#6677](https://github.com/go-gitea/gitea/pull/6677)
  * With special thanks to [@mrsdizzie](https://github.com/mrsdizzie) for quietly confirming the underlying bug in [#6677](https://github.com/go-gitea/gitea/pull/6677) and [@perflyst](https://github.com/perflyst) for reporting [#6320](https://github.com/go-gitea/gitea/issues/6320) which should properly be fixed by ([#6594](https://github.com/go-gitea/gitea/pull/6594)

## Help us out!

Gitea is focused on community input and contributions. To keep a project like
Gitea going we need people. **_LOTS_** of people. You can help in the
following areas:

### Programming

If you know Go or HTML/CSS/JavaScript, you may be interested in working on the
code. Working on OSS may seem scary, but the best way is to try! Read the
[Gitea contribution guide](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md),
and then [find an itch to scratch](https://github.com/go-gitea/gitea/issues),
or scratch your own!

### Translating

Want to translate Gitea in your own language? Awesome! Join the Gitea project
on [Crowdin](https://crowdin.com/project/gitea). As soon as your translation is
approved, it will be pushed to the Gitea project to be used in future releases!

### Documentation

Documentation is important, but also time consuming. If you enjoy writing and
have a pretty good knowledge of English, or you would like to translate the
English version to your native language, you're very welcome to do so. Find our
documentation on the main git repository
[here](https://github.com/go-gitea/gitea/tree/master/docs). Just fork, update
the documentation and then create a pull request!

### Support

Do you like people? Can you give calm and thought-out responses to users needing
help? Then you can spend some time providing support to those who need it. Most
answers can really be found in the documentation, so make sure to take some time
to read it. Then, either join our chat or forums (linked below), or simply
help us sort out issues and answer questions on the
[Gitea repository](https://github.com/go-gitea/gitea/issues).

### Donations

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

### … or reporting bugs

If you lack the time or knowledge to do any of the above, just using Gitea and sharing the word is enough to make us happy! One thing you can always do is to report any bugs you find on the [Gitea issue tracker](https://github.com/go-gitea/gitea/issues).

Before opening an issue, read the [contribution guidelines about reporting bugs](https://github.com/go-gitea/gitea/blob/master/CONTRIBUTING.md#bug-reports). After opening an issue, try to stick around a while to answer any questions we might have. Replies greatly help us find the root cause of an issue.

## Thanks

This release would not have been possible without the pull requests from the following people:

* [@adelowo](https://github.com/adelowo)
* [@apricote](https://github.com/apricote)
* [@appleboy](https://github.com/appleboy)
* [@aswild](https://github.com/aswild)
* [@barkap](https://github.com/barkap)
* [@bogdanpetrea](https://github.com/bogdanpetrea)
* [@DblK](https://github.com/DblK)
* [@eloyekunle](https://github.com/eloyekunle)
* [@emonty](https://github.com/emonty)
* [@EpicCoder](https://github.com/epiccoder)
* [@gabrielsimoes](https://github.com/gabrielsimoes)
* [@gdeverlant](https://github.com/gdeverlant)
* [@gdutyifei](https://github.com/gdutyifei)
* [@gzsombor](https://github.com/gzsombor)
* [@HarshitOnGitHub](https://github.com/HarshitOnGitHub)
* [@jeblair](https://github.com/jeblair)
* [@jolheiser](https://github.com/jolheiser)
* [@joohoi](https://github.com/joohoi)
* [@jonasfranz](https://github.com/jonasfranz)
* [@kolaente](https://github.com/kolaente)
* [@KubqoA](https://github.com/KubqoA)
* [@lafriks](https://github.com/lafriks)
* [@LoveEevee](https://github.com/loveeevee)
* [@lunny](https://github.com/lunny)
* [@manuelluis](https://github.com/manuelluis)
* [@mrsdizzie](https://github.com/mrsdizzie)
* [@muhammedtiftikci](https://github.com/muhammedtiftikci)
* [@pciavald](https://github.com/pciavald)
* [@pbrackin](https://github.com/pbrackin)
* [@pgodwin](https://github.com/pgodwin)
* [@mporrato](https://github.com/mporrato)
* [@richmahn](https://github.com/richmahn)
* [@sapk](https://github.com/sapk)
* [@sebastian-sauer](https://github.com/sebastian-sauer)
* [@segevfiner](https://github.com/segevfiner)
* [@silverwind](https://github.com/silverwind)
* [@saromanov](https://github.com/saromanov)
* [@sd1998](https://github.com/sd1998)
* [@stevegt](https://github.com/stevegt)
* [@techknowlogick](https://github.com/techknowlogick)
* [@tklein23](https://github.com/tklein23)
* [@typeless](https://github.com/typeless)
* [@wewark](https://github.com/wewark)
* [@Whisprin](https://github.com/Whisprin)
* [@xabufr](https://github.com/xabufr)
* [@xdch47](https://github.com/xdch47)
* [@yasuokav](https://github.com/yasuokav)
* [@zeripath](https://github.com/zeripath)

[PRs](https://github.com/go-gitea/gitea/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Amerged+milestone%3A1.8.0)
and [issues](https://github.com/go-gitea/gitea/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+milestone%3A1.8.0)
merged in 1.8.0.

# Get in touch

Need help with anything?
You can come on our [Discord server,](https://discord.gg/gitea) or if you're
more old-fashioned you can also use our [forums](https://discourse.gitea.io/).
