---
layout: post
title: Forced productivity with Keyboard Maestro
date: 2013-11-20 17:04  
tags:
- technology
- medicine
---

I get easily distracted. I can be working on task A, which reminds be to do task B, then get into task C, and end up working 3 hours on task C, then back to 2 hours on task B, and finally get back to task A many hours later. Most of the time this isn't a problem, and makes me very productive. Not so much at work. Writing an epic blog post or researching the perfect way to make ginger chicken at work--not such a good idea.

So, I made a quick Keyboard Maestro macro to force productivity:

> While logged in, repeating every 1 minute during the hours of 8am-5:30pm Monday through Friday:

> If my medical record app or my text editing app are not at the front, then:
> 
> 1. Quit the front application
> 2. Open my medical record app 

Brutal, but efficient.[^131120203050]

[^131120203050]: I could make it even more cruel but quitting any app that isn't my medical record app or text editor app anytime I switched to the a new app, but that's a little extreme. At least now I have up to 60 seconds to look something up.