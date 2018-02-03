---
layout: post
title: "Blog Entry #20 – Week Twenty Five"
comments: false
description: "My experience during the twenty fifth week of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twenty five, software development life cycle, c#, asp.net, mvc, model view controller, razor, user roles, user role based authentication, claims based authorization"
---

# Placement Week 25 (29<sup>th</sup> Jan - 2<sup>nd</sup> Feb)
## Monday

- Half the office is off to an introductory C++ course, even though half of them are either seasoned C++ developers or are familiar enough with OO and C-based languages to be able to jump straight into advanced (strange!)
- Due to a meeting, didn't get a chance to go through ASP.NET MVC stuff with Ian, moved the meeting to Tuesday.
- Realised the parallel processing hurdles I was faced with at the end of last week are *currently* not worth the investment of time and energy, as the front-end development needs to begin *ASAP*. Which is why I spent the day renaming classes/methods, and organising code so that there is a stable version of the project, at least somewhat ready for the 3rd design review. Any changes past this point will be improvements and the commit I tagged (I'll never get used to SVN naming) can always be used as a fall-back.

## Tuesday
Spent part of the day going through the back-end system, reviewing key functionality, which lead to finally producing a build of a windows service instead of running a local test-bench. I haven't built an actual service with my code on it in a while, which isn't ideal, but then again I have been preoccupied with getting the thing to actually work...

Latter end of the day was spent with Ian, and him trying to explain how ASP.NET (core) MVC works. The few hours spent going over how the framework works were quite helpful, however as I didn't write anything and generally felt tired by that point in the day, I didn't manage to get as much out of the little walkthrough session as I had originally intended (i.e., asking deeper questions about how the framework structure works and is intended to be developed against).

## Wednesday
In order for me to better understand how ASP.NET MVC works I spent the whole day just messing around with it. I tackled with the user database migration for a while and got overly excited when I finally got it populate a database. Also, finally got around to getting in touch with Alistair and asked him to sort out some of the IT tickets which I had for several weeks now (admin rights, and printing).

By the end of the day I was noting down which exact user roles I will need to have and what actions would those roles entail. As a whole, no real progress towards front-end development, but *some*, relatively important head-space and understanding focussed work was done. After working at relatively low level for about a month, thinking on several levels of abstraction higher is proving to be tough.

## Thursday
Moved away from working with ASP.NET Core MVC, to .NET Framework variant, to ensure a class library I used for back-end is compatible with the front-end. I utilised some of the migration tools to auto-generate database tables and establish some basic role relationships. Useful as that's one thing I will not have to worry about too much for time being.

By the end of the day I had a fairly decent understanding of how the MVC works under this framework, and I began playing around with Razor syntax. That being said, I still have lengths to go before I can be even relatively confident in my ASP.NET skills. This comes as I haven't fully investigated framework, and haven't looked at the bigger picture of the problems it solves, but given time and and practice this should be a breeze (I hope).

Yet again not much "*actual*" progress, but I believe it's relatively important for me to understand __what__ it is I'm working with, and __how__ it works, before I try to solve all the business problems I'm facing.

## Friday
Friday went along similar lines as previous couple of days. I didn't make too many advances toward end goal. However, I finally initialised the project inside the main system solution, and removed all the auto-generated fluff that isn't needed by the front-end (FB/Google credentials for a proprietary, in-house product? hahah, no thanks).

In the morning I set out a plan to work on user role claims, as I got the roles into the system quite quickly. But now as I'm typing this out, I realised I *should* have checked that I got the roles working correctly.

Either way, claims weren't what I ended up working on, instead I:

- Separated the default login/registration implementation, as external registration is not a feature of the system.
- Changed access level on all controllers to require authentication, except for login page.
- Login page has a different default `Layout` from remainder of the site.
- Did some minor formatting to the login screen (i.e., added placeholder text to textboxes instead of using auto-generated labels)
- Sprinkled in company details around usual places like contact page and the site footer.

By end of the day I realised I've skipped quite few steps which I need to take before I can implement what I had in mind throughout the day - which was selecting user role and specifying claims (with some default ones already set) inside the user registration form. Which means Monday will be spent bringing the DB elements I've worked on generating for past ~4-5months to the front-end.
