---
layout: post
title: "Blog Entry #17 – Week Twenty Two"
comments: false
description: "My experience during the twenty second week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twenty one, software development life cycle, c#, subversion, svn, refactoring, project management, gantt chart, microsoft excel"
---

# Placement Week 22 (8<sup>th</sup> Jan - 12<sup>th</sup> Jan)
## Monday
Kicked things off by implementing a basic factory using "Factory method" pattern, which was quite easy to do with the new-and-improved code structure. The factory implementation should allow for simpler introduction of new elements that factory produces, and improve utilisation of the container which injects objects.

With that out of the way I removed an artefact class and its utilisation within the project to ensure there were no gaps left between old object variant and newly introduced object.

Having important tasks done and out of the way I focussed on continuing to refactor _the class_ which I have been trying to decouple and clean up for couple of days now. That remains to be done as mid-way through the day I remembered I would not be able to attend one of the planned meetings this week and had to notify the client about change in plans.

Once that was taken care of, I received a response from the client asking for a chart showing the progress and how far behind/ahead of the schedule the project is, at this point in time. Unfortunately, me not being a great PM meant that I did not have the chart at hand, nor did I have the data ready to quickly generate the chart. This led to me spending remainder of the day gathering the data and working out how to use excel to generate the chart I needed.

One of the things I noticed whilst gathering data and figuring out the details of the schedules, was that;

- Past me had no clue as to how long certain aspect of the project would take
- What are the components/modules that would go into making the final solution
- Little clue as to how long certain aspects of the project would take
- Order in which components/modules would be/have to be created and finished

Also, I remembered that making linear progress charts of software components is very counter intuitive. This may be in part because software development is a continuous process and rarely has a definitive end point. I mean, well structured, well managed and continuously evaluated PM would probably be able to deal with this through experience and managing the project well, however being both the PM and lead developer of a project is quite a challenge with number of compromises that need to be made.

At this point in time I have focussed primarily on improving my software development related skills and knowhow, and for most part skipped doing anything PM related. Which will have to change soon...

## Tuesday
Intention for the day was to proceed making a Gantt chart and send it off by the end of the day. That was not the case by 5pm.

I collated all the data necessary to have a graph displaying tasks I originally intended to accomplish (prior to starting the development), how the ones I worked on compared to the actual tasks I worked on during duration of the project and to add the cherry on top, the tasks I intend on accomplishing in order to complete the project.

Unfortunately, my MS Excel skills weren't as good as they once used to be and I felt short of displaying all of that data in a presentable chart (couldn't even display half of that data...)

Luckily, during a weekly team meeting "GanttProject" software package got a name drop, and I decided to utilise it on Wednesday.

## Wednesday
Due to my *not-so-great* project management, I dedicated the day to figuring out the broad strokes of tasks I need to complete in order to successfully finish the project.

I managed to get a lot of ideas down and organized them as well as I could. With the data I've accumulated on my rate of progress thus far.

As per last paragraph, one of the things that has become extremely apparent, and something I have observed over many of the project I have been involved in, in addition to most software and non-software projects is that optimistic projections are more often wrong, than not.

This is in-part, due to the fact that I am still learning all the unexpected hurdles that appear during software development, all the *oh-how-could-I-forget-about-this* aspects of projects, and the fact that I am still learning the craft of writing high quality software.

If there's one thing to take away from the analysis of the data on my own progress and timekeeping, is that when putting number down on paper, I should reflect rather than simply estimate (doing research and performing actual analysis helps too, but who has the time for that?).

> "The planning fallacy is only one of the manifestations of a pervasive optimistic bias. Most of us view the world as more benign than it really is, our own attributes as more favourable than they truly are, and the goals we adopt as more achievable than they are likely to be. We also trend to exaggerate our ability to forecast the future, which fosters optimistic overconfidence. In terms of its consequences for decisions, the optimistic bias may well be the most significant of the cognitive biases. Because optimistic bias can be both a blessing and a risk, you should be both happy and wary if you are temperamentally optimistic."
> -**Daniel Kahneman (Thinking, Fast and Slow, Page 255)**

## Thursday
After minor changes I sent off the chart showing current and remaining progress of the project to the client.

One of other things I started sorting out was preparation for front-end development and figuring out general details of hosting etc. In addition to that I organised an upcoming design review to weed out any outstanding issues and ensure the changes I've been working on recently resolve the issues raised in previous project reviews.

What took up bulk of the day was refactoring some of the final parts of the system, which reached to the lowest levels of logic. This is where I found some of the most intricate spaghetti which all came down to one very important misstep in my structure of the software, which all could have been averted very early in the development.

This realization of a logical dependency first came to me whilst reading chapter about boundaries in "Clean Code" by Robert C. Martin. So, once I began working on removing this dependency and improving the overall structure I already had few techniques in mind. However, with time constraints and desire to limit scale of changes necessary I deduced a list of classes that would *need* to be modified on greater scale and others which would require minimalistic alterations.

Now even mentioning the necessity to modify multitude of objects to refactor a singular aspect of the system may set off a red flag for some, and I can unfortunately assure that there were plenty more. Which is why I **had** to fix this to be in-line with the quality of code elsewhere within the system (further discussion on this refactor in Friday section).

One of things that became clear to me on this day was that working intermittently between various levels of abstraction can be tough. To be specific I worked on very low-level data manipulation, high level web/front-end/hosting front as well as managerial (even if for short period of time). Whilst I'm perfectly able to focus on each individual level separately, switching between planes whilst being engrossed in a specific problem is not something particularly enjoyable and something I will have to work on in the future!

## Friday
To end the week, I focussed solely on solving the low-level issue which I began solving day prior. 

What was quite useful was the fact that I had already isolated very fundamental function calls to the interop - great I can reuse these! On top of having these functions, I had functions which utilised this low-level logic to evaluate basic *concepts*. These didn't belong at this level so I moved them up where they made more sense.

After going through the classes which I began this refactoring process in and realising that the class did *waay* too much, on way too many levels of abstraction I decided to figure out what's the level below this class was. This turned out to be relatively high-level abstraction, clearly higher than the level I stripped away, but not low enough to be directly above it. Which begged the question, what lies in this gap?

Once I figured out the answer, all that remained was to write all of these layers, connect them appropriately and fix the class I started refactoring with.

As things stand at the end of the week, the low-level dependency has been isolated in a wrapper, and any changes to the library or underlying logic is constrained to this class (single responsibility principle box ticked!).

Additionally, the calling code is now much simpler to read as there aren't such huge jumps between logic planes which in turn makes functions much easier to read and follow as encapsulated calls now are more along the lines of what one would expect.

On top of it call the repetition has been reduced and error checking has been constrained to appropriate level (another handful of boxes checked off!).

Unfortunately, as figuring out fine details and untangling old dried up spaghetti did take some time, that means there is some fine tuning remaining before job can be called done.

# Other
- Began going gym again!
- Finished reading "Clean Code" by Robert C. Martin. Very fine book! I found that I have learnt a lot of the concepts and ideas within the book through feedback provided during daily code reviews and general feedback from other devs, in addition to picking up good habits and starting to drop bad ones. The breadth of knowledge, experience and advice compiled in the book is phenomenal and I shall be referencing back to it for years to come! Definitely understand why it's a recommended read for junior software developers.
- Started reading "The Shallows" by Nicholas Carr.
