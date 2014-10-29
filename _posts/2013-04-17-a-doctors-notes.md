---
layout: post
title: A doctor's notes
date: 2013-04-17 8:28  
tags: EMR, medicine
---

Physicians spend a large part of their day documenting what they do, primarily in the form of the clinic note, but also telephone notes, record reviews, and the legions of forms the government and insurance companies create.

Over my time as a fellow and a private practice physician, I've created what I consider a relatively elegant and easy system for moderately skilled tech-nerd physicians to create, store, retrieve and disseminate their documentation and I'd like to share a small part of it with you.

I didn't mean this post to become as long as it had. I tried to keep it short by leaving out most of the specifics, potential pitfalls, and alternatives. I failed. So I've created a "too long: didn't/don't read" (TL;DR) version that is both interspersed throughout the text below or [available as a separate post](http://soitscometothis.net/post/a-doctors-notes-abbreviated).

# Introduction #

Data is important. 

Data fails when it is inaccurate or inaccessible.

Paper charts and modern EMRs excel at failing in both of these areas. 

Physicians need a better way to manage their clinical notes than is afforded by the software tools they are issued and most clinics and hospitals. 

# Inaccurate #

> TL: DR: Boilerplate templates and copy-and-paste (CAP) have resulted in voluminous, inaccurate notes. Poorly designed software that inhibits data entry encourages the use of these templates and copy-and-pasted inaccuracies. This also inhibits entering all the pertinent data so that data is lost due to lack of documentation.

The perils of modern EMR documentation are [well described in the literature](http://www.reuters.com/article/2013/01/04/us-electronic-medical-records-idUSBRE9030IJ20130104). Most of the inaccuracies are created because of a combination of pressure to document unnecessary data in conjunction with the power to easily create this unnecessary documentation by templates or copy-and-paste. 

Daily, I see patients in consultation for very specific joint symptoms in which the prior notes have a well documented, template-created, ENT exam but no joint exam.[^1366312334-fn1]

I saw one patient whose initial visit to his PCP was for a sore throat and the exam dutifully noted pharyngeal erythema and tonsilar exudate, as did every subsequent exam for the next 2 years. Either it was the longest lasting case of strep throat in the history of medicine or the data was inaccurate. 

All physicians know that a detailed, page long list of negative symptoms is most likely to mean the ROS was never done rather than that it was done completely. 

And yet, sadly, this data stands as canon in the indelible, idealized EMR.

When you can't even look at your own notes from a year ago and trust in their accuracy, you're lost. 

Another part of the reason that the data is inaccurate is because of numerous barriers to data entry. In a finite amount of time, I will have to document less if I use a feather quill than if I use a ballpoint pen. The same is true with computers. If the software is poorly designed requiring multiple screens, menus, pop ups, check boxes, and radial dialogue boxes, then the data will be incomplete or less accurate because it could not be entered frictionlessly.

It seems clear to me that no one who has ever created the UI of an EMR has actually had to use it to document multiple encounters in a busy clinical practice. This may explain why those physicians who frequently praise their EMR are either academics whose residents are writing their notes, or have paid underlings entering most of the data.[^1366312334-fn2]

# Inaccessibility #

> TL:DR: Modern EMRs, paper charts, changing jobs, network outages, server crashes, and outdated/unsupported data formats all conspire to keep you from accessing the data you created and need to take care of your patients.

Physicians spend a large amount of their time documenting the clinical history and exam; the interpretation of the combined history, exam, labs, imaging, and pathology; and treatments (and most importantly) the response to treatments over time. This historical knowledge is priceless and yet too often is neglected.

As physicians spend so much time creating this record and since it is so important to providing the best possible care, you would think we would guard this record religiously and yet I would assume that most physicians have no ownership over their work product. It is a common theme in the internet nerd community that one should own their data so that if you decide to stop using a company or the company shuts down, you have not lost your data. How much more important are our clinic notes than some Instagram photos or blog posts about your latests cooking experiment? 

Notes can be inaccessible to the physician who created them for many reasons but primarily due to no longer working at the facility where they created the not or just not having remote[^1366312334-fn3] access.

Notes are written in one practice but when the physician leaves he doesn't take the notes with him. In the days of paper charts, this might have been an unfortunate necessity but in the digital age the entire record could fit on a thumb drive.

Notes are written in the hospital on rounds. The notes stay in the hospital chart, completely inaccessible to the individual physicians's clinic EMR. 

Not long ago a colleague left the state. I inherited many of his patients. I was completely unable to get records. He no longer had them as having left them with the clinic when he moved. The hospital owned clinic was shut down. The hospital medical records department had no idea where they might be and seemed insulted that I would even ask them the question as their mandate ended at the hospital doors. All that knowledge and work was lost.

Next, records can be inaccessible because they are locally stored but you are remote, or because they are remotely stored, "in the cloud" in today's parlance, but the internet/server/power is down. Local data is fast, while remote data is slow. Remote data can be ubiquitous, while local data isn't.

Finally, data can become inaccessible due to proprietary data formats. Again, it is well documented that many EMRs create lock-in with their proprietary data format. Even if you can someone get that data out, it is unlikely that the data will survive future advances in technology. Simply put, I cannot read documents I created with word processors from the early 1990s, where as I can still read hand written notes from the same time. Data needs to be in some kind of common, non-proprietary, future-proof format.

# Solution preamble #

This is not a best practices solution.

This is not an ideal solution.

This is a practical, this-is-the-world-I'm-living-in solution. 

It is based on principles that are unchanging but is created with tools that are constantly changing and therefore it adopts to the tools.

It is not a complete EMR. It is a note taking system that I use that is powerful, practical, and functional within the confines of the modern medical system. I certainly wish there was a feature complete, powerful, EMR that allowed me to own my data and accurately input my notes with the benefits of remote and local storage combined. There is not.

It is not likely to be useful as-is for most physicians, but those with a modicum of technical knowledge should be able to easily adapt it or it's principles to their own system.

# Principles #

1. Data must be easily entered at the point of care.
2. Data must remain in the possession of the physician.
3. Data must be protected from becoming unreadable due to expired proprietary formatting.
4. Data must be encrypted.
5. Data must be rapidly accessible both locally and remotely.
6. Data must be easily searchable from outside the files proper.
7. Data must be easily displayed in a aesthetically pleasing format that can be changed in time.[^1366312334-fn4]

# Solution - Hardware #

> TL:DR: Buy an 11 inch Macbook Air and turn on File Vault in the system preferences. 

Although the software is probably the most important part of my system, everything starts with the hardware. Hospitals and large medical clinics typically buy cheap Dell computers running Windows. This inevitably leads to slow, uncustomizable, one-size-fits-no-one machines running outdated software, bogged down by bloatware and viruses.

My weapon of choice is a Macbook Air. Apple computers are considered more expensive, but comparing equivalent models, are equal or cheaper than a similarly powered machine from another company. SSD drives are ridiculously faster than the traditional HDD. The Macbook Air[^1366312334-fn6] is light enough to be easily carried around a clinic or hospital and small enough to type with on your lap or throw on any counter, exam table, or chair. The size also means that I can easily take it with me anywhere resulting in physical security of my files, part of the HIPAA requirement. While $1000 may be expensive compared to cheap Windows laptops, it's cheaper than any board test I ever took and for something I use 8-12 hours a day, seems like a bargain to me.

The operating system for a new Macbook Air is OS X 10.8 or "Mountain Lion". This operating system has built-in full disk encryption. While benchmark tests will show that this slows down the speed of the machine (as the CPU has to decrypt and re-encrypt your data on the fly as you open and change files) in clinical practice you will never notice. Having all my files encrypted provides security to my patient's data and has frequently shut down any complaints from CMIOs that I'm using my personal hardware in the clinic. This disk encryption is part of keeping your patient records safe and HIPAA compliant and most clinics and hospitals have yet to comply with this kind of security. When my last clinic decided to implement disk encryption on numerous Windows machines from Dell and HP running various OS's and with standard HDDs it was a nightmare. Nurses were locked out of computers for days and a drastic decrease in speed was noted immediately. In OS X you just need to flip a switch.[^1366312334-fn7]

If you want, you can get an external monitor, keyboard, and mouse to use when not mobile. My colleague does this. My wife and I do not.

# Solution - Software #

> TL:DR: Write your notes into a plain text editor, using a text macro application, and save them as plain text files into one folder.

Now that I have the hardware, the next question is what to use to create the note. 

Short answer: Anything but the EMR.

Longer answer: EMRs seem almost deliberately designed to be impossible to create notes with easily. They also typically store the data in proprietary formats and the data is usually locked into the EMR. So don't use it. Yes, in a sense this creates more work, but I argue you'll save time in other ways and with the benefit of owning your data.

I advocate you write your notes in plain text. Plain text is praised by programmers and nerds of every walk of life from [lawyers](http://www.macworld.com/article/1161549/forget_fancy_formatting_why_plain_text_is_best.html) to physicians because it is "open", non-proprietary, future-proof, easily encryptable, easily compressible, and results in small file sizes.

Plain text can be written in any text editor. You can even write in word processors like Word or Pages, but I strongly recommend against it. All computers come with a text editor like TextEdit on the Mac and there are many different free and cheap text editors available. Byword, IA Writer, Multimarkdown Composer[^1366312334-fn8], TextWrangler, and Textmate are just a few that I own and use based on my whim and mood. The great thing about plain text is that it does not have any formatting that locks it into one application.[^1366312334-fn9] So if you create a months worth of notes in Byword and then decide to start using IA Writer because of its cute blue cursor, you don't have to change anything about your data.

Your text editor will present you with one big text field that you can type or dictate into. No modal boxes. No pull down menus. No changing from screen to screen just to document different parts of the HPI.

I save each clinic, phone, and hospital note as a separate text document in one large folder called "patient notes"[^1366312334-1366312334-fn10].

Of course, a large empty sheet can be intimidating and also somewhat slow. You don't want to have to type out your headers and other boilerplate every time. For example, you don't want to type out the name and date yourself each time you create a note, do you? So you need a text macro program. I've written about these before and there are plenty of others who have as well. Anything you are going to type over and over should be automated[^1366312334-1366312334-fn11]. 

I use [TextExpander](http://smilesoftware.com/TextExpander/index.html) and you can read my [many posts](http://soitscometothis.net/tag/textexpander) on it or search the web for other's articles. Basically, get a text macro program and learn how to use it. Don't create all your macros at once. Build them up slowly and organically over time as you need them. It will take awhile, but your speed and accuracy in documentation will be impressive. In time, you will go from macros that turn `.hum` into `adalimumab (Humira)` to macros that turn `.mtx1` into `Rx: start methotrexate 2.5mg, take 15mg (6 pills) every 7 days, #30, refill 1` and eventually into macros that turn `.ddxcie` into

    Differential diagnosis of chronic inflammatory effusion/monoarthritis
    
    1. Mycobacterial infection  
    2. Fungal infection
    3. Lyme arthritis  
    4. Monoarticular presentation of rheumatoid arthritis  
    5. Seronegative spondyloarthropathies  
    6. Sarcoid arthritis   
    7. Foreign-body synovitis  
    
    Consider ordering: CCP, RF, TB (quantiferon), ACE level, fungal cultures and smear, mycobacterial cultures and smear, Lyme serum, Lyme PCR joint, MRI, HLA-B27, ophthalmology consult, and/or CXR if not already complete.

Some EMRs[^1366312334-1366312334-fn12] have macro functionality built in but that is limited to the program and the confines/rules of the program. By using a separate application that functions on top of the underlying applications you can use the same macros anywhere. So, if I get an curbside consult email from a family physician asking about what they should be considering in a patient with a chronic inflammatory effusion of the right knee, I can actually type 7 characters and hit send.[^1366312334-1366312334-fn13]

I have a friend who has created amazing macros for things like the NIH stroke scale and a complete neurological physical exam that not only allows him to quickly document those items, but also serves as a kind of checklist to remind him not to skip anything. 

I use it for everything from commonly misspelled works, to entire paragraphs of patient education, to plans of care, to templated procedure notes, to macros that calculate and type the patient's age when I type the patients date of birth into the note.

Other Examples: 

- `.dxra` = Rheumatoid arthritis (714.0)  
- `HepB/C` = hepatitis B surface antigen, hepatitis C antibody 
- `.posana` = A positive ANA does not diagnose an autoimmune disease nor does a negative result exclude it; however, ANA is positive in 99% of patients with Systemic Lupus Erythematosus therefore a negative result strongly argues against such a diagnosis.  ANA can be positive by definition in 5% of the healthy population, typically in titers less than 1:320.  Up to 20% of healthy relatives of patients with rheumatic disease and up to 75% of healthy individuals older than 70 will have a positive ANA (typically less than 1:80 with a speckled or homogenous pattern).  Other conditions associated with a positive ANA are thyroid disease, chronic infections including TB/viral hepatitis, subacute bacterial endocarditis, malignancies, any of the auto-immune or connective tissue disease, multiple sclerosis and patients with silicone breast implants.  In the absence of physical or biochemical evidence of pathology, a positive ANA is not clinically useful. 

One type of macro I use constantly is one that changes any medicine abbreviations like LEF into the full generic _and_ brand name: leflunomide (Arava). This creates an extra level of education and safety for other physicians who may not be as familiar with our specialities medicines and also for the patient, who may know their drug by it's generic name "Avara" while I type LEF or leflunomide. I frequently give my patient's their notes or at least the assessment and plan at the end of each visit so having this clarity built in without any extra work on my part is important.

# The Painful Part - Putting _Your_ note in _Their_ chart #

>TL:DR: Your note saved in your records needs to be placed in the clinic or hospital records that the patient is at. If they have an EMR, just copy and paste the note into their application. If it is a paper chart, print it out.

So, you have _your_ note. Now what? This depends on the medical record system for your hospital or clinic, but with one commonality: it will be ugly, slow, inelegant, and painful. You have to put your note into the medical records of the clinic or hospital in which you're seeing the patient. EMRs are not open and do not use common data formats even between the same EMR at different hospitals. Paper charts are still used widely in most hospitals in the country. There's just no getting around this no matter what you do. If you want to keep your data and want to benefit from the legibility and speed of typed text on your own machine, you just have to put up with it.

At my last job the clinic had an EMR and the hospital used paper charts. It is likely that you have a similar situation. 

## EMR Charts ##

In my EMR and in whatever EMR you are likely to be using, you will need to copy and paste the text into the EMR. In EMR's that have a large open text field like CPRS this is relatively easy. In complicated EMRs like NextGen, you'll have to find a free text dialogue box and paste it in there before "generating" the note. There may be issues with poor line formatting but there are ways around this.[^1366312334-1366312334-fn14] 

Frankly, I have to force myself not to care about the formatting of my notes in the EMR because those who make them and those who buy them just don't care and I would waste hours of my time trying to make them look good. I just copy-and-paste, close my eyes, and hit submit. I have to console myself that the note in my system and the note I send out to the physicians consulting me looks like I actually care.[^1366312334-1366312334-fn15]

## Paper Charts ##

When at a clinic or hospital with a paper chart, I carry a small, retractable universal printer cord with me that I can plug it into the back of the networked printers at the nursing stations and just printing my note to place in the chart.

# Solution - Backup and Security #

These are your notes. These are your patient's notes. They are gold and they are poison. You absolutely cannot afford to lose them to theft or to data lose both because of the loss of such valuable information and also due to potentially severe financial penalties from violating patient privacy laws. Your back ups and your security must be strong and usable (read: easy).

## Security ##

First, you must maintain physical security. This means the computer you use and any back ups you have must be physically protected. You don't leave your computer unattended in your office. You don't leave your back ups in your unlocked office on your desk. 

My computer is on me 90% of the time during normal life, and when it is not, it is locked up. My backups are also either on my person or locked away in a hidden location. Use both physical security and security by obscurity. 

Second, you must have a strong password to lock your machine. It should be easy to remember and easy to type but it also needs to be long [^1366312334-1366312334-fn16] and not simple words. iloveyou, password, 1234567, qwerty, asdfjkl; and temporary are not secure passwords. Use 3-4 words you can easily remember but aren't easily associated with you (kids and pets names are bad), substitute a few characters here and there, and that should be good enough in most cases. A good one might be something like `Caesar?:ettu,Brute`[^1366312334-1366312334-fn17]. 

Third, your data should be encrypted. This can be really complicated and painful to do. But you bought a Macbook Air and turned on File Vault, right? Ok, moving on.

Finally, your remote data must also be transmitted and physically stored securely. If you're using a public company then I would say to be safe you need to have a HIPAA (I think the fancy acronym for this is BAA.) agreement in place with them and they need to promise that they are following HIPAA compliant practices. Most services such as Dropbox, do not. ;-( 

Thankfully, there is a new product (and more on the way) that provides remote, encrypted data in a Dropbox-style fashion for a reasonable price: [Transporter](http://filetransporter.com). You can plug their device into your own networks (that should be physically and electronically secured) and it creates a Dropbox-style folder on your machine giving you the power of Dropbox (both remote and local data synchronization) without the messy business agreements and monthly cost. *I have not implemented this into my workflow yet*, but will in the next two months. I plan on having one at my clinic and one at home providing cloud storage and back up while maintaining a local copy as well. 

## Backup ##

There are many articles out there on the importance of backing up your data. Google them. Read them. Do them.

I make multiple [clone back ups]({% post_url 2013-03-15-The-safety-of-clone-backups %}) of my computer which includes my patient notes. I keep one copy on me and I keep two other copies locked in fire proof safes. It's really not that hard and it is your responsibility. 

You can also set up a remote backup/storage using something like the [Transporter](http://filetransporter.com) mentioned above.

Finally, text files are so small, you can even easily keep a copy of them on an encrypted USB drive you wear around your neck on a chain.[^1366312334-1366312334-fn18] Now that's dedication.

Backup up my data is just a part of my day. I'd sooner leave my door unlocked then not backing up my files.

So that covers principles 1-5 that I [enumerated above][Principles], leaving only search and formatting. 

# Solution - Search #

> Use Spotlight or the powerful search functions in applications like TextWrangler to search quickly and easily in all your notes at once.

Google redefined the power of search in our minds, first with ability to easily search the entire internet and then the ability to search your mail, your desktop, and all your files. Rather than having to store files/emails in complicated, sub-nested folders, you just type a few words that you expect to find in the file/email and instantly see all the matching results.

Mac's[^1366312334-1366312334-fn20] have full, in-file text search built into the operating system. It's called Spotlight and you can bring it up easily by hitting ⌘-spacebar or clicking on the magnifying class icon in the upper right of your screen. This is the fastest way to search your files. If you need a bit more power and fine-tuning use Spotlight the Finder (option-command-spacebar).

Just today a colleague asked me how many patients with psoriatic arthritis I have that are on azathioprine (Imuran). I didn't think I had any, but I checked and by typing the following characters and nothing else, I brought up the 4 notes on one patient in which I did: `⌘-spacebar .psa .aza`.

Although I'm told that this is possible in some EMRs such as ***, it was not possible on the EMRs I've used in the past including NextGen, Epic, CPRS, and IPR.

Another example of this power is when another specialist approached me recently to ask about a patient he sent me. He couldn't remember their name and actually thought I probably hadn't seen the patient yet. By searching for consults ordered by this physician, I was able to pull up the consult note before he'd even finished speaking, and tell him my findings.

And I use this search functionally all the time. Whenever my nurse mentions a patient to me, my reflexes kick in and I quickly have their last clinic note open, and a new note created and ready for me to document whatever we're about to talk about. 

It is about uniquitous access to information and easy, rapid creating of new data. I've never read GTD, but I wouldn't be afraid to show my system to David Allen.

# Formatting #

> TL:DR: Adding formatting takes some more work and nerdery that you may want. If so, just write in plain text&mdash;it's fine. If you do want to be fancy then learn [Markdown]() and [CSS]().

By it's very nature and what makes it useful for this kind of system, plain text does not have any formatting but there there are times when you may want some formatting. This is why many people when they write papers will use something like Word so they can add strange fonts, weird colors, or pictures. I was tempted to the dark side at one point because I wanted to have my letterhead in the header of the document. This is easiest with a word processor program but can still be accomplished with some nerdery.

I write my notes in a style called Markdown. Markdown allows you to write in plain text but add some extra characters that allow the plain text to be converted to a formatted style like HTML, while still maintaining readability in the plain text.

Confused? Me too at first, so here's an example.

If I want to **bold** something, I just put two asterisks on either side of the words  \*\*like this\*\*. When you read it in plain text it "looks" bold or emphasized, right? Markdown also includes formatting for _\_italics\__, headers, numbered lists, bullet lists, and links.

I then use an application called [Marked](http://markedapp.com/) which will take my text notes and display/save/print them with the Markdown formatting as well as with any other formatting I've created as a template using [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets). When I'm going to print a copy of my note for the patient or the referring physician, or when I'm going to archive it as a PDF[^1366312334-1366312334-fn21] I run it through Marked to get the final document. 

This allows me to take a note that looks like what is on the left and print a note that looks like what you see on the right.

[![](/images/noteandMarkedpreview.png)](/images/noteandMarkedpreview.png) 

When I change clinics (new letterhead) or change moods (different font) or get older (bigger font), I can just change one CSS file rather than having to change every old note.

[![](/images/CSSnoteexamples.png)](/images/CSSnoteexamples.png) 

This last step is a bit more complicated and requires more educational investment that most will want to do. It's ok. You can still make great looking notes just using plain text formatting either with or without Markdown. Other possibilities are to use ALL CAPS for your headers, or to just print your notes out on a printer that is loaded with your office's letterhead. 

# Conclusion #

What I have is an accurate, fast, reliable, secure, and searchable record system for every patient I've ever seen. The cost of the hardware is significant, but relatively not that expensive[^1366312334-1366312334-fn22] and something I would buy anyway even if I wasn't a physician. The cost of the software can range from free to less than 100 USD. The skills necessary to use this system seem minimal to me, but being a tech nerd, I recognized that my opinion may be heavily biased. You will likely need to be able to type fast or have good dictation software. You will need to be comfortable around computers, which for our eminent members is likely not a given, but will certainly be standard for our new initiates. The more "advanced" features like Markdown and CSS, really aren't that difficult compared to memorizing the [Kreb cycle](http://en.wikipedia.org/wiki/Citric_acid_cycle) or knowing when to appropriately order an [ANA](http://www.choosingwisely.org/doctor-patient-lists/american-college-of-rheumatology/).

# Future #

I didn't create this system because I think I'm the smartest guy out there. I created it because I needed something that worked and everything I've used since I started my medical education[^1366312334-1366312334-fn23] has been truly atrocious to the point that even [John Gruber took notice](http://vimeo.com/31926572).

I truly hope that someday a system is created that works wonderfully and follows the principles I've listed above. At a minimum, I hope that a system is created that is so wonderful and powerful that I am willing to compromise on those principles in order to use it as it will mean a vast improvement in the care of patients and in the work burden of all physicians.

[^1366312334-fn1]: FYI: Peripheral edema is not a part of a joint or MSK exam.

[^1366312334-fn2]: I'm looking at you, [Rob](http://more-distractible.org/2013/02/24/death-of-an-evangelist/).

[^1366312334-fn3]: internet or "cloud"

[^1366312334-fn4]: The data must be separate from the formatting.

[^1366312334-fn6]: While I used the 13 inch, I now recommend the 11 inch which I bought for my wife and convinced another colleague to get.

[^1366312334-fn7]: I would argue that it should ship turned on by default.

[^1366312334-fn8]: Programmed by an internist

[^1366312334-fn9]: In fact, I argue that medical records of the future should have a standard file format readable by any EMR so that every physician in a clinic or hospital could use a different EMR to access the same record.

[^1366312334-1366312334-fn10]: I'm really creative. /sarcasm

[^1366312334-1366312334-fn11]: This does not mean your entire note!

[^1366312334-1366312334-fn12]: Epic.

[^1366312334-1366312334-fn13]: And with TextExpander Touch, I can even do that on my iPhone.

[^1366312334-1366312334-fn14]: Different operating systems use different invisible characters to represent a line break. Typically Mac, Windows, and Unix all use a different set of characters so if the system you're copying from is different than the system you're pasting into, as is the case with many EMRs that are running remotely through a VPN, you will get weird line breaks, or no line breaks at all. This can be easily fixed by either changing the character for the line break when pasting using an application like Keyboard Maestro (this is what my neurology friend does), or some Text Editors like IA Writer let you choose your line break character when saving the file as in the image below.  
[![](/images/linebreaksIAwriter.png)](/images/linebreaksIAwriter.png) 

[^1366312334-1366312334-fn15]: This is another benefit of writing your own notes in plain text and doing your own formatting: you can make sure the consult letter you send out looks professional. While it probably shouldn't matter, when I am sent an ugly, poorly formatted, EMR note, I think the sender is less intelligent than is perhaps fair.

[^1366312334-1366312334-fn16]: at least 8 characters

[^1366312334-1366312334-fn17]: Ceasar asked: et tu, Bruté?

[^1366312334-1366312334-fn18]: Would an implantable, subcutaneous chip be going too far?

[^1366312334-1366312334-fn20]: And maybe Windows too? I have no idea as I stopped using Windows machines with XP.

[^1366312334-1366312334-fn21]: I save the PDF and plain text notes together.

[^1366312334-1366312334-fn22]: One hospital I was at spent $70,000,000 just for the EMR software.

[^1366312334-1366312334-fn23]: And even before, as I was installing shareware EMRs on my laptop when I was in college.