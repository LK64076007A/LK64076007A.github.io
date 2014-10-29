---
layout: post
title: Creating a plain text wiki with nvALT
date: 2013-04-10 11:04  
tags: apps, notes, technology
---

## Introduction

When I was in medical school, they issued the student's [Sony Cliés][wikipedia][^1365609755-Model PEG-TJ27]. It was an awesome little device for the time and I took a lot of notes on it while on rounds. Sadly, a few years later, I was unable to read the files when the Clié finally died and I was unable to read the files with any of the software on my computers.

Since then, I've been an advocate for plain text file. Plain text does not use any strange or proprietary formatting so the files can be read on any platform and in any app. The data is about as future-proof as you can get.

There are [many other benefits to plain text as well][macworld].

Although I use many apps on many devices to read my plain text files, my favorite by far is [nvALT][brettterpstra]. It is fast, responsive, intuitive, and created by [a programmer I highly respect][brettterpstra 2]. Unfortunately, it is free, but you can donate money like I did to support its continued development. 

Today I found another useful way to use nvALT.

## Creating a plain text wiki

As I was reading an article on auto-inflammatory syndromes, I was struck with the idea of creating a list of all the rheumatology diseases. I hit my hotkey trigger to bring up nvALT and typed "rheumatology diseases" to see if I might have started such a list before. No results appeared, so I hit enter and the document with the title "rheumatology diseases" was created.

I copy and pasted the list of auto-inflammatory diseases into the note and went back to reading the article. As is typical, the article started with the first disease and moved down the list. *Now I wanted another text document about that disease in which I could write some notes*. While it wouldn't be hard to do, wouldn't it be nice if the original list of diseases could link to this other document so I could easily browse them in the future?

It happens that nvALT has an in-app feature[^1365609755-fn1] that allows you to create links to other documents by wrapping the words in [[double brackets]]. Whatever words are in double brackets link to a note with the same words as the title. Example: "I love to eat [[chocolate]]." would link to a document with the name chocolate.txt. In my case, "FMF - [[familial Mediterranean fever]]" linked to a new document "familial Mediterranean fever.txt".

As I read my way through the journal article, I created a new text document for each disease that is linked to from the disease list document. I imagine in this way, I could accidentally end up writing a book someday, or maybe just a good wiki for my website. Since I'm writing it all in Markdown anyway, the conversion would be relatively simple.

## Conclusion

It's simple. It's elegant.

[brettterpstra]: http://brettterpstra.com/2012/02/28/nvalt-2-2-public-beta/
[brettterpstra 2]: http://brettterpstra.com/about/
[macworld]: http://www.macworld.com/article/1161549/forget_fancy_formatting_why_plain_text_is_best.html
[wikipedia]: http://en.wikipedia.org/wiki/CLIÉ

[^1365609755-Model PEG-TJ27]: [Model PEG-TJ27](http://www.sonyclie.org/models.html)

[^1365609755-fn1]: This means it works in the app, but won't work elsewhere. Because the documents are plain text, this won't break the document when read in other applications, but the link itself won't be active.