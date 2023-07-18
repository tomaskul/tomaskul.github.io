---
layout: project
title: Expense Tracker
description: Personal expense processing/tracking CLI utility tool.
tech: "Golang"
category: "Data Processing"
blogs: false
---

For some time, I intended to put together a tool to help me analyze my personal financial expenditure. Most banks already provide some form of analytics, but unfortunately mine doesn't. I attempted this as a novice developer ~5y ago, and fairly quickly gave up.

2018 attempt faltered mostly due to scope creep and unclear priorities. To prevent another abandonment I:
- Split functionality into: *what needs doing* vs *what's already been done and I can re-use*
- Focussed on minimal feature list and quick iterations
- Minimize external dependencies
- Ensure high level of data privacy (which ruled out a fair few libraries/services/tools)

I knew that any sufficiently feature-rich data visualization tool (of which, there are plenty) would allow to perform data analytics, what my tool needed to do was:
1. Read exported transaction .csv files (easy)
2. Identify transaction category (moderate difficulty)
3. Categorize transactions (moderate difficulty)
4. Output category tallies in an interoperable format (easy) (TLDR; it's also .csv)

Using Go/Golang, practicing TDD, over span of 2months (after work hours) I put together first stable release.

Utility wise, the tool is sufficient, and is moderately easy to extend. I intentionally avoided functionality over-generalization to ensure project goals were being met. For now I'll keep repository private, but once the following tasks are done, I'll share the source code publicly. Notable outstanding tasks:
- Transaction identification process needs streamlining
- Add clear extension points to be usable with other data formats/sources

----

[Github repository](https://github.com/tomaskul/expense-tracker)