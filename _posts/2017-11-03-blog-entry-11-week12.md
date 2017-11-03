---
layout: post
title: "Blog Entry #11 – Week Twelve"
comments: false
description: "My experience during the twelfth week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twelve, phabricator, software development life cycle, c#, sharepoint, sql, subversion, svn, code review"
---

**Word count:** 726

**Week 12:** 23<sup>rd</sup> Oct - 27<sup>th</sup> Oct

# Placement
## Monday
Started the week off by continuing implementing the repository/unit of work pattern into my projects' codebase, basing it on an existing implementation within a separate project. This data access layer abstraction was quite difficult to wrap my head around due to the sheer number of interfaces and various combinations of class concretions. However, after going through it all, line by line, and trying my best to figure out exactly why each character was there, why every single expression was being used was quite informative. Exposure to professional software which has been written by someone much more experienced, gave me a rough target to aim for (both in terms of code quality and my pattern implementation).

By the end of the day however, I was completely lost in the endless layers of abstraction and was struggling with the most basic of problems. Although that's bound to happen when you get too close to the code and lose grand view of the overall goal, which would help you realise that there is a much simpler solution available.

## Tuesday
Doing some final touches to the unit of work implementation, began by removing the original SQL code which I used for learning, and replacing it with the much more structured and useful UoW. This involved a lot of cleaning up, and making the queries more secure, and easier to handle. Spent rest of the day restructuring, to make better use of the UoW and to add data verification in order to gain finer grain control of the processing and seemingly endless possible points of failure. But then again, what reliable piece of software doesn't have equally large number of fail-safes.

I started the morning by asking for feedback from Ian on my performance, to gauge how I am doing, from someone else's perspective. There's only so much I am able to observe and process myself without some outside input. Overall the feedback is pretty good, with me picking things up and apparently writing decent code with rare cases of me receiving feedback to change course on the approach. Hopefully I can keep up this level of performance and go a step, if not few, further!

## Wednesday

- Added database entities
- Entity repositories
- Other minor housekeeping

## Thursday
Started wrapping up the UoW integration and did general cleaning up and organising of the flow of the logic. Added new UoW instance to deal with handling front-end and towards 2<sup>nd</sup> half of the day I decided to get some project management related feedback from Ian, just to get some outside input and suggestions on how I could improve my project management approach, which is pretty lacking at this point in time. Although it is just me who's working on the project and there's no pressure on providing reports or anything it seems justified. However, I would like to have a better overall picture of how things are going and whether sufficient progress is being made.

## Friday
Spent the day organising project tasks on Phabricator, making changes based on code review comments, made further progress on UoW integration, and adding temporary fixes to some of the known issues.

(Full fix would require up to few weeks of my time in order for a reliable and solution to be found, which would be a pretty big task within itself that I currently do not have the time for. However good number of the issues can be temporarily be solved relatively easily until time comes to polish the product.)

On a different note, after a tech review, there's been a suggestion to further improve QMS within the company. From Monday, onward there will be groups formed which will audit the code that is being committed. Consequence of which is that every day an hour will be assigned to perform these reviews and further raise the bar for systems' technical quality.

# Other
- Signed up for the Great Uni Hack in Manchester
- Went home to see family on the weekend!
