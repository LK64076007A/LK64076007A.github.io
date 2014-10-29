---
layout: post
title: Podcasting with Squarespace
date: 2012-11-25 23:02  
tags: Squarespace, podcasting
---

# Summary
If you want to create a podcast, Squarespace is recommended as a complete solution for domain registration, hosting, bandwidth, and syndication. They even have a dedicated [instruction manual][squarespace]. **Update: The lack of analytics regarding total number of downloads for each episode of a podcast is a weakness, especially if you want to get sponsors.**

# tl:dr

## Backstory
I recently decided to make a podcast. This was to be a small hobby, a minor side project, and so the technical aspects of the project couldn't take up much of my time and energy. As I was preparing the content and looking at the best ways to turn this into a reality, it appeared that Squarespace could possibly be able to handle all the hosting, bandwidth, and even the domain registration. It turns out that this is correct and for the most part was quite easy.

I've used Squarespace before for several sites. Mostly I've used version 5 and haven't quite gotten into version 6 yet. My past experience has been that they are very helpful with tech support the few times I've needed it, are very generous with long, free trials to test out the service, and are not pushy sales people. In fact, I'm not sure if they have sales people. They don't even ask for your credit card number up front! These are decent folk.

Before I got started, I did have one question related to doing a podcasting site. On their [pricing page][squarespace 2] it stated that the maximum file size is 20mb; however, on [another page specifically about podcasting][squarespace], it stated the maximum size is 120mb. Well, which is it? This is the kind of straight forward question that if I normally ask a support person, they have no idea what I'm talking about, and if they even bother to compare the urls I send them, then never know what I'm talking about. My experience with the Squarespace support was the exact opposite. 

I clicked on the support chat link on their website, was immediately helped by someone pleasant whose name I don't remember and told simply that the normal limit is 20mb, but specifically for podcasting, it increases to 120mb. Perfect. With that verification, I was ready to go.

## Requirements
First, at least mentally, I needed a domain. Squarespace gives you a free domain if you sign up for a year. Check.

Second, I needed a website. Well, that is the basic service of of Squarespace. I picked a template that was close to what I had imagined. It didn't take me long to have a working prototype and over the next several days was able to turn it into something I was happy with. Honestly, I have no design or artistic sense, so it is a real testament to Squarespace's platform that I was able to do this.

Third, I needed an RSS feed for my podcast that I can serve to podcast apps and to iTunes. Simply, Squarespace has already handled that. All you do is create a "blog" page, i.e. a single page that you can add sequential entries to. Then, when you have a podcast episode to publish, you create a blog entry and in that entry add an "audio block" which automagically creates a podcast feed. Squarespace takes care of the syndication and even puts a streaming player into that post. In addition, they have a preference to enable iTunes options so that it can be compatible  with and submitted to iTunes.

Fourth, I needed hosting for the podcast files. You can host them elsewhere such as [libsyn][libsyn] or it may be possible depending on the size of your episodes and the number of downloads to get by with their cheaper plan with 500 GB of bandwidth and 2 GB of storage[^121125232343], but I wanted to splurge so I went for their unlimited place with unlimited bandwidth and storage[^121125235024]. The storage is relatively easy for the most part. You upload your podcast audio file in the previously mentioned "audio block" and save it like you would any normal webpage.  

And just like that, I have a podcast.

## Problems
If I had to do it again, I wouldn't even look for another alternative. It was great. Still, there are some rough edges that could be honed.

First, the file upload process for non-picture/audio/video files is so well hidden, I didn't think it existed. If you want to upload a file like a PDF to your site, it is possible, but I doubt you'd ever find it on your own. When you are editing a page, the normal behavior is to click a plus sign button to add a block (widget). There are blocks for text, picture, audio, video, horizontal rules, and even blank space. There is no block for generic files. I clicked around for quite a while trying to figure it out. The answer is you first choose the text block, click on the "link" button as if you were going to make a text link, and in the next dialogue box is a place to upload a file. This seems to me to be a very unintuitive and misleading place to burry the file upload function. 

Second, but related, there is no place to easily manage all your files. While you can access some of them from that same dialogue box, you cannot access them all. For example, after creating a podcast episode, I wanted to create a direct link in that post to the file for some that were having trouble getting it to play (IE 6, seriously?). There was no way that I could find in the interface to get access to this file in order to link it, or even just get its file name. I had to look at the source code of the rendered webpage to grab it.

These are two small, but significant problems that were so glaringly bad functionally that I have a hard time believing that they came from the same people who made the rest of the site so good.

Third, when selecting text to be edited in the "edit post" window, if the cursor went outside of the box after selecting text, the window exited the editing mode. 

Fourth, when editing text in the "edit post" window, there are certain keystrokes that will cause the window to suddenly and glaringly jump to the bottom right of the screen for a 1/2 second and then return to the center. This happens, for example, when you type some text and hit the backspace key. This must be a frequent sequence of events unless no one else makes typos like I do. Again, this seems like an obvious bug that I'm surprised it hasn't been fixed. 

Again, overall, a great experience, I'd do it again, and I'm looking forward to using their platform for my podcast. Also, I think I'm finally ready to upgrade by Squarespace 5 site to version 6…next weekend.

[libsyn]: http://libsyn.com
[squarespace]: http://help.squarespace.com/customer/portal/articles/637686-podcasting-with-squarespace
[squarespace 2]: http://www.squarespace.com/pricing/

[^121125232343]: Truthfully, this would probably have been more than enough for me too.

[^121125235024]: The smartest answer is probably to go with the cheap plan and upgrade if you need to. You can upgrade at anytime and in the past when upgrading or downgrading, the process has been seamless and prorated without any issue automatically.