---
layout: post
title: 'Posting to a Github-hosted Jekyll blog on iOS' # quotes allow forbidden characters
date: 2017-06-03 20:31:29 -0500
tags:
- Drafts 
- Workflow 
- Working Copy 
- Jekyll 
- GitHub 
- blogging
- technology
---

[![](/images/BlogpostingtoGithubhostedJerkyblogoniOS1.png)](/images/BlogpostingtoGithubhostedJerkyblogoniOS1.png)

The text all gets written first in [Drafts](https://itunes.apple.com/us/app/drafts-quickly-capture-notes-share-anywhere/id905337691?mt=8&uo=4&at=11l4RT). When writing the text should always come first. Titles, tags, and images are a distraction; they can and should be addressed later. Also, [Drafts](https://itunes.apple.com/us/app/drafts-quickly-capture-notes-share-anywhere/id905337691?mt=8&uo=4&at=11l4RT) is a universally great place to put any text, and those fragments can later turn into posts, making it the perfect place to start.

From [Drafts](https://itunes.apple.com/us/app/drafts-quickly-capture-notes-share-anywhere/id905337691?mt=8&uo=4&at=11l4RT), the text is sent to [Workflow](https://itunes.apple.com/us/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=11l4RT). 

[![](/images/BlogpostingtoGithubhostedJerkyblogoniOS2.png)](/images/BlogpostingtoGithubhostedJerkyblogoniOS2.png)

The command to do this is just a run workflow action with the name of the workflow to be run. 

[![](/images/BlogpostingtoGithubhostedJerkyblogoniOS3.png)](/images/BlogpostingtoGithubhostedJerkyblogoniOS3.png)

The [Drafts](https://itunes.apple.com/us/app/drafts-quickly-capture-notes-share-anywhere/id905337691?mt=8&uo=4&at=11l4RT)'s action can also be created from [Workflow](https://itunes.apple.com/us/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=11l4RT), which takes less taps. 

[![](/images/BlogpostingtoGithubhostedJerkyblogoniOS4.png)](/images/BlogpostingtoGithubhostedJerkyblogoniOS4.png)

A [long, complicated workflow](https://workflow.is/workflows/b98e90b47d334600b6665188c4ef7c43) then

* requests a title 
* requests tags 
* adds correctly formatted metadata[^20170603200740]
* creates a correctly named text file for the Jekyll blogging platform 
* saves the file to the correct path and GitHub account using [Working Copy](https://itunes.apple.com/us/app/working-copy-powerful-git-client/id896694807?mt=8&uo=4&at=11l4RT)

The workflow can even add images. IMAGE1, IMAGE2 etc. are used as text placeholders when writing, then [Workflow](https://itunes.apple.com/us/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=11l4RT) converts those to properly formatted links and requests  the files to be uploaded be chosen from the system photo picker. 

Finally, I just need to enter a commit comment and push to Github where their servers will process the text file using Jekyll and publish. 

[![](/images/BlogpostingtoGithubhostedJerkyblogoniOS5.png)](/images/BlogpostingtoGithubhostedJerkyblogoniOS5.png)

[^20170603200740]: YAML front matter