---
layout: post
title: "Blog Entry #19 – Week Twenty Four"
comments: false
description: "My experience during the twenty third fourth of the placement"
keywords: "placement, uni, university, blog, internship, software engineering, software development, week twenty four, software development life cycle, c#, azure, cloud storage"
---

# Placement Week 24 (22<sup>nd</sup> Jan - 26<sup>th</sup> Jan)
## Monday
Started the morning off by implementing the UoW/Unity IoC workaround that Lee had suggested week previous, and went straight into the meeting with the customer. As I had cancelled the previous meeting due to ongoing refactoring/restructuring and being in midst of sorting out deployment details (domain name, storage and DB etc. quotes), this meeting was quite important (at least in my eyes).

## Tuesday
Team meeting; there will a change in team meeting structure from here on, to make it more open and less *structured*. And a similar change will occur in the monthly one-to-one sessions which it will, or at least in theory should be less systematic. Which I support, we shall see what results these changes will have.

The changes come after the team leader attended performance management workshop/talk not long ago! All of this aside, I don't particularly recall what I worked on through the day... I suppose noting details down would be helpful when it comes to writing these...

## Wednesday
Spent first hour of the morning with Lee, teaching Ben (software tester) how to write unit tests in MSTest v2.

As I brought up in the team meeting on Tuesday, one of the major, ongoing tasks for my project at this point in time, is to catch up with the backlog of unit test which should ideally exist and be available. Which is where Ben comes in, as he will have to write unit tests for a much more important project, my small- scale system would be a good place to get started. However, I didn't give him the *easiest* class to test (even though there's only one method). But in essence, having Ben practice writing unit tests on my code base, and me getting the testing lifted off my shoulders is a win-win-win situation.

Now this is the unfortunate part, I spent remainder of the day trying to figure out why all of the `async` calls of azure store were not waited for. I tried multiple different approaches and means of `await`-ing for all the `async` calls, to the point where out of desperation I forget `async` calls to run synchronously...

Apart from proving that waiting for tasks to finish *is* the key issue I am having, I was unable to solve it. I have been trying to fix this for second day in a row now, and it's getting quite annoying to say the least. Even though I am using all the calls correctly (to best of my knowledge and search) the results are simply not there, which means my plan for Thursday is to read into the details of how Tasks work in C# as it seems like my azure calls are done correctly.

## Thursday
With a little help from Lee the `async` issue has been fixed! It turns out that I accidentally went a step too far and used `async` method, inside internal `async` method call, which just doesn't work (at least for what I was trying to achieve)...

With that out of the day I started doing general QA to see whether everything else is working and finally, *finally* got to the point where I felt confident about testing whether my system could process multiple excel files. As it turns out that was not the case, however most of the fallout happened on Friday.

## Friday
As it turns out, the Microsoft Interop cannot handle interaction with multiple threads. Which is a pretty annoying, as that’s exactly what I am trying to accomplish.

After debugging the thread clashes I came across a specific error which was nondescript enough to make finding solution for it rather long winded and as it turns out there’s essentially one workaround available which I *should* in theory be able to utilise and not make too many changes to my existing infrastructure.

The workaround essentially filters the clash messages that the interop throws and tells the thread what to do accordingly.
All of this sounds like more work than I originally anticipated, but a workaround has been found! But as all things go, the situation wasn’t all that simple. It turns out that the Message Filter (look up “C# OleMessageFilter”, it’s **not** the one in `System.Windows.Forms`) only works in an `STAThread` which is problematic because Task Parallel Library which I am using to create parallelism defaults to `MTAThread`.

One of the means to dealing with this issue was……

As you can tell this was starting to get out of hand, and luckily it was the end of the week. So, I noted the details down and left these issues do deal with on Monday.
