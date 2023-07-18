---
layout: project
title: Expense Tracker
description: Personal, expense tracker CLI utility application.
tech: "Golang"
category: "Data Processing"
blogs: false
---

For some time, I intended to put together a tool to help me analyze my personal financial expenditure. Most banks already provide some form of analytics, but unfortunately mine doesn't. I attempted this as a novice developer ~5y ago fairly quickly gave up.

Initial attempt back in 2018 faltered due to scope creep and overambitious initial design. To prevent another abandonment I:
- Split functionality into: *what needs doing* vs *what's already been done and I can re-use*
- Focussed on minimal feature list and quick iterations

I knew that any sufficiently feature-rich data visualization tool would allow me to extrapolate trends and perform other forms of analysis, what my tool needed to do was:
1. Read exported transaction .csv files (easy)
2. Identify transaction category (difficult)
3. Categorize transactions (easy)
4. Output category tallies in an interoperable format (easy) (TLDR; it's also .csv)

Using Go/Golang, practicing TDD, over span of 2months (after work hours) I put together v0.1.0-alpha of the tool.

Utility wise, the tool is sufficient, and is moderately easy to extend. I intentionally avoided over-generalization of functionality to ensure project goals were being met. For now I'll keep repository private, but once the following tasks are done, I'll share the source code:
- Transaction identification process needs streamlining
- Add clear extension points to be usable with other data formats/sources

[Github repository](https://github.com/tomaskul/expense-tracker)