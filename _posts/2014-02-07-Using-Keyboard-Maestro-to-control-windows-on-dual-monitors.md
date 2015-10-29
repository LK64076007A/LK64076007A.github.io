---
layout: post
title: Using Keyboard Maestro to control windows on dual monitors
date: 2014-02-07 16:21  
tags:
- technology
- Keyboard Maestro
---

I just started using a second monitor at work[^140207162201]. The problem was that every time I would plug my Macbook Air into the monitor via the Thunderbolt connection, the previously arranged window position was lost. I have a very simple arrangement: my text editor maximized on my laptop, and the EMR maximized on the external screen. 

**Keyboard Maestro to the rescue.**

[![](/images/Keyboard_Maestro_Dual_Screens.png)](/images/Keyboard_Maestro_Dual_Screens.png) 

The main actions just move the desired application window to the top left of the respective screens, `SCREEN(1,` for the laptop screen and `SCREEN(2,` for the external monitor. The `+22` for the downward direction moves the window down below the menu bar, which is 22 pixels tall. The `-22` for the window height subtracts the menu height from the total window height so you don't lose the last 22 pixels below the screen. 

The hardest part of this macro is figuring out that you can type these commands into the action. Normally the action looks like this:

[![](/images/Move_and_resize_1.png)](/images/Move_and_resize_1.png) 

It looks like you can only input numbers[^140207163434], but if you start typing, it will transform to this:

[![](/images/Move_and_resize_2.png)](/images/Move_and_resize_2.png)

**Update:** From the Yahoo Keyboard Maestro user group, I found more information on picking which screen you’re giving instructions to. 

- Numbers: designates the screens from left to right. 1, 2, 3…
- Main and Secondary: main refers to whatever screen is currently being used by the active window/application
- Internal and External: the iMac/laptop display versus the external display

You can use these various designations depending on your use case. For example, I was originally using numbers, but that meant I had to have two separate macros for making a window maximized, one for the main monitor and one for the external, but by changing the `1` and `2` to `main`, it will maximize the window that has the focus on that screen. They have slightly different meanings, but this allows different functionality. 

[^140207162201]: The EMR we use is so poorly arranged that a larger screen is needed to make up for the poor design.

[^140207163434]: This has screwed me up several times when trying to create an action. It is not always obvious that another type of input is possible.