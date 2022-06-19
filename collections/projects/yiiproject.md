---
layout: project
title: "Industry Year Project"
year: 2018
tech: "C#,.NET, ASP.NET, Javascript, Razor, SQL Server, Azure, Phabricator, SVN, Bootstrap"
category: "Full-stack"
blogs: true
blog1: "Placement Weeks 45 & 46"
blog1Link: https://tomaskul.github.io/2018/blog-entry-25-weeks-45-46/
blog2: "Placement weeks 26 - 33"
blog2Link: https://tomaskul.github.io/2018/blog-entry-21-weeks-26-33/
blog3: "Placement Weeks 14 - 17"
blog3Link: https://tomaskul.github.io/2017/blog-entry-14-Week1417/
---

### Brief
**The problem:** Host company's clients want to view data which is currently delivered via large .zip files, online. The data inside these .xlsx files isn't easy to port and there is no in-house, online platform to house this data.

When I joined the company, that was as much as was known, and I was there to produce a solution from the ground up. I spent the first month gathering the requirements and typing up the specs to ensure that the project was achievable, grounded, timely and had clear milestones. With stakeholder's and supervising senior developers' approval, I got started.

### Learning
The placement was a great opportunity to learn new skills, technologies, and with C# being software team's speciality, there was only one direction for me to go! After spending couple days reading through company code guidelines and familiarising myself with C# syntax, I soon realised, that apart from few differences in code conventions and concept naming differences, C# was very similar to Java, which I was quite familiar with and thus it was very easy to pick up.

Admittedly, it did take me couple of months to get up to speed with the language intricacies and getting used to strict code conventions, but it was much easier than I originally feared. With the presumed key barrier out of the way I could focus on improving my software development, project management, debugging, documentation and various other skills.

### Solution
To quickly summarise it, my solution is broken down into 3 key elements:

- Worker Daemon - Retrieve desired data from the source files
- Cloud storage - Host data & web application
- Front-end Web Application - Present data

**Side note:** I once got asked "why not simply upload those .zip files to Google Drive/Dropbox, and call it a day?". Whilst that is a very simple solution, the reasons were;

- Allow future integration into a more data-driven approach the company will be taking.
- Make data access, platform independent. Currently if you do not have spreadsheet processor, you're out of luck, which will no longer be the case.
- Updating data presentation is much simpler, as it is detached from the data.

There are numerous more benefits, but these were the key ones, in case you asked yourself the same question.

### Worker Daemon & Backend
After receiving a recommendation for a library which would aid in retrieving data, and writing a quick, proof-of-concept prototype, I was ready to start working on the actual implementation. 

One of the trickier aspects of the whole project was designing a data structure which encapsulates the way data is structured within the source files (no formal definitions, and high variability from file to file, just your average run of the mill issues) in such a way that the algorithm which scrapes data (also designed & implemented by me) needs to perform minimum amount of processing. This was of significant importance, as processing large files would be a routine activity of the daemon and thus long processing times weren't desirable. Additionally, if the data structure wasn't reflective of the source data, it would be difficult to restore the original format (another important requirement).

Alongside the processing, I had to store the data, so the MS SQL Server had to have a simple and flexible schema, which I believe I implemented successfully. This is where the table *normalization* and relationship structuring which has been engrained in my mind at least once a year for 3-4 years came in useful. However, one valuable lesson which I picked up, was that over-normalization can also be problematic/difficult to work with!

Fast forward through testing, countless iterative improvements and end of 2017 is rolling around (about half way through the placement) and I'm almost done with 50% of the intended functionality of the project (i.e. the daemon and backend). At this point I was quite deep into reading "Clean Code" by Robert C. Martin & various design patterns, both of which prompted me to perform some major refactoring within the code base. 

On one hand changing large amounts of code around the time the section of the project should be closed off, isn't the brightest idea. On other hand, the changes I performed made the messy library interaction simpler to follow & understand in addition to making source code significantly easier to test! This also came at the point when my perspective on order of operations and flow of logic shifted as I was essentially "done". This perspective at my level of experience wasn't feasible early on as I couldn't foresee the end state of the system. Then again, this is something nobody is great at, however with practice and experience can get better at, and I believe I've started that journey of improvement.

### Web Application
The web application was relatively a straight forward system. The fundamental goal was to retrieve data and structure it in the same format as the source file. Now admittedly, it's tough to know how the data looks when it's coming in, however, the data structure & database schema I designed earlier provides enough insight to be able to perform this "restructuring" with relative ease. Yay for my limited foresight!

With data displaying somewhat in place I realised that a little detail within the web app that is fairly mundane, but needs to be in place for the web application to behave as specified, was access right management!

At this stage of the project, I put my ability to juggle responsibilities to a test. Firstly, in the bi-weekly meetings with the stakeholder (these have been running since start of the project development), this half of the project was the *showing off* half, as there was nothing of particular interest to *show* during daemon development.

However, active access right management implementation didn't provide much content to visually aid during the meetings. Therefore, I would find, smaller (yet important) aspects that would improve the web applications user experience/look & feel, which was easier for the stakeholder to understand (not to say the stakeholder wasn't understanding, but visual aid helped demonstrate the progress being made). This juggling of developing an intrinsic part of the system and ensuring stakeholder confidence that progress is being made (which it was), was quite interesting, and I probably wouldn't have been able to handle this particularly well if it weren't for the group project module during previous university year.

With my interest in security growing, and me doing advance reading for next uni year, I had another convergence of ideas which prolonged the access right management extension implementation, however made it much more robust and easier to utilize in new parts of the system which would come into play later (i.e. after my contract ends).

Now that the essential groundwork was in place, it was time to wrap up web app feature development. This part was a lot easier than I anticipated and it provided a great opportunity for me to revisit Javascript and play around with various libraries floating about within the 'eco-system'.

### Testing
As much as I was inclined to put TDD into practice, this unfortunately didn't happen. There were couple of features which I did successfully implementing by following the best TDD practices, which was a great success due to complexity of the solution required. However, with the pace of development necessary & software testing only slowing becoming an integral part of the software team, it would have been quite difficult for me to create the whole system by following TDD, especially with amount of large scale changes I so frequently enjoyed making...

On the flip side the time I spent writing tests helped me appreciate the importance of writing clean code & how good unit tests aid in helping find bugs and issues which aren't obvious at first sight. I have since taken this experience and began writing unit tests for all of my active side projects, which helped speed up my development and produce more elegant solutions (some of these side projects may make an appearance on the project list soon).

**Side note:** The conflicting views I have just expressed regarding unit test (not writing them because they'd slow down development vs unit tests speeding up development) comes down entirely up to priority management. As in, it was important for me to finish the MVP, and if I wouldn't have enough time to write implementations to back the tests, additionally, the maintainer (far more experienced than me) and the new tester would likely do a considerably more thorough job than me anyway. This isn't ideal of course and may sound like me avoiding responsibility, but it's just me being realistic, on top of which what software project has ever ran perfectly in sync with the best practice, all the time and was delivered in time and within budget? (not being rhetorical, I'd be greatly interested in learning about them, if they exist).

### End note
As a whole I would say the project has been a success, as it was completed on time and met or exceeded the original requirements. Project aside, I personally took every opportunity to learn as much as I could not only within software development, but across different parts of the business and I am genuinely grateful I had this opportunity.

Lastly, it would be wrong and false to say I did all this learning and growing on my own. Number of people across the whole of the host company helped me out throughout my stay, and I am truly grateful for everything!

## Tools/Languages used in Development

- C# + .NET Framework
- Microsoft SQL Server
- ASP.NET MVC
- Azure (hosting the web app + related infrastructure)
- Javascript, JQuery and number of small JS libraries.
- SVN (Version control)
- Phabricator (Kanban + code reviews)
