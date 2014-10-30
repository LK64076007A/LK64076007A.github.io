---
layout: post
title: Mute commercials on CBS or Hulu with Keyboard Maestro
date: 2013-03-12 10:42 
tags:
- technology
- Keyboard Maestro 
---

In a game of one-upmanship, I've improved on my prior macros for muting commercials on CBS and Hulu. What used to be 1-3 non-annoying commercials[^1363103721-fn1] has turned into five, highly-annoying, commercials in a row. The volume is often much louder than the volume of the show and not infrequently, the same commercial is played all 5 times.

To combat this I made two small changes. First, I combined the two macros into one so I don't have to remember two hot keys or which site I'm watching. A simple Applescript snippet captures the URL from Chrome and an if/then statement looks for the network name in the url. The second change involves turning the screen off and on in addition to toggling the mute key.

The macro flows thus:

<pre>
- Execute Applescript `tell application "Google Chrome" to get the URL of active tab of first window` and save results to variable `currentURL`
- If `currentURL` contains CBS then
    - Toggle system sound mute
    - Repeat action 16 times: decrease screen brightness
    - Execute following action until none of the conditions are met
        - none (this is basically just a pause until)
        - Conditions: screen contains image (the image is the "advertisement" graphic that is displayed during a commercial)
    - Toggle system sound mute
    - Repeat action 16 times: increase screen brightness
- otherwise execute the following
    - If `currentURL` contains hulu then
        - Toggle system sound mute
        - Repeat action 16 times: decrease screen brightness
        - Execute following action until none of the conditions are met
            - none (this is basically just a pause until)
            - Conditions: screen contains image (the image is the "advertisement" graphic that is displayed during a commercial)
        - Toggle system sound mute
        - Repeat action 16 times: increase screen brightness
    - otherwise do nothing
</pre>

I haven't figured out a way to automatically call this macro when the commercials start. I could watch for the "advertisement" graphic but I think that would be way too CPU intensive. I'll keep thinking about it.

I encourage you to make your own macro to learn the system, and you might have to in order to get the correct "advertisement" graphic, but you can get mine [here](/images/mute_Commercials.kmmacros). (right click to download)

[^1363103721-fn1]: I assume this had to do with the newness of the medium was not attractive the old school advertisers and in addition the commercials were aimed at a younger, techophilic demographic. Now I just see lots of car commercials.