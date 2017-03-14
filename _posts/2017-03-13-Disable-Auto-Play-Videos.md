---
layout: post
title: 'Disable Auto-Play Videos' # quotes allow forbidden characters
date: 2017-03-13 20:50:14 -500
link: http://www.kirkville.com/stop-auto-play-videos-from-annoying-you-in-your-browser/
tags:
- technology 
- advertising
---

Kirk McElhearn, [Stop Auto-Play Videos from Annoying You in Your Browser on macOS](http://www.kirkville.com/stop-auto-play-videos-from-annoying-you-in-your-browser/), on March 13, 2017:

> • Here are the direct commands to activate and deactivate this feature in Safari from Terminal, without displaying the Debug menu:
> 
> defaults write com.apple.Safari WebKitMediaPlaybackAllowsInline -bool false
>
> defaults write com.apple.SafariTechnologyPreview WebKitMediaPlaybackAllowsInline -bool false
>
> defaults write com.apple.Safari com.apple.Safari.ContentPageGroupIdentifier.WebKit2AllowsInlineMediaPlayback -bool false
>
> defaults write com.apple.SafariTechnologyPreview com.apple.Safari.ContentPageGroupIdentifier.WebKit2AllowsInlineMediaPlayback -bool false

Amen. 
