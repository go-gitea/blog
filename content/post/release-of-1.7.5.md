---
date: "2019-03-27T12:00:00-05:00" 
author: "jolheiser"
title: "Gitea 1.7.5 is released"
tags: ["release"]
draft: false
---

We are happy to announce that version 1.7.5 of Gitea has now been released. This version only has 3 merged pull requests as we prepare for 1.8.0! 

You can download one of our pre-built binaries from our
[downloads page](https://dl.gitea.io/gitea/1.7.5/) - make sure to select the
correct platform! For further details on how to install, follow our
[installation guide](https://docs.gitea.io/en-us/install-from-binary/).

We'd like to thank all of our supporters on
[Open Collective](https://opencollective.com/gitea) who are helping us
with financial sustainment.

<!--more-->

## Changelog

* BUGFIXES
  * Fix unitTypeCode not being used in accessLevelUnit ([#6419](https://github.com/go-gitea/gitea/pull/6419)) ([#6423](https://github.com/go-gitea/gitea/pull/6423))
  * Fix bug where manifest.json was being requested without cookies and continuously creating new sessions ([#6372](https://github.com/go-gitea/gitea/pull/6372)) ([#6383](https://github.com/go-gitea/gitea/pull/6383)) 
  * Fix ParsePatch function to work with quoted diff --git strings ([#6323](https://github.com/go-gitea/gitea/pull/6323)) ([#6332](https://github.com/go-gitea/gitea/pull/6332))
