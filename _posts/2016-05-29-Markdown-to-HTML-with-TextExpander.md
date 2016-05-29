---
layout: post
title: 'Markdown to HTML with TextExpander'
date: 2016-05-29 16:01:26 -0500
tags: 
- TextExpander
- technology
- Markdown
---
I needed a way to convert Markdown-formatted text to HTML without any line breaks for writing show notes for podcasts using the [Driftwood platform](https://github.com/LK64076007A/driftwood), because it holds the shownotes in the YAML front matter. I wanted to be able to do this on both iOS and OS X. 

I haven't given up on TextExpander, yet[^160529161358], and so far it is the only option I'm aware of in which I can sync the same macros across all my iOS and OS X devices. 

The problem ended up being fairly simple[^160529162217].

First I needed to find a javascript library to do the conversion. Googling returned [just such a library, [Marked](https://github.com/chjj/marked) by [Chris Jeffrey](https://twitter.com/_chjj).

I took the minified version and created a TextExpander snippet of just that code.

Then I made the snippet for the conversion. It consists of only two lines of code. The first calls the Marked library:

`%snippet:marked.min.js%`

and the second takes whatever is in the clipboard, runs it through the marked library, and then removes newlines:

`marked(TextExpander.pasteboardText).replace(/(\n)+/g, '');`

It doesn't get much simpler than that. 

[^160529161358]: I haven't "upgraded" yet either.

[^160529162217]: If it takes me less than an hour to figure it out and write the blog post, it is "simple".