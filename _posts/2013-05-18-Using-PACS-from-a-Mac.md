---
layout: post
title: Using PACS from a Mac
date: 2013-05-18 18:42  
tags: EMR, medicine, technology
---

The title is a bit misleading, but I figured that's what people would be searching for if they had the problem I'm intending to solve.

Technically, this article is about installing virtual Windows machines for free on your Mac so you can use PACS rather than about how to use PACS on a Mac, because, as far as I know, you can't.

A colleague uses a Macbook Air at work except the hospitals imaging system uses PACS with some unfortunate software requirements:

1. Internet Explorer 6.0, 7.0, or 8.0
2. Windows XP (Service Pack 3) or Windows Vista Home Premium or Windows Vista Business 64 bit or Windows 7 32 and 64 bit 
3. Windows 3.1 Installer
4. Microsoft .NET Framework 3.5 (Service Pack 1)
5. Windows Media Player 11.0

This made him sad because he also had to carry around a crappy Windows machine.

Thankfully, we were able to easily solve his problem today.[^20130518185423]

The technique we used came from a [2 year old article](http://osxdaily.com/2011/09/04/internet-explorer-for-mac-ie7-ie8-ie-9-free/) from [OSXDaily](http://osxdaily.com). It uses VirtualBox from Oracle to create a virtual machine and then load a free version of Windows XP for the purposes of testing IE.

The technique is really pretty simple, although you need to not fear the terminal.

First, [download and install Virtual Box](https://www.virtualbox.org/wiki/Downloads).

Second, go to the terminal[^20130518191266] and paste one of the following depending on the version of Internet Explorer you need:

- Internet Explorer 7

`curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | IEVMS_VERSIONS="7" bash`

- Internet Explorer 8

`curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | IEVMS_VERSIONS="8" bash`

- Internet Explorer 9

`curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | IEVMS_VERSIONS="9" bash`

In everything goes well, this will install the Windows operating system needed and the version of IE as well.

Finally, run the application VirtualBox and you'll be able to boot up the Windows virtual machine.

If you have trouble doing that there are several more resources that can help:

- [Microsoft's virtualization website](http://www.modern.ie/en-us/virtualization-tools). You can pick from Windows XP, Vista, 7, and 8.

- [Chris Warton's blog](http://chriswharton.me/2013/02/installing-modern-ie-virtualization-on-virtualbox-for-mac/). Has some tips on installing one of the above Windowns virtual machines into Virtual Box. 

- [Greg Thornton's Github repository](https://github.com/xdissent/ievms) for automatic installation of Window's VMs. Has more detailed instructions.

Let me know if this works for your and allows you to use PACS on your Mac. I'd be interested to know how much this is effecting physicians. 


[^20130518185423]: Actually, it took forever to figure it out. While this technique worked perfectly on my Macbook Air 13 inch, for some reason it would immediately fail on his machine. For some reason, the installer couldn't make the hidden directory `.revms` in his User folder. Once we figured that out, un-hide the hidden files, and created it manually, it worked fine. Took forever to figure that part out though.

[^20130518191266]: Terminal.app or ⌘-space, `terminal`.