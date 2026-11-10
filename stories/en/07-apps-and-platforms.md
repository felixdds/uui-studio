# To Make a BMI Calculator, I Built a Development Platform First

[简体中文](../07-apps-and-platforms.md) · English

I often joke: "To make a BMI calculator, I first built a cross-platform application development platform."

BMI Calculator and MyBible are applications I built with UUI Studio. To me, they are more than demonstration material. They are opportunities to find out where the platform is awkward to use.

## Applications bring problems back to the platform

The BMI calculator gave the interface and interactions a concrete task. MyBible introduced needs involving SQLite data, content navigation, search, and resource packaging. Building actual applications lets me see how UDM behaves in use.

But one person's needs and time are limited. A few applications of my own cannot cover every scenario a development platform might encounter. That is one reason I hope to find collaborators and bring in more real projects.

## From Python experiments to Rust

Parts of UUI Studio were initially implemented in Python. Later, I considered moving to Rust to improve distribution and the project's engineering structure.

I do not know Rust, so I first asked Codex to run small experiments, then gradually expanded the migration. One major migration took over two hours, after which the software was rebuilt and ran successfully.

Previously, doing this in an unfamiliar language would often require substantial learning first. Now I can state the architectural objective, let AI handle implementation, and judge the actual results.

Rust is an implementation tool here. My ultimate concern is whether it suits the problems the system needs to solve.

## The goal at that stage was cross-platform compilation

We successfully compiled on Windows, Android, Linux, macOS, and iOS. Moving between platforms did not present obstacles we could not overcome, and we then returned to Windows to continue development.

At that stage, I needed to establish that this codebase could compile across platforms. I was not requiring full acceptance testing of all features and devices on each platform then.

Those historical compilation experiences must be distinguished from the checks completed for a currently published version on a particular platform. Successful compilation, successful startup, functional checks, and long-term stability should not be combined into one conclusion. For the scope of current public test packages, see the repository's [validation notes](../../README.en.md#current-validation-scope).

## Continuing to improve what is already there

With that initial evidence for the cross-platform direction, I put my attention back into everyday development on Windows, improving common components, rules, and user experience.

A platform need not continually prove its value by adding features. Making existing capabilities more consistent, reliable, and usable is real progress too.

---

[Series index](README.md) · [Product homepage](../../README.en.md) · [Previous](06-working-with-codex.md) · [Next](08-future.md)
