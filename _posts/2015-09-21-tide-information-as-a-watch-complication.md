---
layout: post
title: Tide information as a watch complication
date: 2015-09-21 9:40:57 -0500
tags: 
- sailing
- complications
- Apple Watch
- development
- UI design
--- 

<!-- Apple will never do a watch face that shows the tide level at my local beach. And I *really* want that before I head out on a dog walk. - https://twitter.com/chockenberry/status/579347014443384832 -->

Six months ago, Craig Hockenberry tweeted

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Apple will never do a watch face that shows the tide level at my local beach. And I *really* want that before I head out on a dog walk.</p>&mdash; Craig Hockenberry (@chockenberry) <a href="https://twitter.com/chockenberry/status/579347014443384832">March 21, 2015</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This was over a month before the Apple Watch was released, but I also wanted the same. At the time, my sailboat was at a marina with very little depth at low tide. I needed to plan my departures and arrivals based on the tide. Being able get the tidal information at a glance would be beneficial and much more important to me than things like temperature, sunset time, or moon phase.[^150921100200] 

Although watchOS 2 has been [delayed][techcrunch], the GM is out and at least one app with a complication has been published to the App Store.[^150921134514] 

[My Tide Times Pro][apple] has been updated with a watch complication to show the time of the next low or high tide, and depending on the complication, it's name and height. 

<img src="/images/tide_watch_complication-1.jpg"  width="314" height="195">

I was already using [My Tide Times Pro][apple] as my tidal app of choice[^150921102250] so this is a very welcome addition; however, there was one major, but fixable issue. Actually getting the complication to work was completely unintuitive.

I was ecstatic when I first saw the app update in the store and immediately downloaded it. I then made sure the complication was active in the Watch App, and went to enable it on my watch face. I switch between multiple watch faces depending on my activity, but I use Chronograph frequently. Unfortunately, the [My Tide Times Pro][apple] does not show up as an option for those complications. I then switched to the modular face where it did show up as an option, but when I selected it nothing appeared except `-`. 

<img src="/images/tide_watch_complication-2.jpg"  width="156" height="195">

I switched back and forth to the app on both the phone and the watch, restarting, uninstalling and reinstalling, all to no avail. There was no prompt, instructions, or other hints that I found. I assumed that something must be broken since I'm technically on "beta" software and went on my way.

Then a few days ago, I happened to create a new modular face, but instead of putting the tides in one of the small complication slots, I put it in the large central slots. Initially it was just as useless

<img src="/images/tide_watch_complication-3.jpg"  width="156" height="195">

but the next time I raised my wrist, instructions telling me to force press my local tide in the app to set the complication appeared. 

<img src="/images/tide_watch_complication-4.jpg"  width="156" height="195">

I did so and it worked! 

<img src="/images/tide_watch_complication-5.jpg"  width="156" height="195">

I thought I must have missed something originally, so I deleted the app completely and restarted from scratch. My second experience was identical. The first two times I tried to use the complication failed (first on a face that didn't support it and second on a slot that didn't give me any instructions). That is not a great experience and I wonder if the developer is going to get a lot of email about this from people wondering why it is "broken" or one star reviews in the App Store from asshats with a god complex. I did tag him on my Twitter announcement for this post, and if he writes to me to say I'm an idiot for missing something, I'll post an update.

In the last episode of [Recursion][recursionpodcast] and on [Twitter][twitter], Wayne expressed concerns about <del>force touch</del><ins>3D touch</ins> on the iPhone 6S and 6S+. He is worried developers will use this new interaction method poorly, hiding important functionality behind undiscoverable gestures rather than as a value add to already discoverable and well designed UI. I don't think this was a case of that, but rather a limitation in options given platform constraints, but it does illustrate the issue of discoverable UI. 

## Update

I discussed with Justin, the developer, and he has decided to add a pop up the first time you launch the app on the watch and instructions in the release notes. I think that is about all he can do given the limitations of the platform he is dealing with. It really is a great app and if tide data is important to you, I highly suggest this app. 

[^150921100200]: Wife: When are you going sailing tomorrow? 

	Me (looking at watch): Around 9am.
	
	Wife: When will you be back?
	
	Me: NEVER!!!! (╯_╰”)...um, around 5.	
	
[^150921134514]: Three hours after I published this post, Apple released watchOS 2.0.

[^150921102250]: And I've tried them all: all the apps that just report the tides, and all the apps in which tide data is included, such as expensive navigation apps.

[apple]: https://itunes.apple.com/us/app/my-tide-times-pro-tide-tables/id804031883?mt=8&uo=4&at=11l4RT
[recursionpodcast]: https://recursionpodcast.net/5
[techcrunch]: http://techcrunch.com/2015/09/16/apple-delays-release-of-watchos-2-due-to-bug/
[twitter]: https://twitter.com/waynehartman/status/643417254277726208



