---
layout: post
title: Amazon affiliate link for TextExpander
date: 2015-07-04 4:43:33 -0500
tags: 
- TextExpander
- Amazon affiliate link
---

My affiliate linking scripts were starting to get out of hand with different versions in [Keyboard Maestro][keyboardmaestro], [Pythonista][apple], [Editorial][apple 2], [Drafts][apple 3], [Workflow][apple 4], and [TextExpander on the Mac][7eer]. It was difficult to know what scripts worked where and if they were up to date. I decided to expunge them all but one. 

The *one* would have to work equally well on iOS and OS X as I use them equally and interchangeably. Until now this was not possible as none of those apps was on both devices, but with TextExpander getting JavaScript support, I thought it might now be possible.[^20150704101546]

## Code explanation 

* Line 3: Stores the affiliate code to a variable.  
* Line 4: Stores the clipboard to a variable.  
* Line 5: Defines the regular expression and stores it to a variable. My choice of regex looks for the first string of all capital letters or numbers following a slash, which seems to always be the Amazon (ASIN).  
* Line 6: Runs the match for the regular expression, returning null if it isn't found and an array of it is.  
* Line 8-13: Evaluates the result of the regex search. If it failed, it returns the original text. If it succeeds, it stores ASIN to a variable and creates the new link.  
* Line 15: Writes the new URL to the clipboard. This isn't necessary for the expansion of the affiliate link by TextExpander as the result of the script is what is expanded, not the clipboard, but I like having the link in the clipboard in case I need to paste it somewhere else immediately. 

<script src="https://gist.github.com/LK64076007A/30ed6c4c52e36978540b.js"></script>

[^20150704101546]: Dr. Drang had [written about converting his script over to JavaScript for TextExpander][leancrew], and at first I thought I could just steal his, but this was a dead end. Since he used JavaScript for Automation in his snippet it would not work in iOS and his regex didn't work with the URLs I was getting.

[7eer]: http://smile.7eer.net/i/157164/161942/2936
[apple]: https://itunes.apple.com/us/app/pythonista/id528579881?mt=8&uo=4&at=11l4RT
[apple 2]: https://itunes.apple.com/us/app/editorial/id673907758?mt=8&uo=4&at=11l4RT
[apple 3]: https://itunes.apple.com/us/app/drafts-4-quickly-capture-notes/id905337691?mt=8&uo=4&at=11l4RT
[apple 4]: https://itunes.apple.com/us/app/workflow-powerful-automation/id915249334?mt=8&uo=4&at=11l4RT
[keyboardmaestro]: http://www.keyboardmaestro.com/main/
[leancrew]: http://leancrew.com/all-this/2015/06/clean-amazon-links-with-textexpander/