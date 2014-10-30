---
layout: post
title: Two improvements with Keyboard Maestro 6
date: 2013-05-21 12:57  
tags:
- Keyboard Maestro
- technology
---
I'm a big fan of [Keyboard Maestro](http://www.keyboardmaestro.com/main/) and use it both daily for my workflow as well as occasionally for projects as they arise.

[Version 6.0](http://www.keyboardmaestro.com/main/) was released today and is a major upgrade over version 5. There are many improvements both major, minor, and cosmetic. It was well worth the $25 upgrade price.

[Macdrifter](http://www.macdrifter.com/) has a nice write up and I'm sure that [Macstories](http://www.macstories.net/news/keyboard-maestro-6-0-adds-syncing-browser-actions-device-triggers-and-more/) will have a very detailed review within a few weeks.

Today I'm just going to share two small items made possible with the new version.

## Shorter macros with browser text tokens

First, some types of macros are more easy to create and are smaller due to the [new web browser text tokens](http://www.keyboardmaestro.com/documentation/6/tokens.html). I had [previously created a macro](http://soitscometothis.net/post/Switching-the-current-viewed-webpage-between-Safari-and-Chrome) that would take an URL that was currently open in Safari and open it in Chrome instead, and vice versa. 

The macro in version 5 is fairly long:

[![Switching browsers in KM5 macro](/images/switching_browsers_KM5.jpg)](/images/switching_browsers_KM5.jpg)

The same macro in version 6 is much smaller:

[![Switching browsers in KM6 macro](/images/switching_browsers_KM6.jpg)](/images/switching_browsers_KM6.jpg)

This is all directly or indirectly because there is a text token for the current URL in both web browsers. This gets rid of the AppleScript for getting the URL. It also indirectly allows me to get rid of commands to open the opposite web browser as well as to wait for that browser to be open. In the version 5 macro, I had a command to switch to the new browser since that was necessary in order to enter the URL into the address bar. Since in my situation, I may not want to immediately switch over to the other browser, I was able to leave that off too.

## Easy creation of Markdown links from current webpage

Seeing how easy it was to change the above macro, I decided to make a quick macro to make a Markdown link using the current Safari URL as the link URL and the current Safari window title as the link text. I also used the new text token `%|%` to place the cursor in position to quickly change the link text in case the window title isn't appropriate.

[![](/images/MD_link_from_Safari_title_url.jpg)](/images/MD_link_from_Safari_title_url.jpg)

I'm looking forward to upgrading my old macros and kicking the tires a bit more. I can't wait for my next project so I have a chance to create something new.