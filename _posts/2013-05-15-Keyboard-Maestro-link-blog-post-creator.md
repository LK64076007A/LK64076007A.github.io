---
layout: post
title: Keyboard Maestro link-blog post creator for Scriptogram
date: 2013-05-15 19:22  
tags:
- Keyboard Maestro
- technology
- Scriptogram
- blogging
---

I created a Keyboard Maestro macro to quickly create a link-blog post to Scriptogram without even needing to open a text editor.

The workflow is straight forward and assumes that you are _reading a website in Safari and have already copied the quote you want to the clipboard_:

1. You are prompted for an attribution (either the author or the website you're quoting), the title of your post which will also be used as the url of your post and part of the file name, tags (optional), and comments (optional).
2. The url of the frontmost tab in Safari is saved as a variable.
3. Text is written to a file.

[![](/images/Quick_link-blog_macro_image.png)](/images/Quick_link-blog_macro_image.png)

Only three steps. The real power is in what text is written to a file and the name of the file.

The text is just the boilerplate of a Scriptogram blog post with variables to fill in the data.

    Title: %Variable%Post Title%
    Date: %ICUDateTime%yyyy-M-d HH:mm%
    Link: %Variable%currentURL%
    Tags: %Variable%Tags%
    
    [%Variable%Attribution%](%Variable%currentURL%):
    
    > %CurrentClipboard%
    
    %Variable%Comments%

The text is written to a new file each time as long as the date and post title are unique. I like my file name to consist of the date and the post title as follows:

    /Users/michael/Dropbox/Apps/scriptogram/posts/%ICUDateTime%yyyy-M-d% %Variable%Post Title%.md

Took me all of 5-10 minutes. I surprised myself getting the whole thing correct on the first try. Typically it takes me half an hour to get the format of the macro set up and another 2 hours debugging it.