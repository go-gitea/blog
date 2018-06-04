---
date: "2018-06-04T09:30:00+00:00"
author: "techknowlogick"
title: "Release of 1.4.2"
tags: ["release"]
draft: false
---

It's been a wild and wonderful weekend. Many new users have found Gitea and we are so happy to be able to help you with your self-hosting Git journey. Thank you to all of our backers on [Open Collective](https://opencollective.com/gitea), you are helping us deliver a better piece of software.

We are happy to release version 1.4.2 of Gitea. We have merged [13 pull requests](https://github.com/go-gitea/gitea/milestone/23?closed=1) to release version.

You can download one of our pre-built binaries from our [downloads page](https://dl.gitea.io/gitea/1.4.2/), you just need to select the correct platform. For further details of the installation follow our [installation guide](https://docs.gitea.io/en-us/install-from-binary/).

<!--more-->

## Changelog

* BUGFIXES
  * Adjust z-index for floating labels (#3939) (#3950)
  * Add missing token validation on application settings page (#3976) #3978
  * Webhook and hook_task clean up (#4006)
  * Fix webhook bug of response info is not displayed in UI (#4023)
  * Fix writer cannot read bare repo guide (#4033) (#4039)
  * Don't force due date to current time (#3830) (#4057)
  * Fix wiki redirects (#3919) (#4065)
  * Fix attachment ENABLED (#4064) (#4066)
  * Added deletion of an empty line at the end of file (#4054) (#4074)
  * Use ResolveReference instead of path.Join (#4073)
  * Fix #4081 Check for leading / in base before removing it (#4083)
  * Respository's home page not updated after first push (#4075)
