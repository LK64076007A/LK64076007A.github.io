---
layout: post
title: Create a Markdown link with automatic affiliate codes
date: 2014-08-01 0:49  
tags: 
- Keyboard Maestro
---
I do a podcast with a couple other guys. As we're recording the show, I like to create the show notes live so that they're most accurate and save myself time later. We frequently mention products on Amazon, apps on iTunes, and regular old-fashioned links. I created the following macro for myself so that after I've navigated to the webpage of the link in Safari, I can automatically create a Markdown-style link in my text editor, including optional Amazon and iTunes affiliate links if appropriate. The affiliate links are added using python scrips from [Dr. Drang][1] and [Brett Kelly][2].

The macro can be triggered by the string `mdlink` of the hotkey ⇧⌃⌥⌘p.

Since I write all my show notes in nvALT and my workflow is to find the webpage in Safari, the first part of the macro activates nvALT. The topmost Safari URL is then saved to the clipboard. The clipboard is then parsed by two If statements looking to see if it is an Amazon or iTunes link, and if it is add the affiliate code. Finally, the text for the Markdown link in inserted using the Safari title as the text for the link.

## Macro Text

My Macros  
mdlink  
Triggered by any of the following:  
The exact case string ‘mdlink’ is typed (then deleted)  
The Hot Key ⌃⌥⇧⌘P is pressed  
Will execute the following actions:  
Activate nvALT  
Set Clipboard to Text  
%SafariURL%  
If All Conditions Met  
The clipboard text contains ‘itunes.apple.com’  
Execute the Following Actions:  
Execute Shell Script  

    #!/usr/bin/python
    
    # Via Dr. Drang
    # http://www.leancrew.com/all-this/2013/08/new-apple-affiliate-link-scripts/
    
    from subprocess import check_output
    from sys import stdout
    
    # My affiliate ID.
    myID = '11l4RT'
    
    # Get the URL from the clipboard.
    clipURL = check_output('pbpaste')
    
    # Add my ID and the partnerId parameter to the URL. If there are already
    # queries, add them as additional ones; if not, add them as the only ones.
    if '?' in clipURL:
    itemURL = '%s&at=%s' % (clipURL, myID)
    else:
    itemURL = '%s?at=%s' % (clipURL, myID)
    
    # Write it out
    stdout.write(itemURL)
Save trimmed to Clipboard.  

If All Conditions Met  
The clipboard text contains ‘amazon.com’  
Execute the Following Actions:  
Execute Shell Script  

    #!/usr/bin/env python
    
    # (c) 2012 Brett Kelly.
    # Licensed under the MIT license
    # http://www.opensource.org/licenses/mit-license.php
    # http://nerdgap.com/amazon-affiliate-links-with-textexpander/
    # Some edits from the original to get to to work in KM - ML
    
    import re
    import sys
    from urlparse import urlparse
    from subprocess import check_output
    
    ## PUT YOUR AFFILIATE CODE HERE
    affcode = 'violeneces-20'
    
    rawurl = check_output('pbpaste')
    
    ## Get the base url without all of the query string malarky
    baseurl = rawurl.split('?')[0] 
    
    try:
    parts = urlparse(baseurl)
    except Exception:
    sys.stdout.write(rawurl)
    raise SystemExit
    
    ## Make sure it's actually an Amazon URL
    amazonre = re.compile('[www\.]{0,1}amazon\.')
    
    if not amazonre.search(parts.netloc):
    # Not an amazon URL, return whatever was passed initially
    sys.stdout.write(rawurl)
    raise SystemExit
    
    # Format the simpler URL and append the affiliate code
    goodurl = "%s://%s%s?tag=%s" % (parts.scheme,parts.netloc,parts.path,affcode)
    
    # Write formatted URL to STDOUT
    sys.stdout.write(goodurl)

Save trimmed to Clipboard.  
Insert Text by Pasting  
\[%SafariTitle%](%CurrentClipboard%)  

# Macro Image

[![Macro Image](/images/Markdown_link_with_affiliate_codes.jpg)](/images/Markdown_link_with_affiliate_codes.jpg) 

[Download the macro](https://dl.dropboxusercontent.com/u/3950369/blog_images/Create%20Markdown%20link%20with%20affiliate%20codes.kmmacros). 



  [1]: http://www.leancrew.com/all-this/2013/08/new-apple-affiliate-link-scripts/
  [2]: http://nerdgap.com/amazon-affiliate-links-with-textexpander/