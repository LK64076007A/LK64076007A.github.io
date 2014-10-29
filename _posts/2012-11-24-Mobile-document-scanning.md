---
layout: post
title: Mobile document scanning
date: 2012-11-24 21:50  
tags: technology, apps, scanning
---

# Summary

Scan documents with your smartphone, sync to your home computer with Dropbox, and have them automatically OCR'd so they're searchable later.

# tl;dr

Yesterday, I mentioned that one of the consistent apps on my home screen is [Scanner Pro] [apple]. It is a simple and elegant app with a straight forward purpose: take pictures of documents, save them as PDFs, and upload them to cloud-based services. 

In the digital age in which many of us are trying to live a [Paperless][macsparky] lifestyle, converting paper documents to digital ones is a necessary evil. Scanners of various types are necessary for this task. There is a continuum of power versus portability when it comes to scanners. The more powerful are less portable; the most portable are usually not that powerful. 

At work, where I don't need to be portable, but need lots of power to scan hundreds of pages of double-sided documents and auto-rotate the occasional upside down page, I use the [Fujistu ScanSnap S1500M][amazon], and I wouldn't want to use anything else. At home, where I'm a bit more portable, and typically am only scanning a few pages at once, I go with the [Doxie Go][amazon 2], which I can also take with me on trips if needed. 

But then there are all the times when I'm not at work or home but want to scan something and that's when I turn to the power of the modern smartphone camera and [Scanner Pro] [apple]. 

I have three requirements when I scan documents. 

First, all documents must be in PDF format. PDF is a universal standard that will not be going away anytime soon, and if it does every become obsolete, there are so many people that have depended on it, there will be many options created to convert PDFs to the next standard. [Scanner Pro] [apple] saves all images in this format. 

Next, I need to be able to access to my documents from any of my devices. This means uploading them to [Dropbox][db]. If you don't know what Dropbox is stop everything now and [go learn][db]. [Seriously][db]. Stop! Don't read another word. [GO][db]. [GET][db]. [DROPBOX][db]. [Scanner Pro] [apple] can upload to Dropbox (and a bunch of other Cloud services I don't use) and can be set to upload automatically.

Finally, all my documents must be [OCR'd][wikipedia]. Basically, OCR is the process by which software is used to analyze the image of a document and figure out what the characters are. Without OCR you have an unsearchable document that you can't even copy and paste text out of. With OCR you can search for any words inside the document and copy and paste text from it elsewhere. [Scanner Pro] [apple] does not OCR, and frankly, I'm suspicious of any mobile OCR app at this time. I really want quality text conversion and so I prefer to use the more powerful software and processor on my desktop machine. 

To OCR documents uploaded to [Dropbox][db], I have my home computer watch the folder I upload PDFs to from [Scanner Pro] [apple], and when a new PDF is added, an Applescript is called that uses [PDFpen Pro][apple 2] to OCR the document. All credit goes to David Sparks, AKA MacSparky, author of the aforementioned [Paperless ebook][macsparky 2], for the technique to do this. [He wrote about][macsparky 3] using something called Folder Actions that he used to do this. In the comments of this post[^121124223240], there was a link to another site that did a similar thing using Hazel. [I use the Hazel method][documentsnap], because I actually have many folders that are watched and OCR'd in a similar way, and having them all together in one application makes them easier to monitor.

So, when I'm returning the rental car at the end of a business trip, rather than saving the receipt for scanning at home fraught with the perils of trying not to wrinkle it in the carry on bag and also remember to scan it in the first place, I take a quick picture of it with [Scanner Pro] [apple] and forget about it, because it will be uploaded and OCR'd without any more input from me. The next time I need the receipt, I just search for "car rental receipt" in Spotlight and all those kinds of receipts appear.

[amazon]: http://www.amazon.com/Fujitsu-ScanSnap-Instant-Sheet-Fed-Macintosh/dp/B001XWCQO2?tag=violeneces-20
[amazon 2]: http://www.amazon.com/Doxie-Go-Rechargeable-Mobile-Scanner/dp/B0053TRH2M/ref=sr_1_1?tag=violeneces-20
[apple]: https://itunes.apple.com/us/app/scanner-pro-by-readdle/id333710667?mt=8
[apple 2]: https://itunes.apple.com/us/app/pdfpenpro/id403758325?mt=12
[db]: http://db.tt/F6uGmiXz
[documentsnap]: http://www.documentsnap.com/hazel-rule-to-ocr-documents-using-pdfpen/
[macsparky]: http://macsparky.com/paperless/ "Paperless"
[macsparky 2]: http://macsparky.com/paperless/ "Paperless ebook"
[macsparky 3]: http://macsparky.com/blog/2009/5/24/pdfpen-ocr-folder-action-script.html
[wikipedia]: http://en.wikipedia.org/wiki/Optical_character_recognition

[^121124223240]: I know there aren't any there now, but I swear, there used to be comments there.
