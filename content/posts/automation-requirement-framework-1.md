---
date: "2026-01-04T12:09:44+02:00"
draft: true
title: 'Automation Requirement Framework, part 1: introduction'
tags: ['work', 'automation', 'framework', 'business', 'arf', 'requirements']
series: ['automation requirement framework']
disableShare: true # OR ShareButtons: ["linkedin", "github", "x"] to limit defaults
---

outline:
1. why did i started working on this framework
2. why i think it is beneficial
3. what is the process (including backlog priority & then development priority)
4. task/process differentiation (nr of steps vs. nr of people (teams?) involved vs. 

--
Now, that we live in AI age, anything can be easily build. Claude Code (or other CLI tools), prompt and you might have a working software within minutes. Obviously focus shifted from '**what** and **how** should we build?' TO **when**. Now, that we can create anything quickly, prioritization will play even bigger role than before.

I believe in data driven decision making. There should be an environment present that allows team to determine any variable significance at will. That's what my team struggled with and the reason I wanted to create a simple procedure that would allow any person (anylyst role or not) to find the real value of a project at a given step. I envisioned it as an automated system that takes proposal data as an input and returns priority value as an output. I know what you think - it's just simple equasion  - and you would be right. However the full framework is a bit bigger than this.

## Short history lesson

I work in a field that is on the verge of IT and Business - robotic process automation which is fancy (and standardized) name for a business automation. When such teams were being introduced to organizations about 10 years ago, they RPA software was still very immature and many automations were done using battle-tested Excel macros. It had its disadvantages but allowed for fast development. Currently Microsoft is slowly killing it (due to security risks) and replacing with much safer Office Scripts. Main disadvantages for the macros is that environment it is being ran on might be different than development environment - your US colleague PC has different settings than your Polish machine. RPA software was designed to fix it with 'robots' that run on a VM. Robot could've done same thing as macro but you as a developer (or RPA team) was able to control the environment parameters.

 Single idea in RPA can scale from a single user to multiple departments. Initial tool in our repository were Excel macros. They are hapilly long gone as our delivery tool due to my decision few years ago (but still present in organization unfortunately). We moved fully to RPA software and Python automations.