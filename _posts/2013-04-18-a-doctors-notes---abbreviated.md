---
layout: post
title: A doctor's notes - abbreviated
date: 2013-04-18 12:28  
tags: EMR, medicine
---

We doctors spend most of our working life documenting our clinical encounters but too often suffer from poor chart systems leading to inaccurate or inaccessible notes. We also fail to maintain ownership over our work product leading to a loss of useful clinical and practice information and worse patient care.

As an open, universally used EMR data standard does not exist, created my own system that I'd like to share with you. It is based on a set of principles that I've adopted from other modern, technological principles.

# Principles #

1. Data must be easily entered at the point of care.
2. Data must remain in the possession of the physician.
3. Data must be protected from becoming unreadable due to expired proprietary formatting.
4. Data must be encrypted.
5. Data must be rapidly accessible both locally and remotely.
6. Data must be easily searchable from outside the files proper.
7. Data must be easily displayed in a aesthetically pleasing format that can be changed in time.[^1366329887-fn1]

# Hardware #

Buy an 11 inch Macbook Air and turn on [File Vault](http://en.wikipedia.org/wiki/FileVault) (full disk encryption) in the system preferences. 

# Solution - Software #

Write your notes into a plain text editor, using a text macro application, and save them as plain text files into one folder.

# The Painful Part - Putting _Your_ note in _Their_ chart #

Your note saved in your records needs to be placed in the clinic or hospital records that the patient is at. If they have an EMR, just copy and paste the note into their application. If it is a paper chart, print it out.

# Security #

Maintain physical security over your laptop. It must always be in your possession or locked up in a safe or office that no one else (including janitors) have access to. The easiest system it to just keep your computer on you always, or locked in a safe at home.

Make a strong password. At least 8 characters, capital and lowercase letters, numbers, and symptoms. Make it some kind of phrase that it easy to remember and type. E.g. `Caesar?:ettu,Brute`[^1366329887-fn2]

# Backups #

Make [clone back ups](http://soitscometothis.net/post/clone-backups-why-and-how) of your machine. Make multiple copies of your back ups. Encrypt them. Keep them locked up. You can even make a USB necklace with all the notes on them.[^1366329887-fn3]

# Search #

Use [Spotlight](http://support.apple.com/kb/ht2531) or the powerful search feature of [TextWrangler](http://www.barebones.com/products/textwrangler/) to rapidly search through all your notes when you need to find something like "all your patients with psoriatic arthritis on azathioprine" or "all the consults sent to me by Dr. so-and-so".

# Formatting #

Formatting is really not necessary but if you want to print out pretty notes or add letterhead to your faxed PDFs, you can use the [Markdown format](http://bywordapp.com/markdown/guide.html) when writing your notes and the [Marked application](http://markedapp.com/) for creating pretty PDFs with custom CSS formatting.

# Conclusion #

In the end, you have an accurate, fast, reliable, secure, and searchable record system. It's relatively cheap with the only significant cost being the hardware. You can use it across multiple clinics and hospitals using different medical record systems while maintaining a single unified records system on all your patients. 

# Future #

I hope we don't have to wait long until we do have cross platform, open EMR records. Until then, I think this is the best solution for physicians who have a modicum of nerd power.

[Read the full 6000 word original post from which this abbreviated version was created]({% post_url 2013-04-17-a-doctors-notes %}).

[^1366329887-fn1]: The data must be separate from the formatting.

[^1366329887-fn2]: Ceasar asked: et tu, Bruté?

[^1366329887-fn3]: +10 nerd points!