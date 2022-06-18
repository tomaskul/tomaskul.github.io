---
layout: post
title: "Blog Entry #18 – Week Twenty Three"
comments: false
description: "My experience during the twenty third week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twenty one, software development life cycle, c#, azure, cloud storage"
---

# Placement Week 23 (15<sup>th</sup> Jan - 19<sup>th</sup> Jan)
## Monday
Ask Ian whether I could get some (even minor) involvement with other projects, to observe reviews and the like. This comes after my realization that I haven't been particularly proactive recently. Luckily there were few places for me to be present. Started by simply observing how senior devs decoupled old, *very* poorly written and structured SQL view (also at this point, any sympathy towards sub-queries had been completely killed off).

The general approaches where similar to how I would have approached the problem, however it was easy to tell that they had *far* more experience dealing with poor code (i.e. actually getting it to not be awful). Breaking the problem down into manageable chunks, identifying which of those chunks it the primary cause for concern and figuring out ways of how to resolve the issue was their approach and that's really the right way of tackling this type of a problem.

Having said that, the number of possible solutions proposed by both of the devs, and ways of evaluating the options (viability and overall effect) were quite impressive, and hopefully one day I'll reach that level! Only contribution from me during this debugging session was my questioning of reason behind particular hurdle for solving the biggest issue noted, which seemed to help Ian and Lee think of a suitable solution.

## Tuesday
[Forgot to note down the details of what I worked on]

## Wednesday
Just like Tuesday, didn't really note down what I worked on. However, I was _sort of low-key_ propositioned a graduate role by the team leader. Reason behind uncertainty in that phrasing is due to it being mentioned as a possible option for me to check out when I am looking for graduate roles this time next year, and not a firm offer. Also, this could be simply coming from the line manager and not whoever would be hiring me.

Either way, whether or not I explore this option will be decided in due time.  

## Thursday
Finished the `static` aspect of the unit tests that I started writing the day before, and wrote all of the unit tests for the lowest level interaction logic. I managed to find few simple bugs which may or may not have caused issues in the future, and doing the testing allowed me to easily remove several redundant, argument edge case checks knowing that nothing was broken in process.

On top of unit testing I updated the SVN ignore properties of the repo (about 5-6 months late, but better late than never I suppose)

## Friday
Friday was quite short as I decided to use some of the overtime hours I've accrued since last week. Before leaving I managed to adjust to thumbnail generation to work with newly built class which deals with azure cloud storage (very minor changes).

Once that was set, I brushed up few things, remove obsolete tests, and checks from code I was unit testing on Thursday, following feedback during morning code review.
