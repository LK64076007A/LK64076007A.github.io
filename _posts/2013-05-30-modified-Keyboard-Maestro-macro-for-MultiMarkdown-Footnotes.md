---
layout: post
title: A modified Keyboard Maestro macro for MultiMarkdown Footnotes  
date: 2013-05-30 18:53  
tags: Keyboard Maestro, Markdown, technology, blogging, article
---

**Update: This post is long out of date. Zettt and I worked together to come up with a better, faster way to do the same thing with Keyboard Maestro. Find his latest version of his Keyboard Maestro Markdown Library to see it in action.**

# Introduction #

If you write in (Multi)Markdown and have Keyboard Maestro, I recommend you check out Andreas's (@[Zettt](https://twitter.com/Zettt)) [Keyboard Maestro Markdown library](http://www.macosxscreencasts.com/general/keyboard-maestro-markdown-library/), which makes it easy to write in Markdown through various schemes such as easily wrapping selected text with various special characters[^20130530190615]; creating inline links, reference links, and image tags with fill-in templates; making ordered and unordered lists from selected lines of text; and several others. His videos clearly explain how to use them. He also chose a brilliant hotkey schema that makes it easy to remember all the options once you learn one or two.

He's currently working on some updates with the release of KM6, but that got me thinking about a modification I wanted to make.

# Problem #

As it stands now, after placing the footnote, the cursor is left at the bottom of the document, rather than back in the text where the writing will continue.[^20130530193065]

This slight break in workflow is an unfortunate drawback of creating footnotes[^20130530191980]. Some text editors do have the ability to remember cursor position so that it can be returned it to the original position, but one of the reasons I use Keyboard Maestro for these tasks is so they will be editor agnostic since I'm constantly changing my editor.

# Solution #

Keyboard Maestro 6 added a cursor position token: `%|%`. Since the original macro involved two paste actions separated by moving the cursor, I was going to need to combine them into one paste action. Instead of using ⌘-↓ to move the cursor to the bottom of the text, I use ⇧-⌘-↓ to select all the text from the cursor position to the bottom of the document. I then cut (⌘-X) this to the clipboard. Finally, I paste a concatenation of the footnote tag, the cursor position token, the clipboard, and the footnote:

<pre>[^%Variable%MMDFootnoteTag%]%|%%CurrentClipboard%

[^%Variable%MMDFootnoteTag%]: %Variable%MMDFootnoteText%</pre>

The extra carriage return is because, in my experience, you need to have a blank line between footnotes, unlike reference links, to get them to display correctly. Fletcher Penney [recommends this format](https://github.com/fletcher/MultiMarkdown/wiki/MultiMarkdown-Syntax-Guide) with regards to bibliography support in Multimarkdown.

The final macro looks like this:

[![](/images/modified_KM_macro_footnote.jpg)](/images/modified_KM_macro_footnote.jpg) 

If you're paying close attention, you might notice that I also added a default value for the footnote tag, which is just the date and time in [ICU yyyyMMddHHSS format](http://userguide.icu-project.org/formatparse/datetime).

I think this makes it much easier and natural to write Multimarkdown footnotes, which may turn out to be a bad thing since I'm suddenly adding them all over the place.[^20130530201400]

You can download the macro [here](/images/Multimarkdown_Footnote.kmmacros).

[^20130530190615]: Asterisk, double asterisk, quotation marks, parentheses, brackets, and backtick quotes.

[^20130530191980]: Unless you make inline footnotes and convert them using [Brett Terpstra's system service](http://brettterpstra.com/2012/01/24/a-service-for-writing-multimarkdown-footnotes-inline/). I tried it, but too often it wouldn't work because I was trying to nest a footnote inside a link inside something else. 

[^20130530193065]: The macro is written to insert the footnote tag at the current cursor position, ⌘-↓ to move to the bottom of the document, and then paste the footnote.

[^20130530201400]: Like this one, for no good reason other than I could.