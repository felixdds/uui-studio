# The Stories Behind UUI Studio

[简体中文](../README.md) · English

I am a dentist, and the person behind UUI Studio's concept and architecture. I handle requirements, architectural rules, direction, and judgments about the actual user experience. Codex generates the implementation code. These articles describe where the idea came from, specific design choices, and how we kept trying and improving.

> If AI can handle something, I try to let it. We each do what we do best, without dismissing others or discounting my own contribution.

Read in order or start with a question that interests you. These are accounts of development and design decisions. For the capabilities and validation scope of the current public test packages, consult the [product homepage](../../README.md), [release notes](../../RELEASE_NOTES.md), and [testing guide](../../测试指南.md), currently in Chinese.

## Suggested reading order

1. [Why a Dentist Wanted to Build a Cross-Platform Development Tool](01-origin.md)

    From an idea in 2014 to working with AI, and a habit of asking why.

2. [Five Months of Development in the Gaps](02-between-patients.md)

    How work between patients and remote conversations on a phone added up to a project.

3. [The Little Cross Beside a Property](03-inline-properties.md)

    Why two properties displaying inherited can mean different things, and how UDM preserves explicit intent.

4. [Why Splitter Is a Property of Panel](04-component-responsibilities.md)

    From resizing a panel to persisting runtime state, deciding what components and services should each own.

5. [The Development Tool Should Follow Its Own Rules](05-studio-first-consumer.md)

    Studio uses UDM first, while applications keep their own language, theme, and runtime state.

6. [Codex Writes the Code; I Keep the Architecture on Track](06-working-with-codex.md)

    From bypassing UDM to approvals and black-box logs, turning design principles into engineering constraints.

7. [To Make a BMI Calculator, I Built a Development Platform First](07-apps-and-platforms.md)

    What BMI and MyBible revealed, along with the Rust migration and compilation on five platforms.

8. [Where I Hope This Project Goes Next](08-future.md)

    Respecting professional habits, finding collaborators, and continuing architectural work into retirement.

## A software developer's perspective

[A Software Developer's Perspective](../../docs/en/review.md) is separate from the first-person stories. It discusses consistency, engineering boundaries, and questions for further assessment. It is analytical commentary, not an outside expert's endorsement or an independent audit.

[Product homepage (Chinese)](../../README.md)
