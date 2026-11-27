# UCM — One architecture. Many consumers.

**A standards-first application architecture with a working visual development prototype.**

UUI Studio is a Delphi-inspired, AI-assisted desktop development environment and a reference implementation of UCM. The architecture is not limited to Studio: future development tools and applications can consume the same component model.

## Why this project exists

The idea originated in the architect's experience with Delphi and the emergence of HTML5. Mature platform WebViews and AI-assisted engineering now make it practical to explore a complete visual development workflow without building or bundling a separate rendering engine.

## Architecture

- Declarative component definitions, defaults, inheritance, composition and events.
- Shared HTML/CSS/JavaScript runtime mechanisms and native host integration.
- A disciplined subset of Web standards, with necessary expressive capabilities preserved.
- Dependency-aware application builds, rather than shipping the entire development environment.
- Human-led design and reviewable AI-assisted project changes.

## Evidence and status

The prototype demonstrates the basic approach. In a documented November 2026 optimization session, the definition/defaults baseline went from 180,320 to 131,590 bytes (27.02% reduction). This is a source-definition measurement, not a runtime performance benchmark. The engineering history also records a shift from optimizing an individual BMI example to optimizing the shared application builder.

Earlier Studio versions were run on Windows, macOS and Linux according to the architect's development experience. Android 10 and iOS 17 are minimum application targets; current full-matrix certification is not claimed. Studio is designed for desktop use. Cloud build is a proposed future capability. Independent security, performance and large-scale application evaluation remain open.

## Collaboration invitation

I am interested in working with a technology company or research-oriented engineering team to evaluate and develop this architecture further. My intended role is continuing architectural and product-design leadership, alongside a professional engineering team. The current Studio is a starting point, not a constraint on the design of a future product.

A useful first step would be a technical walkthrough, followed by a jointly scoped evaluation of the component model, runtime and application builder.

[Project repository](https://github.com/felixdds/uui-studio) · [Architect's GitHub profile](https://github.com/felixdds)

See the accompanying strategic presentation for the architecture, engineering cases and proposed collaboration.
