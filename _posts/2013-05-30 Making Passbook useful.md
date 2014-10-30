---
layout: post
title: Making Passbook useful  
date: 2013-05-30 15:44  
tags:
- technology
- Passbook
---

I shop for groceries at Harris Teeter[^20130530160464]. If you use their loyalty card, the prices are much cheaper.[^20130530160545] I don't like to carry a loyalty card on me, either in my wallet or on my keychain.[^20130530160716] I used to leave the loyalty card in my car, but then I'd forget to bring it into the store with me.[^20130530160833] They have an [iPhone app](. https://itunes.apple.com/us/app/ht-mobile/id422306980?mt=8&at=11l4RT)[^20130530160955] that includes a scannable loyalty card, but it's slow and poorly designed. I would have to remember to open it up while I was on the last aisle in order to give it enough time to load and, it seemed, download the card from a server somewhere. This was unacceptably slow. So my work around was to take a screen shot of the loyalty card and just display that. It worked better, but was still not elegant.

So with help and prompting from [some guy I met on the internet](https://twitter.com/waynehartman)[^20130530161214], I made a location-based Passbook card that pulls up the loyalty card's barcode whenever I'm at the store.

I used the website [Passdock](https://api.passdock.com/users/sign_up/) to create the card using one of their templates. I wasn't able to create the barcode programmatically because Harris Teeter doesn't use one of the approved barcode styles for Passbook. Instead, I trimmed out the barcode from the screenshot I had taken and put that in the place of the logo. I used the built in DigitalColor Meter app in OS X to make the colors match and put in the GPS coordinates to make sure it would appear whenever I was at the store. It took a little debugging at first, but it works perfectly.

Now, rather than being annoyed whenever I'm checking out, I get a little flush of satisfaction.

[^20130530160464]: Don't be creepy™.

[^20130530160545]: Or maybe they're much more expensive to begin with and only reasonable with the loyalty card.

[^20130530160716]: Minimalism is cool, right?

[^20130530160833]: Remembering things is hard.

[^20130530160955]: And [Android too](https://play.google.com/store/apps/details?id=com.harristeeter.htmobile&hl=en).

[^20130530161214]: What a wonderful day it will be when I hear those words from my daughter's mouth.