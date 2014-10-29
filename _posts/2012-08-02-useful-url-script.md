---
layout: post
date: 2012-08-02 19:56  
title: Crazy useful url script from Dr. Drang
link: http://www.leancrew.com/all-this/2012/08/the-safari-6-url-crisis/
tags: TextExpander
---

Paste the url from the top tab in Safari into current location of the cursor with one line of Applescript in TextExpander. 

[Dr. Drang][leancrew]:

> Boom. Give that a nice abbreviation, like ;furl for “front URL,” and it’ll insert the URL directly where you’re typing. There’s no need to run the script and then paste the URL—that’s an inefficiency that comes from thinking the script has to act like you would.

**Update:** I've found this works better in Keyboard Maestro because I'm typically tying in urls right after another character, like a "(". TextExpander won't expand a macro in such a situation whereas Keyboard Maestro will. Just have the macro run an Applescript and paste the results.

For Safari: `tell application "Safari" to get the URL of the front document`

For Chrome: `tell application "Google Chrome" to get the URL of active tab of first window`

[leancrew]: http://www.leancrew.com/all-this/2012/08/the-safari-6-url-crisis/ "Dr. Drang"
