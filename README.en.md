# UUI Studio

[简体中文](README.md) · English

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/brand/uui-studio-horizontal-dark.png">
  <img alt="UUI Studio" src="assets/brand/uui-studio-horizontal-light.png" width="760">
</picture>

UUI Studio is a visual application development tool built for human–AI collaboration. Developers can edit layouts, properties, and events in the designer. AI can work on the same project within the user’s approved scope. The project and business scripts remain editable after the app is built.

## Strategic collaboration · UCM Partnership

UCM is a standards-first application architecture with a working prototype. We welcome technology partners to evaluate and develop it further.

**[Partnership invitation](PARTNERSHIP.md) · [Technical brief](docs/partnership/Technical_Brief.md) · [Presentation PDF](docs/partnership/UCM_Strategic_Presentation.pdf)**

## UCM architecture file

Studio uses one authored UCM JSON file for component definitions, events, rules, defaults, and creation values. Application and platform defaults sit alongside their rules. Studio and the build tools share the expansion step, and the app builder selects the runtime data and resources each project needs.

Ordinary enums list their options directly. A fixed default is the key of the ordered option list. For inherited font settings, the shared Select editor displays the effective ancestor value.

[View ucm-definition.json](architecture/ucm/ucm-definition.json)

## 0.2.0-alpha.1

This prerelease completes the underlying architecture migration and preserves the existing design and AI workflows. Projects use JSON-based UCM, and the builder selects the runtime component code and resources each project uses. Building the same project for Windows and Android has been demonstrated during development. This release is intended for technical evaluation and early testing.

[Windows installer](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.4/UUI-Studio-0.2.0-alpha.1-Windows-Setup.exe) · [Portable ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.4/UUI-Studio-0.2.0-alpha.1-Windows.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.4/SHA256SUMS.txt) · [Release notes](https://github.com/felixdds/uui-studio/releases/tag/v0.2.0-alpha.1.ucm.4)

The installer is self-contained. If Windows reports an unknown publisher, verify the source and SHA-256 checksum. Extract the entire portable ZIP into a fresh folder. Both packages include English and Simplified Chinese offline Help and editable examples. AI features require your own provider configuration and API key.

## Looking for a team to take over development

I’m a dentist and the founder, architecture designer, and project lead of UUI Studio. The project grew out of a question I’ve returned to for years: how can we reduce repetitive cross-platform UI work and keep the same application editable by both its users and professional developers?

I’m looking for a company or professional team willing to take over ongoing development. I would like to remain the project lead and architecture designer, working with the team to set priorities, review key design decisions, and guide delivery. The team would lead implementation, systematic testing, cross-platform validation, and release maintenance to turn a working prototype into a dependable product.

A practical first step would be to choose a small business scenario and evaluate project maintainability, the AI approval workflow, and cross-platform builds together. If that goes well, we can discuss long-term collaboration and handover. Please use [GitHub Issues](https://github.com/felixdds/uui-studio/issues) to start a technical conversation.

[Project stories](stories/en/README.md) · [Downloads and demo](docs/en/downloads.md) · [Historical demo](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1) · [0.1 historical release](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261111-motion-android.1)

This repository provides public information, test distributions, and a place for technical discussion. Studio’s full source code is not published here. Use and distribution are governed by the bundled terms and permission from the rights holder.
