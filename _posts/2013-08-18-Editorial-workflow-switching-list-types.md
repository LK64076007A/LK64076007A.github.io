---
layout: post
title: Editorial workflow - switching list types
date: 2013-08-18 18:53 
tags: apps, workflow, technology 
---

I've had Editorial for less than an hour and I've made my first workflow. 

I create my hacks as I need them and shortly after I starting writing I needed to change an unordered list to an ordered list. 

First, I picked the action that outputs the selected text from the document. I then did a regex search for `^(\s*)[-*] `[^130818233455] to find the beginning of each line starting with the preface for an unordered list and replace it with `$11. `. The input is then used to replace the selected text in the document.

This was a good start but I wanted to be able to easily switch back and forth. I put those three actions inside an `if` action so that it only fires if it finds that there is a line starting with `-`. I added a `stop` action inside the `if` action to end the workflow once the if statement runs. I then added another `if` action that is basically the same except looks for lines starting with `1. ` and replaces them with `- `. 

Finally, I added an action at the beginning of the workflow that extends the selected text to the beginning and end of the lines to make selecting text a bit easier. 

You can download this workflow [here](http://editorial-app.appspot.com/workflow/5530680926666752/dS2_NO1n8U8).

[^130818233455]: The `\s` accounts for any preceding whitespace (tabs or spaces) and the `[-*]` looks for either possible syntax for bulleted lists.