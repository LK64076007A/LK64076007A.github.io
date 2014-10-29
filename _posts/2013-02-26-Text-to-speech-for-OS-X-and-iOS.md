---
layout: post
title: Text-to-speech for OS X and iOS
date: 2013-02-26 9:45  
tags: technology, article, text-to-speech, iOS, OS X
---

## Introduction ##

I love to read and have to read a lot for my work and hobbies, but sometimes, for various reasons, reading is not ideal. Maybe my eyes are tired. Maybe I need to do something physical that precludes the physical act of reading but not the mental aspect.[^201302261054] In those situations, I let my software read to me with text-to-speech. 

## Text-to-speech on iOS ##

Text-to-speech on iOS is already built into the OS. To turn it on go to `Settings > General > Accessibility > Speak Selection` and turn it on. You can also switch the dialect if you want.[^1302260948] From now on, when you highlight any text, one of the options on the pop up menu will be "speak". Hit this and the text will be read to you. There is a major limitation with this: **if you lock the device or switch to a different application, the reading stops.**

Another option is a dedicated app. [A colleague](https://twitter.com/SiMBa37) recommends [Voice Dream Reader](https://itunes.apple.com/us/app/voice-dream-reader-text-to/id496177674?mt=8&partnerId=30&siteID=l8AT4zEd6Ao) for 10 USD in the App Store. I have not used it so I can't comment on it.

## Text-to-speech on OS X ##

OS X also has built-in text-to-speech software. As far as I can tell, it is always on, but that may be a left over preference on my machine from years back so to check, go to  `System Preferences > Dictation & Speech`. I also turn on the keyboard shortcut for this. Otherwise, all you need to do is highlight some text, right click, and select `Speech > Start Speaking`. 

I use this frequently when reading an article and I get tired, or I need to be doing something else like cooking at the same time. I've also found that just turning this on when reading something important like a medical journal article lets others know I'm doing something work related rather than just surfing the internet for memes, i.e. don't interrupt. It is also a great way to proof read your writing. What your eyes often miss, your ears will clearly hear.

## Text-to-speech OS X to iOS ##

Sometimes there is a very large article I want to read but don't want to sit at my machine for an extended period to time. Thankfully, OS X has some built in functions that allow you to turn the text into an audio file using the text-to-speech functions. OS X comes with this ability pre-programmed in the services section. To turn it on, go to `System Preferences > Keyboard > Keyboard Shortcuts > Services > Text` and make sure `Add to iTunes as a Spoken…` is checked. From then on, when you have text highlighted, you can right click, go to Services, and click on `Add to iTunes as a Spoken…`. This will convert the text-to-speech, first as a lossless AIFF (a very large file). It will then re-encode using AAC (to make it a smaller file) and then import into iTunes under a special playlist. 

This works fine in general, but I don't usually sync my iPhone with iTunes as I keep most things in the cloud. Thankfully, Automator[^1302261013] makes it very easy to create your own.[^201302261023]

[![](/images/AutomatorTTS.png)](/images/AutomatorTTS.png) 

This creates a service for when text is selected. You run it the same as the prior service: right click, go to Services, and click on `The Name of the Service`. It changes the text to audio format, saving to the location of your choice, and using the voice of your choice. It then re-encodes the file to a format most compatible with spoken word, thus greatly decreasing the file size, and deletes the original file. I have it save to a folder inside Dropbox so that I can play it later (or sooner) on any device I have.

[^1302260948]:  I prefer Australian English.

[^1302261013]:  A built-in part of OS X.

[^201302261023]: Or just take mine.

[^201302261054]: Cooking, doing dishes, folding laundry.