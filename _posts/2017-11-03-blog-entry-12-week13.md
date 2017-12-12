---
layout: post
title: "Blog Entry #12 – Week Thirteen"
comments: false
description: "My experience during the thirteenth week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week thirteen, phabricator, software development life cycle, c#, sql, subversion, svn, code review, debugging"
---

**Word count:** 772

**Week 13:** 30<sup>th</sup> Oct - 3<sup>rd</sup> Nov

# Placement
## Monday
The new code review process begins, I received a ton of feedback and audited someone else's code for the first time (pretty pointless suggestions in grand scheme of things, but hey! need to start somewhere).

Spent the morning by going through old commits and making sure that the changes I have made to fix any of the concerns, are reflected by getting the old commits validated. Spent rest of the day making countless fixes based on the suggestions during code review.

## Tuesday
Second day of the new audit routine - I was the only one who committed code on Monday (*yay*?), the consequence of which was everything I wrote being shredded to bits. Which then lead me to spent the whole day going through every single comment and making the amendments on the suggestions made.

With the changes made I decide to go with the overwhelming number of commits approach so that the auditors get off my case and I can actually make progress.

**Edit from the future:** Last paragraph is me half-heartedly joking about the reviews (my sarcasm comes off really badly in text it seems), however what has become abundantly clear is that philosophy of:

> Measure twice, cut once

is much more productive and progressive than countless, half-arsed attempts at solving a problem.

## Wednesday
It appears that is wasn't my countless commits, but rather better code that managed to reduce number of suggested improvements which got me start the day by making minor fixes to code I wrote on Tuesday.

With fixes done I went on to plugging things together and began dealing with possible concurrency issues, data type conversions issues (multiple mutations are pretty tough to do correctly) and continued by thinking through the high-level system logic.

Additionally, I made appropriate unit test changes to reflect changes I have made with the useful suggestions I received during morning code reviews and reviews Ian has been conducting throughout duration of the project.

Lastly, I removed a bug, which rendered a whole method useless. The bug was picked up by the updated unit test, and the single line of code which caused the issue was a well-intentioned, but poorly implemented safeguard against `IndexOutOfRange` exception which I saw coming.

## Thursday
Almost all, of my Wednesday's commits received approval which is a significant improvement from Tuesday! Spent the entire day implementing the high-level system logic which I intended on implementing for about a week and decided to act on based on once of the code review comments I received on Tuesday.

The intention for this level logic (at least from my current thought process), is to read roughly like a robot-like excerpt from requirement spec for the project.

Overall made good progress and quite pleased with code I have written today! (Believe this might be some of the better from-scratch code I have written in a while, if not to date, but will see what guys think about it tomorrow morning)

## Friday
All, but one of my commits got approved (unapproved one was due to some commented out code which I forgot to delete...) which is a complete 180 on state of my project from start of the week.

Decided to spend the day doing some housekeeping things and getting the system to a presentable state. 

*I forgot to mention that during Monday stand-up, Ian suggested that I get the software to the point where it can perform the most essential of its' purpose by the next client meeting, which means I had 2 weeks to meet that agreeable target. 1 week remains.*

To kickstart myself and ensure I meet this target I:

- Fixed SQL command issue (I have and always will dislike race conditions)
- Fixed dependency injections issues (Surprise, surprise, race conditions yet again!)
- Tested whether the high-level logic, and conjunction with rest of my system works as intended, and to my surprise and joy - it did!

Lastly to finish of this rollercoaster of a week I also:

- Did my-no-weekly update to my burn down chart (number wise - not looking so good, but realistically - a lot of progress has been made)
- Helped teams' software tester with some tasks regarding a different company project

## Other
- Got back into playing Civ
- Bought number of books, and games on steam
- Application to the Great Uni Hack in Manchester got approved, and I received an invite. If all goes well and my plans do not change, will be going to my first Hackathon in a while!
- Have been watching the new season of Mr.Robot
