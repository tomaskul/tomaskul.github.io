---
layout: project
title: "AUDRI - Automated Driver"
year: 2017
tech: "Java 8, JavaFX, WEKA, GitLab, Adobe Photoshop CS6, Trello, CSS, Markdown"
category: "AI Simulation"
blogs: false
---

![Audri]({{ site.url }}/assets/images/audri.png)


### Acquiring the project
As one of the year-long 2<sup>nd</sup> year Computer Science modules, I had to work on a specific project with group of my peers. The first stage of acquiring the project included writing expressions of interest towards 3 of our groups' preferred projects, and doing a small presentation pitching ourselves to the project supervisors. We successfully received offer to work on our 1<sup>st</sup> choice project which involved developing and implementing an inverse reinforced learning algorithm (En.wikipedia.org, 2017) which given a demonstration of a driving style, would be able to learn and replicate the shown behaviour.

### Team
Our team was comprised of total of 6 people with good distribution of skills and experience across the board (i.e., GUI experience, Computer Science with Artificial Intelligence students). As we all understood that self-driving vehicles are the way of the future, and found the project involving development of AI which is capable of learning to drive itself quite exciting, which is not only motivated to pick this project, but to also be driven and motivated to completing the project.

At the start of the project we all agreed that in order to best utilise our skills and expertise we would split into 3 sub-groups: one to develop the artificial intelligence, one to develop the simulation, and one to develop the graphical user interface which is where my responsibilities resided.

### The Project
Here's an excerpt from the project brief, outlining the specification of the project

>Apprenticeship learning also known as learning by demonstration or imitation learning, is a machine learning approach for generalising the demonstrations provided by an expert. This project involves implementation of a Java based tool which contains a simulator for driving a car on a high way with multiple lanes and a chosen apprenticeship learning technique to learn how to drive safely avoiding collisions. The car under control will have a fixed speed higher than the other cars on the way. The left lane should be preferred over the middle lane over the right lane, over driving off-road. The goal is to generate an AUtomated DRIver (AUDRI) by learning to drive properly on the highway mimicking the behaviour of a demonstrator and if possible, even improving the learning process by using the data obtained from some previous demonstrators. The tool should also allow a user to evaluate/observe his/her safe driving skills as compared to AUDRI on the same simulation interface.

### My role
I volunteered to work on the GUI implementation of the program, which included many responsibilities, such as: correctly drawing the simulation, responding to design suggestions, fixing graphical bugs, providing consistent appearance to the application and more.

I began by creating concept of the design (paths of navigation, structure of the interfaces and classes). I progressed forwards by creating a 3-Dimensional ArrayList of images data structure to house different layers of the simulation view (one layer to store the road/ground, 2<sup>nd</sup> to store the traffic cars & 3<sup>rd</sup> layer for the user/AI vehicle). However, this approach was very inefficient, slow and wasteful which is why I quickly changed direction to reduce memory usage and to make simulation view refreshing quicker by not storing all the image data, but rather initialising the road and only updating the vehicles when necessary.

Once the core of the drawing functionality was implemented, all that remained was tying together all of the separate branches of the development and ensuring that the program operates seamlessly and that the team members working on other aspects of the program could test of functional bugs (i.e., collision detection precision, AI behaviour) outside the JUnit tests.

My role concluded by me adding fullscreen functionality to allow better showcasing the core of the program, stylising the appearance through use of CSS and animation effects. With the final touch being introduction of the Demo screen which is a separate instance of the simulation, which demonstrates the AI, running entirely on its’ own in a slightly more visually appealing screen with addition to some key metrics (collision count and overtake count).

### Final product
Once the project had concluded, our team had produced a program which met all the specified requirements, followed good code practices, had simple and easy to follow user interface, ran without any problems.

The project has been great and very valuable experience in developing actual software whilst following common industry practices (Agile based).

The video below showcases the finished program and the AI running on its own!

<div class="video-container"><iframe src="https://www.youtube.com/embed/zw0KIRQLVNU" frameborder="0" allowfullscreen></iframe></div>

### Demo day
At the end of the project (17<sup>th</sup> of May 2017), our and every other group working within this module, had to come together and in convention style format present their complete projects.

Professors, staff and students of the University, and representatives from sponsoring companies (some projects were hosted by companies such as MHR and Sumo Digital) were the guests who made their way around the demo day grounds and inquired us about the project.

This was great experience in pushing me to be able to pitch and describe the program and the experience of working within the group to many people with range of technical knowledge.

[Photo of our group during the demo day to be added sometime in the future]

## Tools/Languages used in Development

- Java / JavaFX 8
- WEKA (Waikato Environment for Knowledge Analysis)(Cs.waikato.ac.nz, 2017)
- GitLab (Version control)
- Adobe Photoshop CS6 (Poster creation)
- Trello (Web-based alternative of a Kanban board)
- CSS
- Markdown (GUI Documentation)

## References

En.wikipedia.org. (2017). _Apprenticeship learning._ [online] Available at: [https://en.wikipedia.org/wiki/Apprenticeship_learning](https://en.wikipedia.org/wiki/Apprenticeship_learning) [Accessed 8 May 2017].

Cs.waikato.ac.nz. (2017). _Weka 3 - Data Mining with Open Source Machine Learning Software in Java._ [online] Available at: [http://www.cs.waikato.ac.nz/ml/weka/](http://www.cs.waikato.ac.nz/ml/weka/) [Accessed 8 May 2017].
