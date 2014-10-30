---
layout: post
title: NIH Stroke Scale with Keyboard Maestro and TextExpander  
date: 2013-01-30 20:10  
tags: 
- Keyboard Maestro
- TextExpander
- medicine
- programming
- technology   
---

A colleague of mine wanted a way to easily document the NIH stroke scale score with the added benefits of not having to type the whole thing each time, prompts to remember what to evaluate and what the scores mean, and also have the final score calculated for him. Requirements included that the input had to be in TextExpander due to a preference for that applications input style, and the output would have to be in the middle of a Pages document that was using a single font and no bold or italics.

He had already created the TextExpander snippet and basically needed me to figure out a way to use KM to calculate the score and put it into the note. Oh, one more thing: He wanted to do this with only one command. 

## Challenge accepted!

The KM macro first types out the shortcut for the TE macro, which calls the TE snippet pop up window, and then pauses until the TE snippet window disappears. 

The TE window has all the steps of the NIH Stroke Scale including prompts to remind the user how to do it correctly.

[![NIH Stroke Scale TE Menu](/images/NIH_stroke_TE_menu.png)](/images/NIH_stroke_TE_menu.png) 

Once the TE part is complete, the KM macro continues. All it really does it use regular expressions to find the individual numbers in the scale and add them together for the final score. Since the final score is really just simple addition of 15 single digit numbers, the whole exercise is a bit of a Rube Goldberg, but it was fun anyway and any less brain power and time needed at 2 in the morning during a stroke is probably a good thing.

And the final result:

<video width="640" height="480" controls="controls">
  <source src="/images/NIH_stroke_scale.m4v" type="video/mp4" />
  Your browser does not support the video tag.
</video>

[![](/images/NIH_stroke_scale.jpg)](/images/NIH_stroke_scale.jpg) 

The resulting KM macro file [is here](/images/Calc_NIH_stroke_score_from_TE_macro_combo.kmmacros).

The original TE snippet:

    NIH STROKE SCALE %1m/%e/%Y %H:%M
    1a. Level of Consciousness:	%fillpopup:name=1a.:default=0 (Keenly responsive.):1 (Arousable with minor stimulation):2 (Requires strong stimulation):3 (Comatose)%
    1b. LOC Questions (month/age):	%fillpopup:name=1b:default=0  (Answers both questions correctly):1  (Answers one question correctly):2  (Answers neither question correctly)%
    1c. LOC Commands (eyes/grip):	%fillpopup:name=1c:default=0  (Performs both tasks correctly):1  (Performs one task correctly):2  (Performs neither task correctly)%
    2.   Best Gaze:			%fillpopup:name=2:default=0  (Normal):1  (Partial gaze palsy):2  (Forced deviation)%
    3.   Visual:			%fillpopup:name=3:default=0  (No visual loss.):1  (Partial hemianopia):2  (Complete hemianopia):3  (Bilateral hemianopia)%
    4.   Facial Palsy:			%fillpopup:name=4:default=0 (Normal):1 (Minor paralysis):2 (Partial/Central paralysis):3 (Complete paralysis)%
    5a. Motor Left Arm:		%fillpopup:name=5a:default=0 (No drift for 10 seconds):1 (Drift without touching):2 (Some effort against gravity):3 (No effort against gravity):4 (No movement):0 (Amputation or fusion)%
    5b. Motor Right Arm:		%fillpopup:name=5b:default=0 (No drift for 10 seconds):1 (Drift without touching):2 (Some effort against gravity):3 (No effort against gravity):4 (No movement):0 (Amputation or fusion)%
    6a. Motor Left Leg:		%fillpopup:name=6a:default=0 (No drift for 10 seconds):1 (Drift without touching):2 (Some effort against gravity):3 (No effort against gravity):4 (No movement):0 (Amputation or fusion)%
    6b. Motor Right Leg:		%fillpopup:name=6b:default=0 (No drift for 10 seconds):1 (Drift without touching):2 (Some effort against gravity):3 (No effort against gravity):4 (No movement):0 (Amputation or fusion)%
    7.   Limb Ataxia:			%fillpopup:name=7:default=0 (Absent):1 (Present in one limb):2 (Present in two limbs):0 (Amputation or fusion)%
    8.   Sensory:			%fillpopup:name=8:default=0 (Normal):1 (Mild to moderate loss):2 (Severe loss)%
    9.   Best Language:		%fillpopup:name=9:default=0 (No Aphasia):1 (Mild to moderate):2 (Severe aphasia):3 (Mute or global aphasia)%
    10. Dysarthria:			%fillpopup:name=10:default=0 (Normal):1 (Mild to moderate):2 (Severe dysarthria):0 (Intubated or other)%
    11. Extinction and Inattention:	%fillpopup:name=11:default=0 (Normal):1 (To one modality):2 (Profound loss)%
    TOTAL:				