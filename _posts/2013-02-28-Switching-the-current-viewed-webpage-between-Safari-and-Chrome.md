---
layout: post
title: Switching the current viewed webpage between Safari and Chrome
date: 2013-02-28 14:27  
tags: 
- Keyboard Maestro
- technology
---

**Update:** This macro was made for Keyboard Maestro 5. Although it will work with KM 6, a newer version of the macro is available as is much simpler and faster with less risk of bugs.

### Problem ###

Safari is my typical browser of choice, but sometimes I want to open a webpage I'm already looking at in Safari in Chrome instead[^20130228142554]. Sometimes I'm looking at a webpage in Chrome and want to open it in Safari. 

### Solution ###

It's not super elegant, but I made a Keyboard Maestro macro to switch back and forth. 

It consists of two nested if/then statements that check for which browser I'm using, grabs the URL of the front window, opens the other browser, pauses until the browser is running and the front window is open, pastes the URL into the navigation bar, and finally hits enter.

- If Safari is at the front
	- Execute the Applescript `tell application "Safari" to get the URL of the front document` and save results to variable `currentURL`
	- Activate Google Chrome
	- Pause until Google Chrome is at the front and the front window exists
	- Type the keystroke ⌘T
	- Type the keystroke ⌘L
	- Insert the text by pasting: `current URL`
	- Type the keystroke `return`
- otherwise execute the following
	- If Google Chrome is at the front
		- Execute Applescript `tell application "Google Chrome" to get the URL of active tab of first window` and save results to variable `currentURL`
		- Activate Safari
		- Pause until Safari is at the front and the front window exists
		- Type the keystroke ⌘T
		- Type the keystroke ⌘L
		- Insert the text by pasting: `current URL`
		- Type the keystroke `return`

I assigned the shortcut Caps lock (which on my computer simultaneously pressed shift-command-control-option) - u. 

[![](/images/open_current_webpage_in_other_browser.png)](/images/open_current_webpage_in_other_browser.png) 

[Download the macro](/images/Open_current_webpage_in_the_other_browser.kmmacros).

[^20130228142554]: For example, if you're limiting Flash to Chrome only via [the Gruber method](http://daringfireball.net/2010/11/flash_free_and_cheating_with_google_chrome).