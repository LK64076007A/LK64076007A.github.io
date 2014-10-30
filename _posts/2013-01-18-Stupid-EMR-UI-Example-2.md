---
layout: post
title: Stupid EMR UI Example 2
date: 2013-01-18 20:43  
tags:
- medicine
- programming
- EMR
- UI
---

I love tech and I especially love software, but like most things that we deeply love, when they fall short, it's very hard to not get angry.

This is one reason I have such a hatred for the current state of Electronic Medical Records. They're abysmal. [John Gruber even makes fun of them][vimeo]. (Minute 24:28, but the whole talk is worth listening too.)

Today I share [another example][soitscometothis] of poor design.

In the EMR I use now, NextGen, I've been complaining about the joint injection procedure template for 1.5 years. They still haven't fixed it.

I use a standard medication called Synvisc One. Synvisc regular is a 2ml (16mg) injection you give once a week for 3 weeks. Synvisc One is all 6ml (48mg) given at once.

Just to lay out all the numbers for you. This medication is available as:

- 2ml
- 6ml
- 16mg
- 48mg

That's it. Two strengths. Expressed either in a volume or a mass.

You can document this in two places in the procedure template. I want to point out, that this is the first mistake, having two places to document one thing.

And here's how they look:

![](/images/Synvisc_Nextgen_order_1.png) 

First, there's no units. Specifically it just says "units". Is that milliliters? Liters? Milligrams? Grams? Number of injections? Is this for Synvisc or Synvisc One? If I pick one of these, what am I actually documenting or ordering? The closest guess is that this is in milliliters, but then you can't pick "6", the size of Synvisc One. There is a "2", so you could document Synvisc regular. Even then, **1 in 5 available choices will always be wrong**. Why even offer a possible wrong choice?!?! I also point out that this is a pop up menu, so you've already been removed from the screen you're working on.

And here is how the second place to document it looks: 

![][dropbox] 

This one at least has units, but still has all the other problems. 

I would offer the following fixes:

1. Have only one place to order the drug.
1. Instead of a pop up window, make it a radial button choice. 
1. Have two options: Synvisc and Synvisc One

This improve things as follows:

1. Only one place to document. 
1. No choices that are wrong.
1. No extra pop up menu.
1. No need for the user to know the milligrams, milliliters, or any other unit. They just need to be able to read what is on the box.

I hope that before I die[^1301182110], a decent EMR exists. 

We have a long way to go.

[^1301182110]: It wouldn't hurt if it wasn't horribly ugly either.

[dropbox]: /images/Synvisc_Nextgen_order_2.png
[soitscometothis]: http://soitscometothis.net/post/stupid-emr-ui
[vimeo]: http://vimeo.com/31926572