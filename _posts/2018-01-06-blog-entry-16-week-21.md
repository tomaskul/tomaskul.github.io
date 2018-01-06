---
layout: post
title: "Blog Entry #16 – Week Twenty One"
comments: false
description: "My experience during the fourteenth, fifteenth, sixteenth and seventeenth week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twenty one, software development life cycle, c#, subversion, svn, debugging, new year, .net, refactoring, god class, god object, unit tests, data storage"
---

# Placement Week 21 (2<sup>nd</sup> Jan - 5<sup>th</sup> Jan)
## Monday
New Year's Day / Bank holiday

## Tuesday
Began the new year by attempting to figure out where I left off over a week ago and once I figure it out I carried on with the refactoring. As I was trying to refamiliarise with existing code and remember the exact changes I was adding, I didn't make too much progress. But according to others, the whole week will probably follow the same pattern.

Additionally, software tester has come back to the office after *the trampoline accident* few months back.

## Wednesday
*I don't remember what I worked on, will update this once I look back through commits and comments...*

## Thursday
Slowly began improving the main processing side of the system which has been in its' current state since the start of the project. It is enough to mention that this _class_ still bares uncanny reassemablance to the prototype I built before starting work on the actual system, to make anyone with any amount of experiece in software development cringe.

The _class_ currently is an unwieldy mess which; stretches across number of layers of abstraction, is hard to read and follow, has series of tough-to-identify dependencies, and is in genuine need of refactoring, which I finally got around to doing.

**Note to self:** once major refactoring is complete, post statistics about _the class_ and analyse the changes! (I will probably forget to do this)

Towars latter end of the day, I asked Ian to look over concurrency/`.NET` tasks to make sure I know what changes I will need to perform in order to implement one of the more instrumental aspects of the system. As things stand now, it seems like I'll only need to make few minor changes and implement a basic factory. Once that is done I will likely need to do extensive testing to ensure *everything* works as expected and to try and eliminate as many concurrency related issues as I can (near impossible to do, but will have to try!).

Additionally, I remembered that during last few weeks, the changes that I have made to the architecture of the whole project has broken most if not all of my unit tests which will have to be re-written soon. On top of all of this I also started thinking about rolling multi-threading out further into my project to increase mean cpu and ram usage and possibly slash time required to do all the processing.

## Friday
I proceeded my refactoring efforts of the over-convoluted and not-particularly reliable _god class_. After few reads I decided to take bottom-up approach as few of the methods seems to have fewer dependencies and would be easy to improve (I was *wrong*). I began with method which deals with thumbnail image generation/db data inserts, during refactoring I started questioning how my system will deal with db storage and data storage. After pondering for a while, I decided to ask Lee (senior member of software team) for some help/advice on what would be a sensible approach.

After explaining the problem I have found, he pointed out possible approaches and a potentially huge security issue, which I shall start resolving and circumventing next week. Overall I didn't get as much done as I planned, but few important things got brought up that will require my immediate attention.

# Other

- Spent New Year's day travelling back to Chester, which took a *lot* longer than it should have, thanks to the awful traffic back home... Although difficult travel on New Year's day seems to be becoming a tradition for me.
- Meltdown & Spetre broke mainstream news with essentially every CPU that's out in the world being vulnerable to kernel-level attacks. Here's a good The Register [https://www.theregister.co.uk/2018/01/04/intel_amd_arm_cpu_vulnerability/](article) on the security bugs.
- Over last few months I've been reading "The Code Book" by Simon Singh, and have started enjoying breaking simple ciphers (slowly working my way up)
