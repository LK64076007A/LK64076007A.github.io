---
layout: post
title: Saving sequential webpages as PDFs with Keyboard Maestro
date: 2012-10-13 8:06  
tags: Keyboard Maestro, technology, programming  
---

I needed to save as PDF a series of 80 webpages on a slow server on a password protected website. I could have sat there for an hour doing it manually, but since I wanted to get dressed and have a cup of coffee, I made a Keyboard Macro shortcut instead.

[![](/images/Saving_with_KM.png)](/images/Saving_with_KM.png) 

In order to use this macro, you need to set up a very useful shortcut for saving files to PDF. In the stock OS, you hit ⌘-P (Command-P) to bring up the print dialogue box and then in the bottom left hand corner of the pop up menu click the down arrow by PDF and choose save as PDF. **A much faster way  to do this,** is to create a system shortcut that allows you to hit ⌘-P twice to initiate the save as PDF action. I learned this from MacSparky and [still go to his page every time to remember how to set it up](http://macsparky.com/2008/3/19/keyboard-shortcut-for-save-as-pdf-in-os-x.html "still go to his page every time to remember how to set it up").

The first two steps are to set up some incrementing variables to allow the files to be named with sequential numbers. If the webpages you're saving have unique names, this won't be necessary, but for my case it was.[^1210130817] 

The rest of the code is in a repeat loop. Since I knew it was going to be exactly 80 repeats, it was easier to do it this way than a while, or if loop. 

The first part of the real code is to initiate the save as command with ⌘-P twice.

Then the file name is entered with the last digit being placed by a variable that will increment by +1 with every new name. Since the saving dialog seemed to take awhile, I added a pause into the mix. Then ⌘-down arrow moves the whole webpage to the very bottom where the "next page" button is. Keyboard Maestro has a powerful function to find images on a webpage and then use that image. In this case, when it sees the image of the next button, it left clicks the mouse in the center of the button. 

The pages are slow to load, so I have a pause in there until the screen contains the image of a circular arrow. This is the refresh button in Safari and only shows up once a page is loaded. It's an easy hack to make sure the next page is loaded. 

And then this cycle repeats itself until all the pages were saved. It worked perfectly.

I didn't even have time to do my hair and finish my coffee.

[^1210130817]:  Setting the constant 1 to the variable i was probably unnecessary, but I was trying to get this done quickly, not elegantly. 