---
layout: post
title: "Programming Tips (WIP)"
comments: false
description: "A small collection of programming and software development related tips"
keywords: "software engineering, software development, tips"
---

In order to write better code, to better understand approaches taken to solving problems, conventions used and many other aspects of 
programming (which I couldn't list of top of my head as of first writing this), there is a lot of information about practices and 
techniques used to know, understand and utilise in order to become a great programmer. As my programming experience is quite limmited at 
this point in time, I decided to collate tips, advice and various other useful pieces of information in one place, to be used as a 
reference when coding.

Some of items in this post will be very basic, some may become irrelevant over time or not even apply to certain programming paradigms 
(i.e., there's definitely going to be a lack of tips which would be relevant to someone writting a functional program). As time goes on
I will add and modify the content over time to ensure it's accurate and as grammatically accurate as possible. Lastly, this is meant to 
be a personal reference sheet. 

---

## Table of contents

1. [Naming](#naming)

      1.1. [Consistency](#consistency)
      
      1.2. [One letter variables in loops](#one-letter-variables-in-loops)
      
      1.3. [Choosing names](#choosing-names)
  
1. [Complexity](#complexity)

      2.1. [Code Duplication](#code-duplication)
      
      2.2. [Minimise your class surface](#minimise-your-class-surface)
 
1. [Commenting](#commenting)

1. [Composition vs Inheritance](#composition-vs-inheritance)

## Naming
### Consistency
Regardless of chosen naming/spacing convention, applying the conventions _consistently_ matters. For example if the given naming 
convention specifies using only upper case letters for constants within the application, then stick to it as personalising the code 
opposed to keeping entire codebase in the same format, causes readbility, consistency and various other minor issues.

White space increases readability and should be used to separate ideas just like paragraphs in prose.

### One letter variables in loops
E.g. _for_ loop, the outer loop should be **i**, inner loop should be **j**, then **k**, etc. This is easier to follow for most 
people.

```
for(int i = 0;...){
  for(int j = 0;...){
    for(int k = 0;...){
      ...
    }
  }
}
```

### Choosing names
Useful when choosing names:

- Variables are nouns: ( ```hourly_rate``` )
- Functions that do something are verbs: ( ```compute_sum()``` )
- Functions returning a boolean are questions: ( ```is_max()``` )

## Complexity
If a specifc function (or method) performs more than the name of the said function, then there's a chance the code inside is too complex. 
Far more desirable, recommended and professional approach is breaking down functionality into as small and singular behaviour as possible. 
For example if you're doing some sort of damage calculation within a game, do not maitain entire calculation formula inside a single 
function, and break it down into smaller more modular parts.

### Code Duplication
> Don't repeat yourself. This includes not analyzing your code for areas where you could generalize a bit. This is a fine line though 
> because there is such a thing as too general or too abstract. Instead of using variable names such as num1, num2, num3, ..., numN 
> use more appropriate data structure(e.g., array, dictionary, list)

### Minimise your class surface
> Not everything needs to be public. If it shouldn't be called by any other code, it should be private. The fewer public members that 
> are exposed the easier it is for someone else to understand what your class does and how to use it.

## Commenting
> Use comments sparingly, usually to reference external documentation or other resources. Filling your code with obvious comments liked 
> int balance; // balance of account isn't useful and just creates noise. Additionally if you feel the need to excessively comment your 
> code it's a good sign you aren't being clear, try adding more methods and making your code simpler to understand.

## Composition vs Inheritance
> Most classroom courses love them some inheritance, but in the real world composition via interfaces is much easier to test and 
> maintain. Composition forces you to make your code more modular which makes it easier to test. It also gives you the flexibility of 
> mocking out interfaces until you are ready for them, which lets you focus on the task at hand during development instead of 
> "hopping around" to various functionality when trying to complete a task. This added focus tends to make you write better code in 
> earlier iterations since you are not trying to juggle too much scope in your head at once.

## References
u/ericsw and u/wseymour on reddit 
(https://www.reddit.com/r/learnprogramming/comments/69eexp/how_do_you_learn_to_write_bettercleaner_code/)

## Fixes and notes for next commit
- Formalise references section and add inline reference to a figure in references section
- Add few published sources to back up any statements I made or quoted
- Look up "SOLID", "DRY" and "YAGNI"
