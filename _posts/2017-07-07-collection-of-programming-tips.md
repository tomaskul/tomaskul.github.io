---
layout: post
title: "Programming Tips"
comments: false
description: "A small collection of programming and software development related tips"
keywords: "software engineering, software development, tips"
---

In order to write higher quality code, to better understand approaches taken to solving problems, conventions used and many other aspects of programming (which I couldn’t list of top of my head as of first writing this), there is a lot of information about practices and techniques used to know, understand and utilise in order to become a great programmer. As currently my programming experience is quite limited, I have decided to collate tips, advice and various other useful pieces of information in one place, to be used as a reference when coding.

Remark: Some of items in this post will be very basic, some may become irrelevant over time or not even apply to certain programming paradigms (i.e., there’s going to be a lack of tips which would be relevant to someone writing a functional program). As time goes on I will add and modify the content to ensure its accuracy and get rid of typos. Lastly, this is meant to be a personal reference sheet and in its current state of completeness and quality I wouldn’t recommend anyone to use it. Refer to the sources provided in the references section below.

---

## Table of contents

1. [Basics](#basics)

      1.1. [Naming](#naming)
      
            1.1.1. [Consistency](#consistency)
            
            1.1.2. [One letter variables in loops](#one-letter-variables-in-loops)
            
            1.1.3. [Choosing names](#choosing-names)
            
      1.2. [Commenting](#commenting)
      
      1.3. [Code duplication](#code-duplication)
      
      1.4. [Minimise class surface](#minimise-class-surface)
      
      1.5. [Complexity](#complexity)
1. [Design Patterns](#design-patterns)
1. [Principles](#principles)

      3.1. [SOLID](#solid)
      
      3.2. [YAGNI](#yagni)
      
      3.3. [DRY](#dry)
      
      3.4. [Composition vs Inheritance](composition-vs-inheritance)
1. [Other](#other)

      4.1. [Code daily](#code-daily)
      
      4.2. [Read high quality code](#read-high-quality-code)
      
      4.3. [Useful reads](#useful-reads)
      
            4.3.1. [Programming](#programming)
            
            4.3.2. [UX / Design](#ux-/-design)
1. [References](#references)

---

## Basics
### Naming
#### Consistency
Regardless of chosen naming/spacing convention, applying the conventions _consistently_ matters. For example if the given naming 
convention specifies using only upper case letters for constants within the application, then stick to it as personalising the code 
opposed to keeping entire codebase in the same format, causes readbility, consistency and various other minor issues.

> White space increases readability and should be used to separate ideas just like paragraphs in prose.<sup>(reddit, 2017)</sup>

#### One letter variables in loops
E.g. _for_ loop, the outer loop should be **i**, inner loop should be **j**, then **k**, etc. This is easier to follow for most 
people <sup>(reddit, 2017)</sup>.

```
for(int i = 0;...){
  for(int j = 0;...){
    for(int k = 0;...){
      ...
    }
  }
}
```

#### Choosing names
Useful when choosing names<sup>(reddit, 2017)</sup>:

- Variables are nouns: ( ```hourly_rate``` )
- Functions that do something are verbs: ( ```compute_sum()``` )
- Functions returning a boolean are questions: ( ```is_max()``` )

### Commenting
> Use comments sparingly, usually to reference external documentation or other resources. Filling your code with obvious comments liked 
> int balance; // balance of account isn't useful and just creates noise. Additionally if you feel the need to excessively comment your 
> code it's a good sign you aren't being clear, try adding more methods and making your code simpler to understand.<sup>(reddit, 2017)</sup>

**_To be expanded upon..._**

### Code Duplication
> Don't repeat yourself. This includes not analyzing your code for areas where you could generalize a bit. This is a fine line though 
> because there is such a thing as too general or too abstract. Instead of using variable names such as num1, num2, num3, ..., numN 
> use more appropriate data structure(e.g., array, dictionary, list)<sup>(reddit, 2017)</sup>

### Minimise class surface
> Not everything needs to be public. If it shouldn't be called by any other code, it should be private. The fewer public members that 
> are exposed the easier it is for someone else to understand what your class does and how to use it.<sup>(reddit, 2017)</sup>

### Complexity
If a specifc function (or method) performs more than the name of the said function, then there's a chance the code inside is too complex. 
Far more desirable, recommended and professional approach is breaking down functionality into as small and singular behaviour as possible. 
For example if you're doing some sort of damage calculation within a game, do not maitain entire calculation formula inside a single 
function, and break it down into smaller more modular parts.

**_To be expanded upon..._**

## Design patterns

## Principles
### SOLID
[https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design))

### YAGNI
[https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)

### DRY
https://en.wikipedia.org/wiki/Don%27t_repeat_yourself

### Composition vs Inheritance
> Most classroom courses love them some inheritance, but in the real world composition via interfaces is much easier to test and 
> maintain. Composition forces you to make your code more modular which makes it easier to test. It also gives you the flexibility of 
> mocking out interfaces until you are ready for them, which lets you focus on the task at hand during development instead of 
> "hopping around" to various functionality when trying to complete a task. This added focus tends to make you write better code in 
> earlier iterations since you are not trying to juggle too much scope in your head at once.<sup>(reddit, 2017)</sup>

**_To be expanded upon..._**

## Other
### Code daily

>By everyday, I mean everyday! How do professional athletes improve their skills? By practicing on a daily basis. Sure there can be off-days, where you take a break from it, but this should not be the norm. Name one athlete that won a gold medal by only practicing once or twice a week. Learning how to code is very similar to learning a new language or art. It takes a lot of practice! You can know everything there is to know about computers. But without practice, you won't be able to write code that is maintainable, let alone write something that people would actually want to read.<sup>(The Coding Delight, 2017)</sup>

### Read high quality code

>Every developer should read high quality open source code. When I first went through underscore.js and jQuery (not the entire code base), my mind was blown. Let me warn you: because the code is written by professionals, readers need to have a strong foundation in programming and in the language that the source is written in. In the the case of underscore and jQuery, the language would be JavaScript. 

>In order to get a good open-source education, I recommend finding source code that is
> - Relatively short (roughly around 1000 lines or less would be ideal)
> - Well documented.

>I recommend reading relatively short source code for two reasons. Firstly, short source code means readers don't have to spend as much time navigating the source to connect the pieces. Secondly, readers can fully understand shorter code bases much faster than a framework that has 100,000 lines of code. Shorter code bases such as modules are compact. Readers only see what they need to see.<sup>(The Coding Delight, 2017)</sup>

### Useful reads
#### Programming
- [Survival Guide for Junior Developers](https://medium.com/learning-new-stuff/survival-guide-for-junior-developers-d35371dd0818)
- [10 Tips on How to be a Great Programmer](https://blog.jooq.org/2017/05/09/10-tips-on-how-to-be-a-great-programmer/)
- [The Definitive C++ Book Guide and List](https://stackoverflow.com/questions/388242/the-definitive-c-book-guide-and-list)
- [Design Patterns / Design Antipatterns / Refactoring / UML](https://sourcemaking.com/)


#### UX / Design
- [User Experience Professionals Association](http://uxpa.org/)
- [Level Up Your CSS Skills With These 20 Pro CSS Tips](http://webdesignerwall.com/tutorials/level-css-skills-20-pro-css-tips)
- [Good design is invisible: an interview with iA's Oliver Reichenstein](https://www.theverge.com/2012/7/24/3177332/ia-oliver-reichenstein-writer-interview-good-design-is-invisible)

## References

1. u/ericsw & u/wseymour on reddit. (2017). How do you learn to write better/cleaner code? • r/learnprogramming. [online] Available at: [https://www.reddit.com/r/learnprogramming/comments/69eexp/how_do_you_learn_to_write_bettercleaner_code/](https://www.reddit.com/r/learnprogramming/comments/69eexp/how_do_you_learn_to_write_bettercleaner_code/) [Accessed 8 May 2017].
1. The Coding Delight. (2017). The 5 Effective Methods for Becoming a Better Programmer. [online] Available at: [http://www.thecodingdelight.com/become-better-programmer/](http://www.thecodingdelight.com/become-better-programmer/) [Accessed 17 Jun. 2017].


## Fixes and notes for the future
- Add few published sources to back up any statements I made or quoted from memory
