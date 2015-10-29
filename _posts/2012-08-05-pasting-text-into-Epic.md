---
layout: post
date: 2012-08-05 11:14  
title: Errors when pasting text from a Mac into Epic and Allscripts
tags:
- Keyboard Maestro
- medicine
- technology
- programming
---

**Update 2 (5.23.2013):** When my friend updated to Keyboard Maestro 6, this fix stopped working. This may be because the filter line endings had nothing to do with the fix, rather that process had an unexpected side effect of changing rich text to plain text. We are in the process of testing this theory. If you can't wait, try filtering with "remove styles".

**Update:** [@psufka](http://twitter.com/psufka) reports that he has seen this with Windows machines, so apparently is not an isolated Mac compatibility issue.

A colleague  and friend was having trouble with the Epic electronic medical record. He writes his notes in Pages on the Mac and when he would try to paste the text into Epic, it would mess up. What he was seeing was his note was losing words and the paragraph formatting was screwed up. It was making his life painful, slow, and frustrating…basically like all EMRs make life.

**Thankfully, there's a really simple solution**

What was happening (I think) was that he was pasting text from a Mac environment into a Unix environment, [which have different (invisible) characters to end a line][editpadpro].[^1208051113]

[Keyboard Maestro][keyboardmaestro] has a function to change the line endings of whatever text is in the clipboard. So now, he copies the text to the clipboard using ⌘-C, switches to the EMR, and ⌃⌘-V pastes the correctly formatted text into the EMR without any screw ups.

![Epic pasting KM macro](/images/pastingIntoEpic.png) 

The same thing was also happening with another EMR he uses, Allscripts. The same solution worked there too.

Keyboard Maestro is a very powerful application for the Mac. I can't begin to say how great it is. It is also not for beginners. If you're looking to get started with taking more control over your machine, this is not the place I'd recommend starting unless you have a strong familiarity with computers and have someone to help you along the way. Otherwise, it's very much worth it's price of $36.

[keyboardmaestro]: http://www.keyboardmaestro.com/main/
[editpadpro]: http://www.editpadpro.com/tricklinebreak.html

[^1208051113]: There is probably a little more to it than that since the first string of each new paragraph was disappearing, but I'm not an expert and my fix works.
