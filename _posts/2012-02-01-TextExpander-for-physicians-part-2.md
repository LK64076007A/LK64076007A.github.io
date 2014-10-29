---
layout: post
date: 2012-02-01 20:37
title: TextExpander for physicians, Part 2
tags: TextExpander, medicine
---

In part 1, I tried to explain what TextExpander was and why a physician might want to use it as a force multiplier by showing a few examples of macros that I use daily.

[TextExpander for physicians, Part 1][1]

In part 2, I will cover special codes, syncing between computers, and iOS apps.
## Special codes

### Time and Date

Special codes are text you can put into a macro that tells TextExpander to do something other than just type out the characters. The simplest example is their Time/Date codes. Inside the macro that creates my consult note template is some characters that automatically inserts that day's date into the note. Instead of having to type, and remember, the date every time I start a new note, the macro does it for me. `ddate = %B %e, %Y = February 1, 2012` There are numerous permutations of this code so you can create the date however you want.

Time codes are also helpful at times. There are many codes to document the time exactly as you might need it but the built in macro that comes pre-created is `time = %1I:%M %p = 9:04 PM`. I have discovered two useful cases for this. The first is documenting how much time I spend on a patient and how much of that time is in counseling and coordination. Keeping track of time is only going to happen if it's easy. This macro makes it very easy. As I walk into a room, I tap the code "ttime". When I finish the history and exam, while the patient is getting their clothes back on and I'm finishing up my note, I hit it again, "ttime". And when I'm done with my counseling I hit it a final time. Now I know how long my visit was and if over 50% of that time was in counseling. This allows me to track my time spent per patient so I can better plan my schedule. If I'm taking 20 minutes per patient, but only scheduling 15 minutes, obviously I need to change my schedule. Also, if over 50% of my time is in counseling, then I can bill by time rather than by the traditional coding levels.

I've also used this lately to keep track of how long it takes to make phone calls to patients. I've been surprised how long the typical call lasts and by having this data, I can more accurately plan my schedule, bill and allocate resources.

TextExpander also comes with some codes for date and time math. Most of my follow ups and planning takes place at regular intervals: every 4 weeks, 6 weeks, 8 weeks and 12 weeks, 12 months or 24 months. This may apply to the next follow up appointment, lab check, infusion time, TB test or DXA scan. While it is easy to say "follow up for labs in 8 weeks", this abstractness appears to be poorly mentally processed. Being more concrete fixes this problem.

	.8wfu = Follow up in 8 weeks (around March 28, 2012). 

More complicated structures wouldn't be that difficult to create.

	.inrchecks = Check INR on 2/4/12, 2/7/12, 2/10/12, and 2/13/12 (Monday).

All the dates and the day of the week in that last macro are automatically calculated.

Are you a hospitalist with a patient needs neurochecks every 4 hours?

	.q4nchecks = Neuro checks q4 hours (01:33, 05:33, 09:33, 13:33, 17:33, 21:33). 

### Fill ins

Another special code is the fill in. `%fill:name%`. This has the macro prompt you to enter text that will be inserted into the text when the macro is created. For example, you might have a macro that prompts for a follow up time.

	.fut = Return to clinic in %fill:numberofweeks% weeks.

This creates the following prompt:

[![fill in prompt](/images/textexpander_fut.png)](/images/textexpander_fut.png) 

Enter the desired time:

[![macro filled in](/images/textexpander_fut_2.png)](/images/textexpander_fut_2.png) 

Hit "enter" and your text appears:

[![Macro completes](/images/textexpander_fut_3.png)](/images/textexpander_fut_3.png)  

I use this all the time for form letters and consult note templates. For each different fill in, you need to change "name" in `%fill:name%` to a unique identifier. Or, if you leave it the same, whatever you put in one place, will appear in all the others with the same phrase. For example, in my consult note, I don't have to retype the patient's name, consulting physician or reason for consult/chief complaint:

[![consult note macro](/images/consultnote_macro.png)](/images/consultnote_macro.png) 

### Copy clipboard

Another special code is the "clipboard", `%clipboard`. This inserts whatever is copied to your clipboard. I use this more for non-medical uses, like writing code or html but the one place I use it regularly in medicine is when saving my notes to file. I use a file name structure that is "Patient Name" and "date of visit." Using the code `%clipboard %1m.%e.%Y` and making sure to copy (Command-C) the name from my note to the clipboard before keying the macro, I save a lot of time saving files.

	.nd = James Bond 2.1.2012.pages

### Cursor placement

The final special code I'll mention is the cursor placement. `%|` (That's percent pipe.) puts your cursor wherever you want with in the text that the macro creates. For short macros, this isn't needed, but when I use my consult note template, I don't need the cursor at the end of the document, requiring me to scroll back up to the first page to start typing. Instead, I place it in the History of present illness, so I can start typing what the patient is telling me immediately:

[![James Bonds note](/images/James_Bond_note.png)](/images/James_Bond_note.png) 

It's a little thing, but you add up all the little things and the time and convenience are incredible.

## Syncing between computers

Once you have created a lot of macros, your library is going to become a valuable commodity. You will become dependent on these macros and feel lost without them. You will want to make sure you back up your library as well as have it available on any computer you may use. Thankfully, the developers of TextExpander have enabled backing up and syncing of your library through [Dropbox][2]. If you don't know what Dropbox is[^1202012211], stop reading immediately and go get it. 

Now that you have Dropbox and have enabled syncing in the preferences of the TextExpander app, your library of macros will auto-magically appear on any computer[^1202012213] that you've also synced using Dropbox. This also works with the iPhone and iPad versions of the applications.

In fact, I have a friend who writes all his clinic notes in TextExpander Touch on his iPad using a bluetooth keyboard.

## iOS apps

TextExpander Touch, the version of the app available for the iPhone, iPod Touch and iPad, is quite good as well, but a bit limited due to restrictions of the operating system. The main restriction is that you cannot use the app to expand text just anywhere in iOS. TextExpander Touch will only work in apps that are specifically enabled to use it. Thankfully, there are a lot of [those apps][5]. The apps also have a built in text editor, so you can write notes there and then copy and paste them or email them elsewhere. It is slightly limiting but nice to have. I tend to use this more for taking notes in meetings and at dinner meetings, when taking out a laptop&#8212;even one as small as a Macbook Air&#8212;would be overly distracting to others.

---

Well, that's enough for tonight. In the next, and hopefully final, part, I will finish up by laying out ideas for macros to use in your practice, keys to creating shortcuts you can remember, non-medical uses of macros and advantages of a stand alone applications versus the built-in functionality that some EMRs have.




[^1202012211]:  Shame on you.

[^1202012213]:  If you are unfortunate enough to have to use a Windows computer at work but are a Mac guy at home, the Windows program [Breevy][3] has bi-directional sync with TextExpander through Dropbox. You may also want to check out [this site][4].

[1]: {% post_url 2012-01-30-TextExpander-for-physicians-part-1 %}
[2]: http://www.dropbox.com
[3]: http://www.16software.com/breevy/
[4]: http://www.monster.com/
[5]: http://www.smilesoftware.com/TextExpander/touch/apps/