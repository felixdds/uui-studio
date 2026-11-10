# The Development Tool Should Follow Its Own Rules

[简体中文](../05-studio-first-consumer.md) · English

I do not want Studio to be a special case above UDM. Its own main interface should use the same components and layout rules.

## The first consumer

Studio uses Panel, Button, SplitButton, themes, languages, and layout mechanisms under the same model as applications built by users. As we develop Studio, we are also continuously using and testing UDM.

If a component or rule is awkward in a real development tool's interface, Studio may encounter the problem first. When we fix it, I want the improvement to go into the shared mechanism so that applications can benefit too.

I do not want two disconnected systems: one just to make Studio work, and another to hand to users. A development tool should follow its own application model first.

## Studio is itself an application that keeps using the model

To me, Studio is more than a tool for editing applications. It is itself a complex application that continuously uses UDM. Panel layout, property editing, and theme switching must work in everyday development, not merely look right in a demonstration.

That makes Studio an important way to test the architecture. If completing its interface keeps requiring us to bypass UDM and write special logic, I need to ask: is a necessary capability missing from the model, or has the implementation failed to follow the existing rules? I want us to improve the common mechanisms rather than give the tool shortcuts unavailable to user applications.

At the same time, Studio's needs cannot cover every application. The existing ten editable examples provide other scenarios, and we can add more when needed. But moving from ten examples to a hundred does not by itself establish architectural maturity. What matters more is whether they cover different data, layouts, interactions, and platform conditions, expose problems, and test whether the same rules still hold.

## Shared mechanisms, independent state

Following the same mechanisms does not mean sharing the same state.

Studio and an application can choose different themes and use different languages. Studio may have an English interface while the application has a Chinese one. AI Workspace inside an English-language Studio can also accept Chinese instructions, work with Chinese content, and respond in Chinese.

The application's runtime environment is kept separate from Studio. That independence allows the editing tool and the application being edited to work in their own contexts. This is a discussion of runtime and state boundaries, not a claim that all security isolation has been fully verified.

## Translations need to know when the source changes

The language system tracks changes using hashes of the English source text. This helps identify translations that need updating and entries whose source text has been deleted while a translation remains.

The capabilities were already there, but I thought the list could be easier to understand. I asked for entries to be grouped into three categories:

- Entries whose source text has been deleted, which can be cleaned up.
- Entries needing an update after the source changes.
- Updated entries, which can still be edited further.

During implementation and checking, Codex also found that old translations could re-enter the system from distribution resources, and continued fixing that problem. We did not add a new component. We made an existing mechanism more coherent.

To me, this connects directly to Studio using UDM first: find problems through actual use, then put the improvements where they belong.

---

[Series index](README.md) · [Product homepage (Chinese)](../../README.md) · [Previous](04-component-responsibilities.md) · [Next](06-working-with-codex.md)
