---
layout: post
title: Logging time per visit with Keyboard Maestro
date: 2014-02-21 8:14  
tags: Keyboard Maestro, technology, medicine
---

I wanted a better idea of how much time I was spending per visit. This data could also be used when billing by time. I wrote three[^140221081628] small macros to complete this task.

All three macros use the same trigger, ⌘⌥⌃⇧b.[^140221081908] This brings up a menu for me to choose what part of the macro-system I want.

[![](/images/BBT_1.png)](/images/BBT_1.png) 

All three macros also write data to the same log file on my desktop.

## Macro 1 - Start of the visit

I trigger the first macro when I'm walking into the room. It does three simple tasks.

1. Stores the current time of the day in milliseconds to a variable.
1. Displays the current time preceded by the phrase "Visit started at " in a small window on the screen
1. Writes the current time preceded by the phrase "Visit started at " in the log file

[![](/images/BBT_2.png)](/images/BBT_2.png) 

## Macro 2 - End of the visit

I trigger the second macro when I'm walking out of the room. It does 5 simple tasks.

1. Stores the current time of the day in milliseconds to a variable.[^140221082823]
1. Calculates the length of the visit, rounded to the nearest minute.
1. Appends text to the log file with the end time of the visit and the total visit length.
1. Pastes a template phrase required by the government and insurance companies into my clinic note with the length of the visit as calculated above.
1. Displays the various code levels on the screen for each time interval, so I know what billing level to code the visit.

[![](/images/BBT_3.png)](/images/BBT_3.png) 

## Macro 3 - Set a new date

This is just simply appends a break and a date header to the log file. I trigger this before my first visit each morning in order to keep the log file neat and organized. I could automate this, but for each way that I thought to do so, I thought of several possible fail points. 

[![](/images/BBT_4.png)](/images/BBT_4.png) 

[^140221081628]: I'd previously tried to do this with one macro, but had too many complications and bugs. Seperating them out is equivalent to writing well-contained functions. 

[^140221081908]: ⌘⌥⌃⇧ is mapped to the `caps lock` key on all my computer, so it is just one key.

[^140221082823]: Now I have the start time and the end time, in milliseconds, stored to separate variables.