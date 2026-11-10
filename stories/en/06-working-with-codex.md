# Codex Writes the Code; I Keep the Architecture on Track

[简体中文](../06-working-with-codex.md) · English

Codex can often implement a feature quickly, but its approach may not fit UUI Studio's architecture. A result that appears to work may still need to be redone.

## Getting it onto the screen is not enough

Sometimes Codex bypassed UDM and used direct DOM manipulation to satisfy a UI requirement. The result looked right, but that path did not follow the unified model. I asked for it to be reimplemented.

We went through several rounds of restructuring: gradually moving useful parts into a new structure, then deleting what was no longer needed. I found that AI readily adds code and follows familiar technical habits, but does not necessarily volunteer to remove existing code.

Over time, I asked it to understand the project and component definitions before making changes, and explain the scope and verification method. I do not believe a long-running conversation alone can permanently ensure that AI understands the architecture. Rules need to live in the model, documentation, process, and checks.

## An application task and ongoing architectural work

Asking AI to make a small application from a few clear requirements is a useful way to develop software. Such work may also require careful judgment and repeated revision. I do not dismiss its value.

In leading UUI Studio, my work also includes decisions spanning the underlying application model, components, editor, and runtime: which mechanisms should be shared, which states must stay separate, which values can be derived, and which explicit user settings must be preserved. With each new feature, I must judge whether it still follows those rules.

For example, a property displaying `inherited` and the question of whether the user explicitly set it are two different matters. Whether Splitter can be a Panel property concerns component responsibilities. Whether Storage must know every component concerns the boundary of a general service. These are more than requirements to "make this feature work." They affect how later features can be added and how existing ones remain consistent.

Studio's own use of UDM keeps putting these decisions to the test in practice. The work does not end with one example: we keep developing the tool with the same model, then correct what does not make sense. Sometimes a feature already runs, but I still ask for it to be redone because the implementation has not respected the architecture.

The distinction I want readers to understand is the difference in responsibilities between completing a particular application task and maintaining a platform's rules over time. Both can use AI. Expressing requirements, making architectural trade-offs, checking results, and correcting course do not automatically take care of themselves.

Codex generates the code; I remain involved in goals, architecture, and judgments about user experience. That is our division of work, each contributing our strengths. Other people using AI does not diminish their work. My using AI for this project does not require me to discount my own contribution either.

## Two different kinds of AI collaboration

Codex helping me develop UUI Studio and AI Workspace inside UUI Studio are two different things.

The former is my collaborator in building the tool. The latter is the working environment I want to provide to application developers: AI reads the current project and component contracts, proposes a plan, implements it after user approval, then builds, runs, and checks the application.

Something Codex accomplished during development must not automatically be treated as a capability already available in the product's AI Workspace.

## Approval is an extra action with a purpose

An AI's ability to generate code does not give it permission to change a project without the user's approval. I required a clear approval mechanism in AI Workspace.

Initially, the approval mode was placed in Connection settings. I realized the existing SplitButton could serve the interaction: the main button approves and executes, while the menu lets users choose approval by task or by implementation stage.

This adds a control step, but lets users decide more clearly what AI should do. Fewer clicks are only one possible benefit; user control matters too. This account describes the evolution of the feature. For the capabilities of a particular public test package, consult its release notes.

## A black box that preserves the order of events

I also want AI to see enough runtime information rather than guess from a report that simply says something is wrong.

Studio's black-box mechanism retains operations and events from recent runtime sessions, including their order, targets, parameters, and necessary state. Related objects can be expanded when needed. I particularly care about causal order: deleting details too early may remove the evidence needed to identify the source of a problem.

Its first purpose is debugging, not just displaying attractive logs. A completion report should not stop at "the code is written." It should include feedback from actual building, running, and checking.

## When one approach stalls, try another

During development, we encountered window positioning and animation problems. Things worked on macOS, while a suitable solution on Windows remained elusive. I eventually had two Codex instances, one on Mac and one on Windows, exchange information and analyze the problem together. The problem was resolved.

I have also considered having AI on different platforms test separately and send findings to the main project. Code changes still need to be coordinated so conflicting edits do not happen at the same time. These ideas can be developed gradually; they do not all need to be implemented at once.

---

[Series index](README.md) · [Product homepage](../../README.en.md) · [Previous](05-studio-first-consumer.md) · [Next](07-apps-and-platforms.md)
