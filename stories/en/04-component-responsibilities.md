# Why Splitter Is a Property of Panel

[简体中文](../04-component-responsibilities.md) · English

When Codex first implemented Splitter, it made it a separate component. That is a common approach, but I asked: if Splitter is there to resize a Panel, why can't it simply be a property of that Panel?

## Docking already tells us the direction

When a Panel is docked on the left, its resizing edge is on the right. When docked on the right, the resizing edge is on the left. The same relationship applies at the top and bottom. If the direction can be derived from Dock, why define it separately?

Splitter therefore became a boolean property of a docked Panel: `true` enables resizing, and `false` disables it. It no longer needs to exist as a separate component, and there is no separate direction enum to store.

Dragging the Splitter at runtime changes the Panel's size. Double-clicking restores the design-time size explicitly saved by the designer in the Form.

What satisfies me is not simply having one fewer component. The user has one fewer relationship to maintain. If existing rules can express something, there is no need to ask the user to configure it again.

## Storage need not know every component

Later, we needed components to remember runtime state. A Form might remember its window size, and a Panel might remember a layout adjusted by the user.

But I did not want Storage Service to understand the internal logic of every component. Otherwise, adding a component could mean going back and modifying the storage service too.

My requirement was that components decide what to save, how to interpret that state, and how to restore it. Storage Service should only provide general data storage and retrieval. Components and services should each have the responsibilities that belong to them.

An explicitly saved design-time size should also remain conceptually distinct from a user's runtime adjustments. One expresses a designer's decision; the other expresses a preference arising during use.

## Sometimes I ask for more code

This does not mean I always ask Codex to write less code. For example, when browsing to a directory containing `project.uui`, I want Studio to recognize the project itself. When a property input first receives focus, I want to be able to enter a new value directly. When a spacing editor can derive the remaining values, it should still preserve those the user explicitly set.

Those interactions may require more implementation work. If they reduce unnecessary actions, they are worth considering. Simplifying Splitter and adding interaction details follow the same criterion: make the tool easier to understand and the work easier to do.

---

[Series index](README.md) · [Product homepage](../../README.en.md) · [Previous](03-inline-properties.md) · [Next](05-studio-first-consumer.md)
