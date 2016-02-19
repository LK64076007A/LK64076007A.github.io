---
layout: post
title: 'Driftwood: quickly start podcasting from your iPhone'
date: 2016-02-06 12:15:14 -0500
tags: 
- Driftwood
- technology
- iOS
- Github
---
 [Driftwood](https://github.com/LK64076007A/driftwood) is a tool I created to rapidly deploy the necessary tools for publishing a podcast: a website, a podcast formatted RSS feed, and hosting for the files. A secondary goal was to be able to do all this from an iPhone. I was inspired in part by Manton's [microcast](http://www.manton.org/2016/01/new-podcast-timetable.html) [Timetable](http://timetable.manton.org), and from my own use of Jekyll and Github pages to host [my blog](http://soitscometothis.net). My final goal was to be able to "self"-host podcasts that I'm currently paying $100+ a year to a commercial company, especially on one that is mostly retired but not dead. 

# Examples

- The demo page can be seen [here](http://soitscometothis.net/driftwood).

- My own page using this template is [here](http://soitscometothis.net/microcast).

- The Github repository is [here](https://github.com/LK64076007A/driftwood).

# Design

The concept and execution is simple: Github is used to both host the source files, build the website and RSS feed from those source files using Jekyll, and host the audio files.

The template design for the webpage is clean and elegant, thanks to [Kiko](http://github.com/gfjaru/Kiko) by [@gfjaru](https://twitter.com/gfjaru). I made a few tweaks but nothing significant. Since podasts are all about the audio and not the webpage[^160206103026], I think a simple page is best, and the user can add additional features as needed. 

Getting started is simple:

1. Clone or fork [Driftwood](https://github.com/LK64076007A/driftwood) to your own repository.
1. Rename it.
1. Edit `_config.yml` with your information.
1. Edit  `about.md` with your information.[^160206105149]
1. Replace `images/itunes.png` with your own logo (1400x1400)
1. Replace `audio/ep1.m4a` with your own file
1. Edit the file in `_posts` with your information, date, shownotes, etc.

And your first episode is up!

Add future episodes by adding a new audio file to `/audio/` and a new markdown file to `/_posts/` making sure to follow the template of the original file.

If you need further information on formatting post pages for [Jekyll](http://jekyllrb.com/), you'll find a lot of information at the [Jekyll website](http://jekyllrb.com/) or on Google, since the first thing one does after using Jekyll to publish their blog is to write a post on using Jekyll to publish their blog.

# Doing it iPhone only

You can edit the files directly on Github in the browser, but I find it much more pleasent to use one of the awesome iOS apps for Github: [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8&uo=4&at=11l4RT) or [Git2Go](https://itunes.apple.com/us/app/git2go-git-client-you-always/id963577401?mt=8&uo=4&at=11l4RT). 

You'll need one of those apps anyway to upload the audio files and logo because there is [no way to upload a binary directly to Github from the browser](http://stackoverflow.com/questions/29053961/upload-a-binary-file-using-browser-to-github) even on a desktop OS. **Edit:** Ten days after I wrote this Github [announced](https://github.com/blog/2105-upload-files-to-your-repositories) they're adding the ability to upload binaries from the browser..

If you don't have a logo, you can make one very easily using [Pixelmator for iOS](https://itunes.apple.com/us/app/pixelmator/id924695435?mt=8&ign-mpt=uo%3D4&at=11l4RT), which is a steal at $5.[^160206113949]

Record your own episode. You can use the built-in Voice Memos app, which is free with very limited editing functionality, or use [Ferrite](https://itunes.apple.com/us/app/ferrite-recording-studio/id1018780185?mt=8&at=11l4RT), which is more expensive but very powerful with multi-track editing and other professional features. Again, use one of the above apps to upload it. 

# Concerns

1. Is Github the best place to host audio files? 

    Probably not. It's certainly not designed for that and if one makes changes to the files then the version tracking aspect of Git will cause those changes to be saved using up a lot of storage space. File size is limited to 100mb and anything over 50 will likely get a warning. Also, a repository size is soft-limited to 1 gig. In general, these will not likely be an issue, especially for small project podcasts. The purpose of Driftwood is a tool for rapid deployment. If you want to host the files somewhere else, it is a trivial problem. Merely put the full URL for the audio file in the YAML front matter for the episode page and change the podcast.rss file from `<enclosure url="{{ site.url }}{{ site.baseurl }}{{ post.file }}" length="{{ post.length }}" type="audio/x-m4a"/>` to `<enclosure url="{{ post.file }}" length="{{ post.length }}" type="audio/x-m4a"/>`. You can Dropbox, S3, Internet Archive, or any other place where you can directly link to the url of your file. 

1. What about using Github Large File Storage for the audio files?

    I tried that and it didn't work. Either I missed something or you can't really link directly to the file url so it breaks. If you find a way to get it to work, please let me know. 

1. I want to use mp3 files not m4a files.

    No problem. Just change the audio type in `podcast.rss` to mp3. 



[^160206103026]: I don't think I've ever been to the webpage of 95% of the podcasts I listen to. I even considered making this tool "headless"--without a website, just the RSS feed.

[^160206105149]: Please leave the attributions.

[^160206113949]: The "repair" tool alone is worth that in its ability to save any photo.