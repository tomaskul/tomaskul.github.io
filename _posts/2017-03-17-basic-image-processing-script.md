---
layout: post
title: "Basic Image Processing Script"
comments: false
description: "Matlab script which is able to separate plant from background elements in a given image"
keywords: "script, university, project, matlab, image processing"
---

![Iip]({{ site.url }}/assets/images/iip.png)

During 2<sup>nd</sup> year of my degree, I picked an introductory module to image processing, and was assigned to create a simple image processing script which implements some of the core image processing principles in order to generate a binary image from a small set of pictures of plants. Image above shows one of the original plant images alongside the output my script generates.

Although my script was simple, relatively fast and used toolkit functionality there were number of issues with my implementation such as it not being 100% reliable (script struggles dealing with shadows, and certain shades of green), more than ideal amount of noise makes it to the output image and few other minor problems.

## Tools/Languages used in Development

- Matlab R2015b
