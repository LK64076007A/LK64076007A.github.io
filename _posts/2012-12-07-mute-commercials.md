---
layout: post
title: Mute commercials on CBS.com with Keyboard Maestro
date: 2012-12-07 13:06  
tags:
- Keyboard Maestro
- programming
- technology
- commercials
---

I watch TV on my Macbook Air on the weekends when I'm ironing. Sadly, commercials are becoming more popular with CBS airing 4 in a row, often the same exact commercial over and over. There's no way to skip them, but I made a quick macro with Keyboard Maestro that mutes the sound until the commercials are over and then turns the sound back on.

You have to toggle the macro manually when the commercial starts, but otherwise, it works great.

[![](/images/Muting_CBS_macro.png)](/images/Muting_CBS_macro.png) 
 
The macro is a very simple three steps.

1. Toggle System Sound Mute, turning off the sound.
2. Watch for an image to disappear from the screen. The image is a screen capture of the word advertisement that overlays advertisements when they're playing.
3. Toggle System Sound Mute, turning on the sound.

The picture I used to monitor:

[![](/images/Advertisement_image.png)](/images/Advertisement_image.png) 

Now I don't have to listen to annoying commercials.

**Update:** Same macro with a slightly different picture works for Hulu. Also, now I'm occasionally seeing 5 commercials in a row.