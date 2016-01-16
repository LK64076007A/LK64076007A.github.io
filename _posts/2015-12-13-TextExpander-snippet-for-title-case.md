---
layout: post
title: TextExpander Snippet for Title Case
date: 2015-12-13 11:34:25 -0500
tags: 
- TextExpander
- 1Writer
- Javascript 
---

One of the benefits of TextExpander [now][smilesoftware] being able to use Javascript is that you can make much more powerful scripts that run both on the Mac and iOS. One benefit of [1Writer][apple] using Javascript and being popular with the technocrats is you can easily adopt their scripts for TextExpander and use them in other apps.

[Brian Jones][twitter] recently published a [1Writer script for changing selected text to the title case format][github] of [John Gruber][daringfireball]. 

By removing the last three lines

    var selectedText = editor.getSelectedText();
    var formattedText = toTitleCase(selectedText);
    editor.replaceSelection(formattedText);

and replacing them with 

    toTitleCase(TextExpander.pasteboardText);

it can now be used with TextExpander on [iOS][apple 2] or [Mac][smilesoftware 2].

[The code on Github][github2].

[apple]: https://itunes.apple.com/us/app/1writer-note-taking-writing/id680469088?mt=8&at=11l4RT
[apple 2]: https://itunes.apple.com/us/app/textexpander-3-+-custom-keyboard/id917416298?mt=8&at=11l4RT
[daringfireball]: http://daringfireball.net/2008/05/title_case
[github]: https://github.com/jonesbp/1writer-title-case
[smilesoftware]: https://smilesoftware.com/textexpander/entry/textexpander-adds-javascript-support
[smilesoftware 2]: https://smilesoftware.com/textexpander
[twitter]: https://twitter.com/jonesbp
[github2]: https://github.com/LK64076007A/textexpander-title-case