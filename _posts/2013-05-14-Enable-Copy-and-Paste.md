---
layout: post
title: Enable Copy and Paste
date: 2013-05-14 22:47  
---

The website Uptodate, a common medical reference site for physicians, appears to disable copying text on the iPhone. This makes it very difficult to copy snippets of text into the notes I'm taking as I read. It also prevents using iOS's text-to-speech functionality when my eyes get tired. 

Thankfully, it's not very difficult to restore this functionality. 

1. On your iPhone, create a bookmark of this page. 
2. Copy the following text to your clipboard:
<pre>
javascript:(function(){

function allowTextSelection(){
  var styles='*,p,div{user-select:text !important;-moz-user-select:text !important;-webkit-user-select:text !important;}';
  jQuery('head').append(jQuery('&lt;style /&gt;').html(styles));
  
  window.console&amp;&amp;console.log('allowTextSelection');
  var allowNormal = function(){
    return true;
  };
  window.console&amp;&amp;console.log('Elements unbound: '+
    jQuery('*[onselectstart], *[ondragstart], *[oncontextmenu], #songLyricsDiv'
    ).unbind('contextmenu').unbind('selectstart').unbind('dragstart'
    ).unbind('mousedown').unbind('mouseup').unbind('click'
    ).attr('onselectstart',allowNormal).attr('oncontextmenu',allowNormal
    ).attr('ondragstart',allowNormal).size());
}

function allowTextSelectionWhenPossible() {
  window.console&amp;&amp;console.log('allowTextSelectionWhenPossible');
  if(window.jQuery){
    window.console&amp;&amp;console.log('jQuery has now loaded');
    allowTextSelection();
  } else {
    window.console&amp;&amp;console.log('jQuery still not loaded.');
    window.setTimeout(allowTextSelectionWhenPossible, 100);
  }
}

if(window.jQuery) {
    window.console&amp;&amp;console.log('jQuery exists; will use');
  allowTextSelection();
}else{
  window.console&amp;&amp;console.log('jQuery not loaded; will include.');
  var s=document.createElement('script');
  s.setAttribute('src','http://code.jquery.com/jquery-1.9.1.min.js');
  document.getElementsByTagName('body')[0].appendChild(s);
  allowTextSelectionWhenPossible();
}


})();  
</pre>
3. Go to the bookmark menu in Safari, find the bookmark you just created, and hit edit. 
4. Replace the URL with the clipboard contents. 
5. Go to Uptodate or any website that blocks copying. 
6. While on that page, hit the bookmark, and functionality should return. 

Credit: I got the JavaScript above from [Alan Hogan](http://alanhogan.com/code/text-selection-bookmarklet).