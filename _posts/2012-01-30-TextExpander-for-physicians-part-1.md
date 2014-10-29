---
layout: post
date: 2012-01-30 18:13
title: TextExpander for physicians, Part 1
tags: TextExpander, medicine
---

As a physician I write a lot.[^1201301814] Most of my writing is the same or similar to things I've written before and will write again. Repeatedly typing the same things character by character is a waste of time, energy and cartilage. In order to turn my 70 word per minute[^1201302145] into hundreds of words per minute without ended up as a patient myself, I engage a force multiplier, TextExpander.

TextExpander is a text macro program. Simply put, you type a few characters and the program outputs quite a bit more characters. In the last 6 months of use, it's saved me from typing over 1/2 a million characters, saving an estimated 24 hours of time based on 70 words per minute or at a more typical physician rate of 40 words per minutes, it's saved me almost 2 solid days of typing.

But like all beautiful things there's so much more than that.

### Personal history

I've been using text macros since junior high school. When writing a history day paper, instead of typing "Commodore Matthew Calbraith Perry", I typed CMCP and the whole name would spring forth. I was able to do with with the built-in functionality of the version of MS Word I was using at the time, but I don't think it was truly a marco function rather than a hack that I created using the automatic spell corrector. 

In college, it became even more handy. Instead of typing out long chemical names like Co<sub>1-x</sub>Ni<sub>x</sub>Cl<sub>2</sub>&middot;2H<sub>2</sub>O or Fe[S<sub>2</sub>CN(C<sub>2</sub>H<sub>5</sub>)<sub>2</sub>]<sub>2</sub>Cl, I'd type CN2H or FSCCl. Not only did that save a lot of characters but it also saved me all the clicks in getting the subscript on the right characters.

In medicine, the problem is even more obvious. The combination of redundancy, complexity and speed make a text macro program a powerful ally.

### Medical application

The first macros I created were for the drugs and diseases I see all the time.

	.ra = rheumatoid arthritis
	.psa = psoriatic arthritis
	.sle = systemic lupus erythematosus 
	.ssc systemic sclerosis
	.oa = osteoarthrosis 

	.pred = prednisone
	.mtx = methotrexate 
	.lef = leflunomide (Arava) 
	.hcq = hydroxychloroquine (Plaquenil)
	.hum = adalimumab (Humira)
	.enb = etanercept (Enbrel)
	.rit = rituximab (Rituxan) 

Notice how for some of the drugs I've included the brand name. This aides in clarity for the patient or non-rheumatologists who may not be as familiar with the generic names of the drugs. e.g. Rheumatologists typically use hydroxychloroquine but most patients know it as Plaquenil. When a patient leaves the office with my note, I don't want them calling later to leave a message that they aren't on that medication with the long name like my note says.

I can also use it to help me remember how to spell the drugs names or even remember some of the generics myself.

	.ken = triamcinolone acetonide (Kenalog)

Even some non-drug words are just impossible to remember to spell correctly.

	.eyemd = ophthalmology

Occasionally, there are some weird labs whose abbreviations are non-standard but whose names are too weird to spell out every time.

	.la = lupus anticoagulant 
	.acl = anticardiolipin antibody
	.b2g = beta 2 glycoprotein antibody

I also don't like typing out my physical exam findings, but this can be important for other doctors and audits.

	.rom = range of motion
	.nrom = normal range of motion
	.prom = passive range of motion
	.arom = active range of motion
	.rhsj = red, hot and/or swollen joints 

Now we start to pick up the pace a bit. I am frequently recommending that patients exercise, but they are far more likely to follow my instructions if I give concrete examples instead of vague platitudes.

	.exercise = Exercise by walking 30 minutes every day after dinner. 
	    			http://youtu.be/aUaInS6HIGo

Coders love when I include the diagnostic codes with my assessment, especially for the weird (redundant?) rheumatology stuff.

	.dxra = Rheumatoid arthritis (714.00)
	.dxia = Inflammatory polyarthropathy, unspecified (714.9)
	.dxhrd = High Risk Drug (v58.69)
	.dxea = Enteropathic arthritis (713.1)

Not infrequently, I want to impart a bit of knowledge to both the patient and the referring doctor. For example, in the case of a patient referred for a positive ANA or positive rheumatoid factor, it's one thing to say they don't have lupus or rheumatoid arthritis but it's even better to explain what that damn tests means.

	.posana

> A positive ANA does not diagnose an autoimmune disease nor does a negative result exclude it; however, ANA is positive in 99% of patients with Systemic Lupus Erythematosus therefore a negative result strongly argues against such a diagnosis.  ANA can be positive by definition in 5% of the healthy population, typically in titers less than 1:320.  Up to 20% of healthy relatives of patients with rheumatic disease and up to 75% of healthy individuals older than 70 will have a positive ANA (typically less than 1:80 with a speckled or homogenous pattern).  Other conditions associated with a positive ANA are thyroid disease, chronic infections including TB/viral hepatitis, subacute bacterial endocarditis, malignancies, any of the auto-immune or connective tissue disease, multiple sclerosis and patients with silicone breast implants.  In the absence of physical or biochemical evidence of pathology, a positive ANA is not clinically useful. 

	.posrf

> Many conditions can lead to a positive Rheumatoid Factor including chronic hepatic and pulmonary diseases, rheumatoid arthritis, Systemic Lupus Erythematosus, systemic sclerosis, mixed connective tissue disease, Sjögren's, polymyositis, sarcoid, malignancies (especially after therapy), AIDS, mononucleosis, parasitic infections, chronic viral infections, tuberculosis, subacute bacterial endocarditis, cryoglobulinemia, etc.  Frequency of positivity of rheumatoid factor in normal individuals also occurs and varies by age from 5% in those younger than 70 to 10-25% in those older than 70.  Changes in RF level do not reflect disease activity; however, a high titer does predict increased severity of disease including extra-articular manifestations. 

I can even use this to remind me of recommendations on certain items. For example, I can never remember the exact recommendations from the BMJ on the duration of steroids for PMR.

	.bmjpmrsteroids

    Daily prednisone 15 mg for 3 weeks
    Then 12.5mg for 3 weeks
    Then 10mg for 4–6 weeks
    Then reduction by 1 mg every 4–8 weeks

Can't remember the criteria for the diagnosis of Takayasu's arteritis?

	.dxcTA

> 1. Age at disease onset ≤40 years (Development of symptoms or findings related to Takayasu arteritis at age ≤ 40 years)    
2. Claudication of extremities (Development and worsening of fatigue and discomfort in muscles of one or more extremity while in use, especially the upper extremities)
3. Decreased brachial artery pulse (Decreased pulsation of one or both brachial arteries)
4. BP difference >10mmHg (Difference of >10mmHg in systolic blood pressure between arms) 
5. Bruit over subclavian arteries or aorta (Bruit audible on auscultation over one or both subclavian arteries or abdominal aorta)
6. Arteriogram abnormality (Arteriographic narrowing or occlusion of the entire aorta, its primary branches, or large arteries in the proximal upper or lower extremities, not due to arteriosclerosis, fibromuscular dysplasia, or similar causes; changes usually focal or segmental)

> 3 of 6 required for diagnosis with a yield to 91% sensitivity and 98% specificity.
    
> Arend WP, Michel BA, Bloch DA, et al. The American College of Rheumatology 1990 criteria for the classification of Takayasu arteritis. Arthritis Rheum 1990;33:1129–1132

You look like a gunner on your note while making sure you remember the diagnostic criteria.

Of course, you can't forget your note templates.

    .arthronote

> Rheumatology Procedure Note

> Procedure: Arthrocentesis
Date of Service: %B %e, %Y<br />
    
> Consent: Verbal consent obtained from patient.<br />
Time Out: Yes.
    
> Procedural Medications:  1% lidocaine, \*** cc; \*** 40mg/1ml, \*** mg; \*** Gebauer's Spray
    
> Description of Procedure: After consent was obtained, the \*** was prepped with betadine and alcohol.  Gebauer's spray and plain 1% lidocaine was used as local anesthetic. The joint was entered and \*** ml's of \*** colored fluid was withdrawn and sent for \***.  Steroid and Lidocaine were then injected and the needle withdrawn.  The procedure was well tolerated and hemostasis was obtained.  The attending physician was present for the entire procedure.
    
> The patient was asked to continue to rest the joint for a few more days before resuming regular activities and warned that it may be more painful for the first 1-2 days.  He/she was instructed to watch for fever, or increased swelling or persistent pain in the joint. Call or return to clinic prn if such symptoms occur or there is failure to improve as anticipated.

See those strange characters after "Date of Service"? This is special code in TextExpander that automatically inserts that day's date when the note is created. TextExpander has a lot more codes like this and others than can really power your macros. More on that in part 2.

---

Hopefully, by now, I've convinced you that you can save a lot of time and stress by turning your frequently used words, phrases and templates into easy to type macros. In future posts, I will delve into some more advanced, yet easy to pick up, topics including:

1. Special codes in TextExpander
2. Syncing your macros across computers
3. Keys to building and remembering your macros
4. TextExpander on your iPhone and iPad.
5. Ideas for macros 
6. Non-medical uses for TextExpander

I will also answer some potential objections to my method, such as why you might want a text macro program if your EMR comes with templates (CPRS) or has a macro functionality (Epic).

If you have any specific questions or concerns you'd like addressed in the future posts, let me know.

**Updated**: [Part 2]({% post_url 2012-02-01-TextExpander-for-physicians-part-2 %})

[^1201301814]: Consult notes, progress notes, telephone notes, lab monitoring notes, drug orders, infusion orders, lab orders, school excuses, work excuses, disability letters, consult letters, etc.

[^1201302145]:  On a good day.