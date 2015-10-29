---
layout: post
date: 2012-01-20
title: Forcing Spotlight to re-index
link: http://idoitonamac.blogspot.com/2011/07/os-x-lion-and-spotlight.html
tags: 
- OSX
- Spotlight
---

For some reason today,[^1201202107] I just couldn't find the correct instructions for forcing Spotlight to re-index using the Terminal. Therefore, I'm reposting the instructions here so this is easier to find in the future.

    // First copy and paste this at the command prompt
    sudo mdutil -E /

    // Enter your password when prompted, and then paste this
    sudo mdutil -i on /

[^1201202107]:  Listen, Google, [Duck Duck Go](duckduckgo.com) is starting to look more attractive every day.