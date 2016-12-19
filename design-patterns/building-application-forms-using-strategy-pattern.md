# Building application forms using strategy pattern

Earlier this year we had a client that used to have a rather cumbersome old system for submitting applications. When they came to us, what they initially **desired** was a way to build their own forms. However, through agile process we determined that what they **needed** was actually just better application forms. While the content and rest of the folks focused on what the form should look like and what it should contain, I spent time deciding on the architecture and structure. 


Now, there were really two main ways of doing it, one perhaps more obvious than the other. At a glance, it sounds like "figure out the form sections, create viewmodels and views for each section and question, build a mapping engine for saving to and loading from database"-job. Okay, fair enough, lets build one form like that. Oh what's this, you need ten more forms? More viewmodels. More views! Wait, do my viewmodels really know every single one of my questions and fields and my entities are really just value objects storing data? What just happened to my domain concerns? Let's rewind back for a minute and do it the right way.

