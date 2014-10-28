---
layout: post
title: Keyboard Maestro macro screenshots
date: 2014-07-29 17:25  
tags: KeyboardMaestro
---
I create a lot of macros with KM and I like to share them both on this blog as well as in the KM forums[^140729172855]. Taking screenshots of the macro is an important part of this sharing and has been very useful to me as I have learned to use KM from my betters in the community. Previously, I would use the standard screen shot functions of OS X, but with very long macros that did not all fit on one screen there was no elegant solution.

I believe it was in [6.0](http://www.keyboardmaestro.com/documentation/6/keyboardmaestro.html) that Peter added the ability to copy a macro as an image. I failed to pay much attention to this at the time in light of all the other great functionality, but recently put it to use.

The copy as an image puts the highlighted portion of your macro into the clipboard. By itself, this isn't very useful because I need an actual image to upload to the blog, and as far as I can tell that functionality is not built in[^140729173600]. 

So I created a macro.

## Macro description

You can either select individual parts of the macro you want to share, or select nothing and the whole macro will be used.

Using a hotkey, trigger the _Create Screenshot Macro_.

1. Select the `copy as image` from the menu
2. Prompt the user for the file name
3. Save the file to the desktop

There's also a `copy as text` if you want to just share the text of the macro. I prefer to write my own descriptions because I think it's more useful, but including the text is nice too. See below.

## Macro text

Create screenshot of KM macro  
Triggered by any of the following:  
The Hot Key ⌃⌥⇧⌘M is pressed  
Will execute the following actions:  
Select Menu Item in Keyboard Maestro  
Select: Edit ⇢ Copy as ⇢ Copy as Image  
Stop macro if menu cannot be selected.  
Prompt for User Input ‘File Name’  
What do you want to call the file?  
Input the following variables:  
File Name  
Finish with the following buttons:  
OK  
Cancel (cancel macro)  
Store button pressed in variable ‘Result Button’.  
Write Clipboard  
To file: ~/Desktop/%Variable%File Name%.jpg  
With format JPEG).  

## Macro image

[![Macro Image](https://dl.dropboxusercontent.com/u/3950369/blog_images/Create%20KM%20screenshot%20image.jpg)](https://dl.dropboxusercontent.com/u/3950369/blog_images/Create%20KM%20screenshot%20image.jpg) 

[Download the macro](https://dl.dropboxusercontent.com/u/3950369/blog_images/Create%20screenshot%20of%20KM%20macro.kmmacros).

## Room for improvement

I would like the ability to automatically name the jpg with the name of the macro. 

[^140729172855]: If you use KM and aren't in the forums, you are really missing out.

[^140729173600]: Is this an oversight, am I missing it, or is this deliberate on Peter's part because he wants the user to create the macro by themselves?