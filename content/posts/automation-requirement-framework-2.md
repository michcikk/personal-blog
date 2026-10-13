---
date: "2026-10-13T09:09:44+02:00"
draft: false
title: 'Automation Requirement Framework, part 2: process deep dive'
tags: ['work', 'automation', 'framework', 'business', 'arf', 'requirements']
series: ['automation requirement framework']
disableShare: true # OR ShareButtons: ["linkedin", "github", "x"] to limit defaults
---

{{< not-ai-icon >}}

# split workflow

Hopefully you found your project priority based on [priority calculation](/content/posts/automation-requirement-framework-1.md) I covered earlier. You also might already have your own buckets and for sure you have found your type - either **task** or **process**. There is a difference in automating an action that takes 20 minutes of employee's time daily and an complex payroll process that spans across hours or even days. Tasks would usually fall into category of (standard) operating procedures (SOPs) and usually end up as a straightforward translation of person's actions to automation's actions. Processes, on the other hand, are complex, usually cross-team, efforts that include multiple SOPs representing sequence of steps that are interconnected by the final goal. 

Understanding your types is really important at this stage as next steps are taken based on it. Apart from complexity-based split, there's separate flow for **one-time** kind of automation. Those are usually time-bound, scope-limited and require specific type of requirements to begin work on them. One-time are usually migrations, backups or data removal. This type also affects a [priority calculation](/content/posts/automation-requirement-framework-1.md) as deadline is a big factor to take into account.

On each type we do have separate discovery flow - global, local and fast.

## per-type discovery flow

 ``` mermaid
%%{ init : { "theme" : "default", "flowchart" : { "curve" : "linear" }}}%%

flowchart TD
    
    local@{ shape: "h-cyl", label: "📍*TASK*"}
    global@{ shape: "h-cyl", label: "🪐*PROCESS*" }
    fast@{ shape: "h-cyl", label: "⚡*ONE-TIME*" }

    refine[["refinement (<i>streamline</i>, <i>improve</i>, <i>adjust</i>)"]]
    scope@{ shape: "folder", label: "scoping (<i>extend</i>, <i>limit</i>, <i>include other areas</i>)"}
    decide@{ shape: diam, label: "decision" }
    technical[["technical refinement & architecture design"]]
    localForm@{ shape: "card", label: "***SCOPED*** questionnaire" }
    globalForm@{ shape: "card", label: "***FULL*** questionnaire"}
    development@{ shape: "console", label: "development" }
    onlyImprovement@{ shape: "doc", label: "document new process" }
    otherSolution["different solution (or technology)"]

    local ---> localForm
    localForm ---> technical
    technical ---> development

    fast --> localForm

    global ---> globalForm
    globalForm ---> refine
    refine ---> scope
    scope ---> decide
    decide --> |<b>automation</b>| localForm
    decide ---> |<b>only process improvement</b>| onlyImprovement
    decide ---> |<b>other</b>| otherSolution 


 ```



# next steps

## task & one-time

Both ***task*** automation and ***one-time*** ideas go through simplified, scoped questionnaire designed to ask only what's important for any of those above. After that we do technical refinement and move to development. At any stages we get artifact that we can always compare to what was agreed upon at the beginning - task detailed description after questionnaire and architecture decision record (ADR).

## process

For ***process*** discovery we get longer action tree. Form itself is longer with more open questions (incl. deal-breakers, something that can completely stop automation or improvement at the early stages). We demand SOPs (if there isn't one, we ask to create) in a form of a document (video will not do :().

If possible, try to use COPIS (or SIPOC) to understand all involved parties (customer of a customer, provider of a provider and more) with all relation & action mapping. This also allows us to understand the process in the broader scope of an organization and how well its working between different areas.

We need metrics, SLAs and any other data available to make informed decision how to improve (and/or automate) the thing. 

### redefine

Having all that information gather, then and only then we can start working on any improvements. We work on fixing the process  but we can also look at what can we do within organization - can this solution be extended to additional places? Maybe only some part of it should be redesigned? Yeah, such questions can only be answered after great research on what's already on the shelf.

# coming next

In next entries we will be looking into what are the actual questionnaires and which questions are the most important ones!