---
date: "2026-02-15T12:09:44+02:00"
draft: false
title: 'Automation Requirement Framework, part 1: introduction'
tags: ['work', 'automation', 'framework', 'business', 'arf', 'requirements', 'software development']
series: ['automation requirement framework']
disableShare: true # OR ShareButtons: ["linkedin", "github", "x"] to limit defaults
---

{{< not-ai-icon >}}

## what do you need this for?

I have started working on this due to constantly hearing of or experiencing myself this trival thing called <i>changing requirements</i>. All development today is created using Agile principles of course, although that doesn't mean we shouldn't have strong foundation to later <b>improve</b> on it. Yes, improve - not change. I think as analysts / designers / developers we should be as thorough as possible when it comes to first sketch of a solution, after all how do you write your stories / tasks / features if anything is missing. At the same time, software development is a bit different than (process) automation development. You need mapped end-to-end process to even start thinking about designing solution - making shortcuts, simpifying, integrating with existing solutions or even researching accesses required. Automating is more of a <i>waterfall</i> project with some flexibility when it comes to extending or improving on the way. Reducing the risk of any changes during the development makes projects being delivered faster and coders a lot happier.

Idea behind creating such framework is not only for asking the right questions resulting in a well laid out documentation. It's also about a priority scoring. As an automation team you get many stakeholders with various needs and they all seem very urgent from the point of a requestor. To be able to respond to any accusations or blaming you should be able to rely on data. This framework also takes that into consideration - project priority is expressed as a number calculated from multiple factors (nr of people impacted, deadline presence, saving, benefit type, etc.). This allows for objective and automated scoring of ideas and putting them at the right place in the backlog.

## immediate benefits

 -  no operational changes during development

> this framework can be implemented in many ways and many elements can be adjusted or removed, having in mind that the most important value coming from this is faster delivery time and happier coders; agile ways still apply but for iterating on cosmetic changes, not design

 -  data-based priority establishment

> this benefit is fastest to notice as it's there as soon as first automation project starts being worked on using this framework

 -  project grouping

> this framework introduces multiple types of buckets that project can fit into - based on simplicity, scopes or systems involved which allows for reliable effort estimation

 -  crucial questions answered

> all most important queries gets addressed at the first steps - and they are not, you know there is something to follow-up on and you will not forget about it

## workflow

Framework is automated (procedural) and focuses on idea that is already shared between stakeholder and your automation team. This is not a guide on how to search new automation ideas in an organization (such effort would be futile as however similar, all organizations are different). Starting point is an idea already registered in your team's "database" - through Jira ticket, Automation Hub workflow, verbal understanding or any other approach your team mind find fit.

<b>1. Idea assessed as technically feasible (might be in a form of hackathon, architect's opinion or any technical team member's investigation)</b>
<b>2. Calculate project priority</b>

This step is an automated form with multiple fields:
 - <u>complexity</u> - (high-level) nr of steps
 > steps should be as broad as possible - if automation is supposed to log-in to a system, download file, modify data and distribute the results it would just result in three actions: download -> modify -> distribute (obviously login is required for a successful download). Diving into details might affect negatively our efforts standardize this step; what can help assesing this is creating your team's dictionary of actions (exactly like example above: <i>download a file</i>, <i>distribute results</i>, etc.)
 - <u>saving</u> (in a simple, standardized units i.e. hrs/month)
 - <u>impact</u> (nr of users affected positively)
 > how many people will stop doing repeatable, mundane task and will result in freed capacity
 - <u>idea introduction date</u> (to calculate rolling priority)
 > how many days pasted since idea was discovered should affect priority
 - <u>benefit category</u> 
 > in this framework there are three (listed by descending importance) - <b>capacity release</b> (actually saving FTEs by taking over their tasks), <b>cost avoidance</b> (actively dodging uneccessary money spending, i.e. buying specific software) and <b>compliance</b> (reducing nr of errors in a process, moving to appropriate data format, etc.); these categories' calculation weights affects final priority calculation
 - <u>is it one-time automation?</u> (i.e. migration of data, system clean-up)
   - if <i>yes</i> - <u>what is the deadline</u>
   > the closer we get to the deadline the higher is priority value
- <u>organizational details</u>
> this should allow for finding requestors / responsible people even if there are personal or company changes and makes structurized project convention naming and storage; I propose only two: <b>main area</b> (People / HR services, Financial Services, Accounting, etc.) and <b>sub area</b> (specific team inside an area - i.e. Procure-To-Pay in Finance). This can be freely adjusted however you see fit for your organization

<b>Priority equation</b>:


<b>3. Bucket placement (optional)</b>
> there are many approaches to do that - my idea is to group by <b>complexity & saving</b> as that makes the most sense (initial effort and expected results mapping); other approaches could rely on completely different set of data, even not included earlier, like <b>nr of teams / people involved in this process & saving</b>. You can arbitrary choose what data you want to map in your buckets and name them accordingly. Buckets are fully optional but for this specific framework splitting complexity by under and over 10 steps allows us to predict if a task will require complete solution design or rather automation will replace existing procedure (more or less) 1-to-1.

<br>

|   | < 40 hrs/month  | 40-60 hrs/month  | > 160 hrs/month  |
|:---|:---:|:---:|:---:|
| <b>task (< 10 steps)</b>  | pocket change  | sure bet  | quick win  |
| <b>process (> 10 steps)</b>  | back burner  | possible ht  | crawling victory  |

<br>

### template

All data can be found in a sheet called "1. Initial questions" in <a href="/downloads/test.txt" download>testing</a>. Next steps will be covered in next entry in a series.