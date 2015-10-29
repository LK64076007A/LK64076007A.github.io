---
layout: post
title: Updated - Fixing shortcuts in Messages.app
Date: 2012-08-25 08:39 
tags: 
- technology
- programming
- OSX
---

### Update 
Make a new Keyboard Shortcut in the preferences menu so that "Close Conversation..." is ⌘-W. That will restore ⌘-⌫ to the correct "delete whole line functionality."

### Original  (August 6, 2012)
I like my keyboard shortcuts to be consistent across applications. Two shortcuts I use frequently ⌥-⌫ (option-delete) to erase the last word and ⌘-⌫ (command-delete) to erase the last line[^1208062014].

Since upgrading to Mountain Lion, every time I hit ⌘-⌫ in the Messages app, I get a prompt asking if I want to delete the conversation. And every single time it's mentally jarring as normal, expected behavior elicits an unexpected and incorrect response. That shortcut is being used as a built-in for the app:

![Wrong shortcut](/images/Built_in_messages_shortcut.png) 

A few minutes of searching the web led me to the universally accepted answer that "no, there is nothing you can do about it." Even a well written (I assume--tl;dr) [piece by Gruber](http://daringfireball.net/2003/12/losers_weepers) weren't promising.

So I took a chance and tried to change the shortcut by adding another shortcut on top of it in Keyboard Shortcuts in system preferences. 

![Changing the shortcut](/images/changing_the_shortcut.png)

I used ⌃⌥↩ because I can't see myself every using that shortcut. I can't explain why it seems to get duplicated and also show a new shortcut of ⌥⌘⌫. I did notice that when I went back and re-did this a few times (to take screenshots), I kept getting different duplications. One thing that seemed to be necessary is trying to first make the shortcut ⌃⌥⌫, which would make an error sound and not accept, then doing another one would lead to the desired results. 

![Changed shortcut](/images/changed_shortcut.png) 

Clear as mud, I know. 

[^1208062014]: This is the case for Textedit, Pages, and Safari. I'm willing to bet it's the case for most native and third-party apps since I've never run across this frustration before.