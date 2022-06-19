---
layout: project
title: Music Library
description: MySQL DB with PHP/JS front-end for Y1 Uni assignment.
tech: "HTML, CSS, PHP, MySQL, JavaScript"
category: "Web"
blogs: false
---

<div class="video-container"><iframe src="https://www.youtube.com/embed/efkOz45v_aY" frameborder="0" allowfullscreen></iframe></div>

This project has been a part of "Databases & Interfaces" module during first year of my degree. The project involved;
- Creating a relational database to store various music library related data using MySQL
- Creating web-based front-end for the database using HTML & CSS
- Implementing data retrieval and input into the database using PHP
- And adding form validation using Javascript

The final front-end product allowed for users to;
- See metrics about the database
- Search for artists/albums/tracks within the database
- Append records (artists/albums/tracks)
- Edit artist/album/track data
- Delete records (artists/albums/tracks)
- Only input dessired data within appending/editing text fields (form validation)

![DatabaseTables](https://i.imgur.com/gS2FH9s.png)

All in all I managed to meet all the requirements, fit all of the code and the database within 2.74MB zip file and achieve 1st class 
mark for the project. My only takeaways are that good text editor can do wonders, and if you're using PHP in your project you better know
exactly what you're doing.

I spent good few days ensuring that the search feature which used simple SQL queries to retrieve data was somewhat protected from 
SQL injections, however someone who is more experienced (or simply enjoys listening to "DROP TABLE*") would 
definitely be able to break this music library interface.
