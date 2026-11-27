# UCM technical evaluation brief

## Thesis
UCM separates application semantics from a particular development tool. UUI Studio is both a consumer and an authoring environment for other consumers. A partner may preserve the current Studio or create a different product on the architecture.

## Design principles
Define facts once; derive what can be derived. Separate responsibilities before organizing delivery. Reuse existing standards and platform capabilities. Keep necessary complexity when it improves the result. Optimize mechanisms rather than individual outputs. Do not sacrifice product behavior for architectural purity.

## Architecture and boundaries
UCM defines component properties, defaults, events, inheritance and composition. Shared runtime mechanisms interpret those definitions and project them into Web technologies. Native hosts provide platform integration. The current Studio still contains legacy shell, property and navigation implementations; complete self-consumption is not claimed. The frozen component-first Studio remains a historical reference, not the current product.

The source archive includes `Studio/ucm-definition.json`, `tools/build-app-runtime.mjs` and `native/studio/src/build.rs`. The linker describes itself as conservative and uses an explicit application profile. Dynamic dependencies require conservative handling; a partner should evaluate completeness and runtime behavior rather than assume optimal pruning.

## Two engineering cases
**JS:** The architect directly reviewed code and corrected an initial misunderstanding: BMI was a test case, not the optimization target. The goal was to improve the shared APP generator. The engineering recap records separation of Studio-only code, consumer-based packaging and a common Run/Build path. Acceptance includes behavior and appearance, not only package size.

**UCM:** The architect reviewed JSON semantics, not the implementation code of the parser. Codex implemented the changes. The November 25 archive records a two-file baseline of 165,711 + 14,609 bytes and a final single definition of 131,590 bytes. Reduction: 48,730 bytes (27.02%). The default-as-key enum retains the entire option list, avoiding position-dependent semantics. Inherited values retain ancestor lookup behavior. Recorded validation is not an independent audit.

## Proposed evaluation (not an existing commitment)
1. Reproduce a pinned build and document dependencies and licenses.
2. Compare generated applications across representative feature sets, including dynamic dependencies and negative tests.
3. Verify declared minimum WebView/OS targets and native host interfaces; measure startup, memory, size and interaction latency against a stated baseline.
4. Review project isolation, AI approvals, secret handling, signing and supply-chain risks.
5. Evaluate a small joint pilot and decide whether to evolve Studio or design a new consumer.

## Evidence register
- Public repository: https://github.com/felixdds/uui-studio
- Historical DOM-Core: https://github.com/felixdds/uui-dom-core
- Architect's supplied source archive: UUI-Studio-Source-Review.zip (current definition length checked; not executed for this brief).
- UUI-UCM-Architecture-Evolution-History.zip: `03-Architecture-Snapshots/snapshot-index.json`, `06-Timeline/session-provenance.json`, `05-Validation-Results/ucm.4-package-result.json` (archive inspected; recorded checks not independently rerun).
- Frozen project: ARCHITECTURE.md, DECISIONS.md, component migration documents, original definition/defaults files (historical, not current contracts).
- Origin, earlier cross-platform experience and product goals: architect's first-person account.

No claim of patent protection, market uniqueness, production readiness, independent audit or completed cloud service is made.
