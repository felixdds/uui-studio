# Why a Dentist Wanted to Build a Cross-Platform Development Tool

[简体中文](../01-origin.md) · English

I am a dentist, not a professional programmer. I used Delphi 7 and liked its visual development experience, but I have no formal software engineering training, and I do not know Rust. The idea for UUI Studio stayed with me for years before I had a way to implement it.

## A question that stayed with me since 2014

In 2014, developments in HTML5 gave me an idea: applications on different operating systems share so many UI concepts. Why keep implementing them separately? Could buttons, input fields, panels, menus, layouts, events, and data presentation have a common description, leaving genuine platform differences to the underlying system?

I wanted a tool with something of Delphi's visual development experience that could also support cross-platform applications. I could not implement it then. The idea stayed with me for twelve years.

In 2026, I first tried asking Codex to handle some automation work, including generating videos from text and publishing them to YouTube. That made me revisit the old idea: could AI help me actually build that cross-platform UI system? That was how we began UUI Studio.

## What I brought was a habit of questioning

Over many years in dental practice, I have developed a habit of asking: why must this be done this way? Which steps are actually necessary? Is there a way to reduce unnecessary burdens on the person receiving treatment?

Safety, clinical outcomes, patient experience, and patient satisfaction are what I care about. Speed may improve as the method improves, but it is a byproduct. When complexity is necessary, it should remain. When an intervention is unnecessary, habit alone is not a reason to retain it.

I brought that habit into software development. In the clinic, I care about the person receiving treatment. In UUI Studio, I care about the developer using the tool and the people who will use the resulting application.

So I might ask Codex to remove an unnecessary component, or ask it to add code so that a user can avoid one more click. I often joke: "To save the user a click, I'd happily have Codex write ten more lines of code. I'm not the one writing them, after all. Ha!"

Those requests point in different directions, but the criterion is the same: are the results and the experience better? Simplicity and complexity are both means to an end.

## An idea I could finally put to the test

I handle requirements, architectural rules, direction, and judgments about the actual user experience. Codex handles implementation code, compilation, debugging, and technical checks. I did not personally write the implementation code for this project, but I do need to judge whether it addresses the problem I want to solve.

Often, I start with a simple question: "Can this be done?" Then come attempts, checks, revisions, and sometimes starting over. UDM and UUI Studio gradually took shape through that process.

Twelve years ago, I had an idea. Now I can look at an actual piece of software and keep asking: "Why couldn't this be a little better?"

---

[Series index](README.md) · [Product homepage](../../README.en.md) · [Next](02-between-patients.md)
