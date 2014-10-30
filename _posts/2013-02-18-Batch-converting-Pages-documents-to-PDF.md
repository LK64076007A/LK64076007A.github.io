---
layout: post
title: Batch converting Pages documents to PDF with Keyboard Maestro
date: 2013-02-18 16:38  
tags: 
- Keyboard Maestro
---

I had 3000 Pages documents that I wanted to convert PDF. I had previously searched the internet for a way to do this easily but was unsuccessful. I suppose I should have tried searching again, because I would have found [Pages2PDF][yourmacteacher], which works much better than what I did. 

Still, relying on someone to create the exact program you need is not as fun or as useful as being able to fix the problem yourself. So I created a Keyboard Maestro macro.

Basically, this automates the steps I would have had to do manually:

1. Open the file in Pages.
1. Select Export to PDF from the menu.
1. Fix the file name.[^130218165655]
1. Move the original file to a new location.

In Keyboard Maestro parlance the steps were:

- For Each Item in a the Finder's selection
    1. Set the file name to a variable fileName
    1. Set the file path to a variable filePath
    1. Open the file at filePath/fileName[^130218170000] in Pages.
    1. Pause for 1.5 seconds.[^130218170107]
    1. Select the menu item PDF… in the submenu Export in the Menu Title File.
    1. Press the Button labeled "Next…"
    1. Insert the text from variable %WindowName%1% by pasting. (Basically, this names the file being exported the same as the original file name, except for the extension.)
    1. Press the button labeled "Export".
    1. Type the keystroke ?-W (to close the open file)
    1. Move the file %Variable%filePath%/%Variable%fileName% to whateverLocationYouWant/%Variable%fileName%

It worked perfectly if somewhat slow. It took several hours to process all the files. 

[![][dropbox]][dropbox] 

[dropbox]: /images/PagestoPDF.png
[yourmacteacher]: http://www.yourmacteacher.com/batch-convert-pages-documents-to-pdf/

[^130218165655]: For some reason, Pages kept truncating my filenames.

[^130218170000]: I don't know why I had to specifically use the path and name. Sometimes KM works fine without that and sometimes it doesn't. I haven't figured out why and when.

[^130218170107]: I didn't test this step any. I just assumed KM would need time for the document to fully open in Pages.