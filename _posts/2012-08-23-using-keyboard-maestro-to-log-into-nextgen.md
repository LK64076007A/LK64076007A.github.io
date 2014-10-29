---
layout: post
title: Using Keyboard Maestro to log into Nextgen
date: 2012-08-23 16:08  
tags: Keyboard Maestro, EMR, technology, programming, medicine
---

It takes me about 45-60 seconds to log into my EMR due to human frailty, distractions and a shit EMR. To speed up the process, allow me to do other things with that time, and keep my anger in check, I set up Keyboard Maestro to login for me:

<video width="640" height="480" controls="controls">
  <source src="/images/KM_to_log_in_to_Nextgen.mov" type="video/mp4" />
  Your browser does not support the video tag.
</video>

The video makes it look easy. In reality, due to vagaries of the Citrix Viewer and variable speed of the network[^120823161512], I had to make a lot of Until loops to continue to check for the right window being ready and at the front before starting the next phase of the log in.

[^120823161512]: At 6:30 am, the network is fast, but when everyone starts to log in at 8am, the thing slows to a crawl.