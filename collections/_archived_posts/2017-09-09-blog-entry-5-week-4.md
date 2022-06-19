---
layout: post
title: "Blog Entry #5 – Week Four"
comments: false
description: "My experience during the fourth week on the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week four, phabricator, windows services, software development life cycle, c#, java"
---

**Word count:**  636

**Week 4:** 28<sup>th</sup> Aug - 1<sup>st</sup> Sep

# Placement
## Monday
Bank holiday

## Tuesday
On the way home last Friday, I realised that requirement spec outlined that the project will take most of the year, so first thing on Tuesday I adjusted the scope to ~half of the year to match my self-imposed goal.

One-to-one with my line manager discussing objectives and my progress, these will be monthly from now on.

Looked into C# and Interop, and began implementing a way to generate the data structures which the project will require.	

## Wednesday
Health & Safety inspection of my working environment first thing in the morning. Continued the day by finishing implementing proof-of-concept application which generates the data structures I’ll need later in the project.

Would have been even more productive if C# Interop wasn’t garbage (tooltip provides description opposite how an object behaves)

## Thursday
Sorted out working from documents so that I could work from home during the upcoming rail strike (additionally a generally useful option to have!).

First half of the day spent implementing Java Apache POI as an alternative to the C# based approach which I’ve taken so far (always important to investigate alternatives and derive the most suitable approach to solving a particular problem).

After getting some input from guys at the office, I went on to spend rest of the day refactoring my C# code from earlier in the week, as they have insisted that garbage, but *working* proof-of-concept code can, and likely would end up in final product. Which requires no further explanation for why that would be problematic for everyone. And even though I intended to write methods and classes from scratch, simply basing everything on proof-of-concept, I didn’t want to run the risk of that happening and cleaned up the proof-of-concept code.

Nonetheless it is still quite poorly documented and structured, it is far better than what I had before.

## Friday
First day working from home, nearly overslept the daily stand-up, and with some IT issues I managed to get started. My goal for the day was to implement my proof-of-concept code into a daemon, where lies the biggest dev risk of the project (as identified by one of the most senior developers in the office).

Prior to being able to work on my target task, I ran into an issue where my data structure was returning null values where I was expecting, well, not nulls. I ended up spending majority of the day trying to solve this issue as it took priority at the time. Went through my usual means of debugging and – nothing.

I turned for help to Lee, who quite quickly found the source of the problem – which was my ingenious self’s’ attempt at reusing an object for passing values to a different method. My approach would pass objects’ value and then wiping the original object to be reused when required, with assumption that local scope variables which receive the value would be able to do their thing. Turns out this is not the case.

With the issue quickly resolved, I began working on my intended task of the day however I quickly ran out of time and decided to finish this next week.

# Other
During this week I spent little time simply cleaning up some things within my own project, no significant progress, just minor changes to aid code readability (mostly just replaced some ints with enums).

Updated my portfolio website, by moving my projects into separate pages. This helps categorising things, only blog posts appear on the home page, and project URLs make sense.

Also a traditional bank holiday bike ride, only ~80km this time around.

# Summary
Overall quite a good week, slightly less progress on my personal project than I would have liked, but it’s also important taking some time off and just relaxing!
