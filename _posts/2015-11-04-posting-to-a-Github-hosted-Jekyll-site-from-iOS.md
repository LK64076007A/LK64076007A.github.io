---
layout: post
title: Posting to a Github hosted Jekyll site from iOS
date: 2015-11-04 21:20:00 -0500
tags: 
- Github
- Jekyll
- Git2Go
- Working Copy
- Byword
---

Using a Github-hosted, Jekyll blog, I normally write my posts on my laptop, committing and pushing the final product in terminal. While this works well enough most of the time, I do actually like to use my iPhone as my primary computing device and want to be able to do everything as well on it as on my laptop. Frequently I don't want to carry my laptop with me. Sometimes an idea for a post will come to me while I'm out camping, on a walk, or sailing. 

So, how can you post to Github from iOS?

# Directly on the website

As far as I can tell, there is no way to create or edit a text file on the Github.com mobile site. 

# Directly on the website forcing desktop version

You can create and edit text files on the desktop version of the website. The drawbacks are that if you are writing into the field form on the website and lose your connection, you will most likely lose your data. You cannot work offline. You cannot use shortcut optimizations such as TextExpander.[^151105095448] Basically, the experience is non-native. You could write in a text editor and then copy and paste into the form field, but including the logging in and navigation, it is a clunky experience.

# Using a code editor

I thought that something as powerful as [Coda for iOS](https://itunes.apple.com/us/app/coda-for-ios/id500906297?mt=8&uo=4&at=11l4RT) might be my answer. They support SSH and FTP. Their screenshots show them managing their own website with it. After downloading it and failing to get it to work, I shot off an email to support asking for help. 

> Unfortunately Coda for iOS does not currently have support for git. This is something that we are considering for a future update but in all honesty I can’t say for certain when it will be added.

I couldn't get [Textastic](https://itunes.apple.com/us/app/textastic-code-editor-for/id550156166?mt=8&uo=4&at=11l4RT) to work either.

# Using a Github client iOS app

I've looked for Github apps before and never found anything that worked well, was being actively maintained, or looked halfway decent. That is why I didn't start by looking at that solution, but I should have because that ended up solving my problem. 

## Working Copy

The first app I came across was [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT). This app is free to use up until the point you need to push commits, and then it is either $2 for 21 days or $10 for permanent unlock. This allows you to make sure you like the app and it works for you before committing to the purchase.[^151105200728]

[Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT) easily logs into Github using your username and password, and allows you to clone your repositories. You can then browse and manage your files as needed. I won't go into all the specifics of how it works as I'm not a Git power user, but for my purposes of creating and submitting text files, it works well. You cannot edit files directly in Working Copy, but it has been designed to work well with exporting to Textastic, Byword, or Editorial, and then bringing the files back into the app. All of the aforementioned apps are superior text and code editors, which I also already happen to own, so it makes a lot of sense to use them rather than having the [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT) developers wasting valuable time solving already solved problems.

[Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT) has been around since 11/2014, gets updates every 1-2 months, and has an impressive ★★★★★ review total for lifetime and current version.

## Git2Go
I subsequently came across [Git2Go](https://itunes.apple.com/us/app/git2go-git-client-you-always/id963577401?mt=8&uo=4&at=11l4RT) by [Nerdishbynature](http://nerdishbynature.com/feed.xml). This app was just released a few weeks ago and is on version 1.0[^151105221354] with a ★★★★ and 1/2 review total. Only two reviews weren't 5 stars, and the 1 star review basically said the app only showed repos and nothing else, which I can attest is wrong. 

Logging in to Github is easy and uses Oauth with Safari View Controller. It literally took me 3 clicks on my iPad and 1 click on my iPhone. Unlike [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT), you can edit files in the app and syntax highlighting for Objective-C, Swift, and Ruby is currently supported with the [developers noting their plans to add others later](https://twitter.com/Git2Go/status/659224986763202564).  Oddly enough, they only charge for cloning private repositories. This is a bit of a "problem" for me since I don't have any private repositories and therefore cannot give them any money unless I create one. I've requested they add a tip jar, but I also think they might want to figure out a different monetization strategy. 

# Conclusions

I'm not sure if I'm going to stick with [Git2Go](https://itunes.apple.com/us/app/git2go-git-client-you-always/id963577401?mt=8&uo=4&at=11l4RT) or [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT). I like them both and will likely continue to monitor their development. Byword is my favorite text editor after BBEdit, and the ability to seamlessly move between devices using iCloud sync is nice. If you prefer a code editor, Textastic is great too. On the other hand, being able to make a quick change to some code, or a spelling mistake on a blog post, right from an app is going to be much easier and quicker with Git2Go as you won't have to make a round trip to another app and back. 

Either way, it is now possible for me to publish and edit posts easily, quickly, and enjoyably on my Github-hosted Jekyll blog. 

This post was written in Byword on an iPhone 6. 

[^151105095448]: When I tried to use the TextExpander keyboard on iOS 9.0, Safari would crash.

[^151105200728]: Unlike Coda for iOS that required I file for a refund.

[^151105221354]: Literally while I was writing this they released 1.1.
