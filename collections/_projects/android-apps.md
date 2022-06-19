---
layout: project
title: "Android Apps"
year: 2019
tech: "Java,Android OS,Android Studio,Mapbox API,SQLite,ADB,AVD"
category: "Education/Apps"
blogs: false
---

In final year of my undergraduate degree I selected Mobile Device Programming (20 credits) as one of my optional modules. I learnt about the underlying principles of how mobile device architecture differs from standard desktops (e.g., System-on-Chip, Package-on-Package), and delved into the Android operating system (while cross-platform app development, platform independent aspects and iOS app development was covered, focus was placed on Android due to the fact that it is the dominant mobile OS and that it's more open to development than iOS). 

During this module I made 3 apps, that focused on different components of the Android OS (activities, services, broadcast receivers and content providers) with the 4th app being an open-ended assignment that required utilisation of all 4 components.

***Note**: I'm writing this a little while after actually making the apps so some details will be missing because of that, and because this post is getting long enough already...*

## App 1: Finger painter
![Fingerpainter]({{ site.url }}/assets/images/mdp-apps/fingerpainter.png)

Starting with a provided `View` that handled on-screen drawing, I added two different Activities, one to allow brush size/shape change and one to change the brush colour. The minimum requirement was to allow 5 colour choices, however I decided to go the extra mile and utilise an external component that provided users a full colour wheel of colour choices.

By making this app I learnt how to create `Activity` navigation and how to send/receive data through `Intent`'s.

## App 2: Mp3 Player
![Mp3Player]({{ site.url }}/assets/images/mdp-apps/mp3player.png)

For this app, I was provided a simple class that handled .mp3 playback. My task was to build an app that would retrieve .mp3's within the Music folder inside the SDCard and allowed music playback even when user was in a different `Activity` or has closed the app.

I wrote the runtime permission requests handling to ensure the app can access the external storage and acquire the available .mp3 files. Secondly I built a service and binder that utilised the provided Mp3Player class and the data retrieved from SDCard to play the selected song.

Unfortunately, I didn't leave enough time to finish the app to the best of my ability, and dropped some marks in terms of several `Service` requirements (such as playback when app is closed).

## App 3: Recipe book
![Recipebook]({{ site.url }}/assets/images/mdp-apps/recipebook.png)

This app was fairly straight forward; make an app that stores recipes, shows recipes, and allows for sorting of said recipes (by title/rating).

For the implementation I created a simple, single table database by using local SQLite database and by performing simple CRUD allowed the necessary functionality. For queries and results I utilised `ContentProvider` as one would expect, which means that the database/storage could be remote and the majority of the app wouldn't be affected.

## App 4: Running tracker
![RunningTracker]({{ site.url }}/assets/images/mdp-apps/runningtracker.png)

With life-logging apps being one of the dominant sectors within the application ecosystem, I developed an app that can be used to track the location and time the user of the app spends running (for those more active, picture Strava).

The app utilised all 4 major components to implement different aspects of the functionality. By utilising modern Android runtime permissions to access fine GPS location, Mapbox API to display location (both current and historic), SQLIte + `ContentProvider` to store location points, and a `Service` + notification to record progress and show time spent running/walking.

While I personally thought the app needed more development time, to the extent that I withheld from uploading it on due date, it turned out that I undersold myself.

> "This is an accomplished implementation that meets the required functionality, but also adds appropriate additional features. The app correctly prompts for the user to grant permission to access the location of the device. On beginning logging a notification informs the user that it is ongoing, but also presents progress information - otherwise not including it on the activity would be remiss. Previous runs are listed and also viewable on the map, and cumulative statistics are presented. The user interface mostly makes good use of the available space and clearly attention has been given to the design of the views. The implementation is particularly good, making full use of the various components. Foregrounding the service would have been appropriate here. The content provider has been usefully extended - here one might envisage the URI schema providing further enhanced views onto the data. The code is well organised, named and clearly commented throughout. The report details the functioning of the application and provides some good justification for the choices made." - ***Martin Flintham (Module Convernor)***