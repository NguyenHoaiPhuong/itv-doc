---
title: "Coding Guideline"
linkTitle: "Coding Guideline"
weight: 1
description: >
  Good practices for coding style.
---

{{% pageinfo %}}
This is a placeholder page that shows you mandatory coding styles to achieve maintainable and structured code for both frontend and backend.
{{% /pageinfo %}}

As a member of the dev team, you should strive to abide by the following guidelines. That being said, no one is perfect, but checking most of these points should be a requirement to allow us to move fast, be productive and have a good time.

## Requirements

### Produce quality & maintainable code

* It works well & there are no obvious bugs
* Is thought to be robust to all possible edge cases (not only the one describe in the specs)
* All the code and comments are written in perfect english
* All identifier names are clear, explanatory of intent and fully descriptive.
* It is as simple as possible (avoid complex methods structures & calls, as DRY as possible, use commonly known data structures and algorithms, avoid hacks and tricks, low cyclomatic complexity, etc).
* Hard to understand parts are well documented
* It is designed to be as simple to extend / modify as possible
* It is designed not to have performances issues on the short nor long run

### Be proactive to maintain & improve quality

* Help to review other's code and detect issues
* Help defining common behaviour and reduce duplicated or very similar code
* Participate in specifications conversation (with tech and non tech teamates) while keeping all the previous points in mind to influence decisions

### Be comfortable with important coding knowledge

* Common data structure and algorithms
* Common design patterns and their possible performances, maintainability or extensibility issues.

### Be autonomous

* Provide more or less accurate task time estimation
* Finish tasks in estimated time
* Manage priorities, issues or disruptions to stay on track of planing
* Be able to resolve complex, unplanned or hard to debug issues, alone.

### Inform the team if any of the above points are not fulfilled

TODO

## Coding goals

When creating code, we should always strive for it to have the following features :

* Robustness : changing something should should not break other part of the codebase
* Changeability : it should be relatively easy to introduce changes
* Transferability : it should be easy for other team members to understand, us and modify the code
* Performance : it should perform well under most circumstances
* Security : depending on the use case (mostly for application that are exposed to the internet), but we should always design code that has minimum known security vulnerabilities