---
layout: post
title: Forcing Pinch to Zoom
date: 2015-11-04 17:10:43 -0500
tags: 
- html
- javascript
- bookmarklets
- technology
--- 

I am tired of developers who disable pinch to zoom on their websites by either setting the meta tag `user-scalable` to no or `maximum-scale` to 1.0. I run across this the most when following Instagram links from Twitter, but it is rampant, such as when I followed a link and landed on this page today:

<img src="/images/bad_tumblr.png"  width="375" height="667">

Maybe it is just my old eyes, but I couldn't read the text. So I pinched-to-zoom and nothing happened. Because of the poor design decisions of whomever made this page, I was unable to appreciate the content. A view of the source confirmed the problem:[^151104173647]

<img src="/images/bad_tumblr_code.png"  width="375" height="667">

Thankfully, I have a series of javascript bookmarklets that deal with such problems.[^151104172527] The following code over-rides any poor decisions on the part of the developer. 

<code>javascript:document.querySelector('meta%5Bname=viewport%5D').setAttribute('content','width=device-width,initial-scale=1.0,maximum-scale=10.0,user-scalable=1');</code>

[^151104173647]: I highlighted the `user-scalable=no`, but the `maxium-scale=1.0` would do the same thing.

[^151104172527]: Such as disabling copy and paste. 
