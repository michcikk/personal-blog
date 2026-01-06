---
date: "2026-01-06T17:09:44+02:00"
draft: false
title: 'What is RPA?'
tags: ['work', 'automation', 'business', 'rpa', 'macro', 'excel', 'uipath', 'microsoft']
disableShare: true # OR ShareButtons: ["linkedin", "github", "x"] to limit defaults
---

## historical background

I work in a field that is on the verge of IT and Business - **robotic process automation** which is fancy (and now standardized) name for a business automation. When such teams were being introduced to organizations about 10 years ago, the RPA software was still immature and many automations were done using battle-tested Office (mostly Excel, Access) macros. It had its disadvantages but allowed for fast development. Currently Microsoft is slowly killing it (due to security risks) and replacing with much safer (and web-enabled) Office Scripts. Main disadvantages for the macros is that environment it is being ran on might be different than development environment - your US colleague's PC has different settings (decimal separator, encoding, etc.) than your Polish-set machine. RPA software was designed to fix it with 'robots' that run on a VM. Robot could've done same thing as macro but now RPA team was able to control the environment parameters.

Robots have all the advantages of macros (fast development time with integrated IDE, fast deployment, identity access management...) and they did not inherit any of the bad stuff. RPA was introduced as no-code tool, evolved in media into low-code tool recently but IMO it was always more code rather than less. Even with code-blocks structures, you need to know how to program to use it to its full potential. I'd argue it's **mid-code, low-maintenance**.

## goal

Purpose of a robot(s) is to take over a well-explored, rule-based and repetitive process or single task from a person who can then move to responsibilities better fit for human brain. It's not *replace-to-fire*, it's *replace-to-shift*. People are better utilized than copying data from one system to the other or writing hundreds of e-mails with minuscule changes. For RPA to work best is to have good foundation (well-defined & documented process) with clear expectations of what's possible.

## vendors

There are many vendors providing RPA services with 2 biggest and most feature-complete ones currently being [UiPath](https://www.uipath.com/) and [Microsoft](https://www.microsoft.com/pl-pl/power-platform/products/power-automate). Former has purpose built platfrom with Orchestration services and recently web-based BPMN tool for integrating robots, AI agents with human-in-the-loop scenarios. Latter has its Power Platform, Power Automate and specifically Power Automate Desktop which was built on solution from [aquired Softomotive team](https://www.microsoft.com/en-us/power-platform/blog/power-automate/microsoft-acquires-softomotive-to-expand-low-code-robotic-process-automation-capabilities-in-microsoft-power-automate-2/). 

> What's really intresting is that Softomotive was working on an open-sourced RPA language called Robin which currently powers Power Automation Desktop expressions. Project was in version 0.9 and code was supposed be available on Github with 1.0. Unfortunately due to aquisition it never happened. There are still traces of Robin scattered around web ([1](https://www.nandan.info/open-source-rpa-language-robin/), [2](https://www.nandan.info/open-source-rpa-language-robin/), [3](https://www.reddit.com/r/rpa/comments/d9jb8u/open_source_robin_a_disruptor_in_the_rpa_industry/)).

There are once big, now in decline vendors like [Automation Anywhere](https://www.automationanywhere.com/) or [BluePrism](https://www.blueprism.com/). Also many more smaller (or not corporate-sized) solutions from other companies like [G1ANT](https://g1ant.com/) or [Sema4AI](https://sema4.ai/).

> Another sad story regarding aquisition - Sema4AI bought RoboCorp which had already developed and open-sourced Python-based RPA solution. It was based on Robot Framework for automated test in Python but RoboCorp team also delivered many Python RPA libraries beside what mentioned framework offered. There was code-blocks IDE built in VSCode and code translation service from UiPath .xaml files. All of it now gone but hapilly all the [code is still available on Github](https://github.com/robocorp/robocorp) and [RoboCorp website is still alive](https://robocorp.com/portal) even if only as documentation portal.

I have not heard about any in-company purpose-built RPA platforms so if there are any in your companies, please [let me know](/content/contact.md).

## RPA & AI

As briefly mentioned above, currently most (if not all) vendors are trying to integrate AI Agents into their platforms. My humble opinion is that it might undermine the reason all such platforms were built. They are not only process-automation but also process-mining and process-storage platforms. It allows for research on organizational excellence and efficiency. Overview of all processes, their interactions, teams involved and most importantly improvements' discovery. Single RPA idea can scale from a one user to multiple departments and tracking that is realtively easy thanks to those platforms. If AI Agents are introduced without any proper preparations, just as personal assistants it might wreak havoc. We would loose all RPA benefits - visibility (person using it however they see fit for whatever processes they want, maybe even for personal tasks), repairability and modifiability (all changes in vendor's hands, we cannot even re-train such agant). It would be Excel macros all over again but without control over behavior (robot and macros are at least limited by code).

Perfect implementation of AI Agents would be to give them one specific task at the time, preferable those which robots cannot do (decision making, taking action based on irregular input or OCR & understanding) and scale with capabilities. Currently I must admit UiPath approach makes most sense as it does just this. Additionally it's really easy to use and build such AI-enabled automations.

## story unfolds

There is a lot to write about RPA - how to work with requirements (look into [arf series](https://michcio.xyz/series/automation-requirement-framework/)]), best workflows & approaches, its relation with classical software coding and many more. I have some hot takes on that and they will pop here in the future. See you around!