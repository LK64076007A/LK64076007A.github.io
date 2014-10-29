Title: Procedure note with TextExpander
Date: 2012-08-29 21:25  
Tags: textexpander, medicine, technology, programming

I do a lot of joint injections so I created a [TextExpander][smilesoftware] macro to quickly write a short procedure note within my visit note. I used TE 4.0 with the new options for fill ins. I have several optional sections that can expand the note depending on the type of injection I do, but at the same time, for the large majority of injections in which I'm not removing fluid or sending the results for testing[^120822085343], the note is quickly and easily generated without template cruft.

[![](/images/Screen_Shot_2012-08-29_at_9.18.20_PM.png)](/images/Screen_Shot_2012-08-29_at_9.18.20_PM.png)  

1. The pink highlighted text are optional sections that can be added by ticking the preceding checkbox. 
2. The amount of injected medication is pre-populated with my normal dosing but can be edited.
3. The medication is also pre-populated but can be switched to any of the options available in my clinic.
4. The lab section already has the two labs I always order, and I can easily add anything else that I need.
5. There are a few pull-down menus in order to make sure the grammar is correct depending on if I'm injecting one or multiple joints.

Arthrocentesis are simple and straight forward procedures. I'm sure this technique would be even more useful in complicated procedures and operations.

###The raw code
    Procedure note
    Informed consent and time out was completed. The %fill:area% %fillpopup:name=popup 8:was:were% prepped with betadine and alcohol in standard fashion. The skin was anesthetized with ethyl chloride. %fillpart:name=lidocaine%The subcutaneous tissues were anesthetized with less than 3ml of 2% lidocaine. %fillpartend%%fillpart:name=fluidRemoved%%fill:amount% ml of opaque yellow fluid with a positive string sign was removed. %fillpartend%%filltext:name=milligrams:default=40 mg:width=3% of %fillpopup:name=steroids:default=Depo-Medrol (methylprednisolone acetate):Kenalog (triamcinolone acetonide) :Synvisc One% and 2 ml of 2% lidocaine were injected into %fillpopup:name=grammar 10:the:each% joint. Hemostasis was obtained. Post op instructions were given. %fillpart:name=labTests%Fluid was sent for %fill:tests%cell count and crystal analysis.%fillpartend%

[smilesoftware]: http://smilesoftware.com/TextExpander/ "TextExpander"

[^120822085343]: Shame on you if you don't document what labs you order in the procedure note.