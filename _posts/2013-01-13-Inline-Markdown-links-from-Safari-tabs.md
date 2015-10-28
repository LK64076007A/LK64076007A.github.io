---
layout: post
title: Inline Markdown links from Safari tabs
date: 2013-01-13 23:06  
tags: 
- programming
- technology
- TextExpander
- Keyboard Maestro
---

This post is mostly for me, so I can remember how I did this in the future.

I was creating show notes for a podcast I do. I needed to make a list of links to scientific papers. Even using Markdown rather than HTML it took me an insanely long amount of time to manually copy over the titles and links. So I decided I'd spend the next hour never doing that again.

First, I figured out a way to get the links easily. Unfortunately, [Papers][mekentosj] does not have a way to easily copy out the information directly, but it does have a way to highlight all the papers you want to link and open them all in tabs in your browser.

Now that I had all the papers open in their own tab, I needed a way to make Markdown links from them. I thought I had read something about doing this before, but I couldn't find it again[^1301132310], but I did find [a post by Dr. Drang][leancrew] that got me halfway there. The only problem was that his method only gave me the second half of a list of reference links when what I wanted was inline links with the title of the webpage as the text.

His technique gave me this:

    [1]: website url
    [2]: website url
    [3]: website url
    [4]: website url

When what I wanted was this:

    [Website Title](website url)
    [Website Title](website url)
    [Website Title](website url)
    [Website Title](website url)

I like reference links too, but I needed the title of the paper for my purposes and I already have another macro that I use to turn inline links into reference links later.

My Applescript knowledge is weak, but I quickly found [this page][lucifr], which I can't read because it's in Chinese, and by looking at the code, figured out how to get what I needed.

I changed Dr. Drang's original code:

    tell application "Safari"
      set i to 1
      set links to ""
      repeat with t in every tab in front window
        set links to links & "[" & i & "]: " & the URL of t & linefeed
        set i to i + 1
      end repeat
      return links
    end tell

to this:

    tell application "Safari"
      set i to 1
      set links to ""
      repeat with t in every tab in front window
        set links to links & "[" &the name of t& "](" & the URL of t &")"& linefeed
        set i to i + 1
      end repeat
      return links
    end tell

You can then throw that into a TextExpander snippet or a Keyboard Maestro Macro and you're prestige.

Frankly, Papers needs a way to do this in the app itself.

[^1301132310]: I need a Nerd-blog Search Engine

[leancrew]: http://www.leancrew.com/all-this/2012/07/markdown-reference-links-from-safari-tabs/
[lucifr]: http://lucifr.com/2012/09/01/selected-safari-tabs-to-markdown-reference-links/
[mekentosj]: http://www.mekentosj.com/papers/