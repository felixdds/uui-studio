# UUI Studio Windows Preview Release Notes

[简体中文](RELEASE_NOTES.md) · English

Version: 0.1.0. Build: 2026-11-10-locale-approval.1. Status: preview test version, localization and approval revision 1.

[View this release](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

[Installer (recommended)](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [Portable ZIP (optional)](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [Demo video in Chinese](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-AI-Cafe-Demo-zh-CN.mp4) · [Checksums](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/SHA256SUMS.txt)

## Choose a download

The recommended standalone installer is `UUI-Studio-0.1.0-Windows-Rust-Setup.exe`, 57,289,602 bytes (54.64 MiB). The optional portable package is `UUI-Studio-0.1.0-Windows-Rust.zip`, 88,405,074 bytes (84.31 MiB). Choose either; the installer does not require the ZIP. Filenames remain the same, so distinguish builds by their identifier and SHA-256.

## Updates in this release

- The language editor groups entries as removed from source, needs updating, and updated. Empty groups are hidden, and counts follow the current filter. Saving recomputes the group; completed target translations remain editable.
- Cleanup confirms all identified removed entries for the language, not just search results. It fixes old bundled translations reappearing during merging. A source entry added back under the same key can appear again; active translations are preserved.
- Approval uses a SplitButton: the main button approves and the menu selects task or implementation-stage approval. Existing projects default to task approval. Under stage approval, the initial approval covers the overall plan and first stage; subsequent stages pause for approval. Ordinary repairs within the currently approved scope can continue.
- Approval is tied to the plan, scope, input version, and a single-use native grant. Scope violations and version changes prevent reuse. Native records appear in the existing message area. Log write failure or capacity limits stop new authorization; chat history does not authorize operations. No shell, file-deletion, or dependency-installation tools have been added.
- A plus button before the input currently attaches images. Conversation-list titles use two lines with ellipsis and a full-title tooltip. Chinese and English built-in help describe these interactions.

## Installation and upgrades

Close Studio and related applications, and back up your projects and data. Follow the setup wizard for the installer. Fully extract the portable package to a writable directory, run `UUI Studio.exe`, and retain all accompanying files. For portable upgrades, use a new directory and then open your own projects.

Running Studio and building user applications require neither Python nor an installed Rust compiler. The packages retain Chinese and English offline help and ten editable examples. AI requires your own service and API key; fees and model availability depend on the provider. Older three-argument `UUI` modules and `uui` v2 modules remain supported; do not migrate old code merely by renaming the interface. See the [testing guide](docs/en/testing.md).

## Validation for this batch

- The full 44-product contract gate, complete package file hashes, runtime allowlist, tool import closure, and six SDK inventories.
- The new portable package and an isolated installation of the same payload: actual startup, hidden development menus, rejection of development-only packaging and migration commands, new v2 projects, editing and saving, standalone Windows application builds, and startup/reopening. The portable package also passed BMI calculation of 24.1 and reset checks.
- Isolated copies of both delivery forms passed language grouping, search, regrouping after saving, editing completed translations, cleanup, and persistence after a full process restart. Each passed 11 actual WebView approval UI/native-interface checks.
- Seven native translation-storage tests and 15 approval tests passed, covering both policies, counter failure/repair and real checks, BMI builds, stage pauses, tampering and scope denial, cancellation, and native logs. Model responses come from a scripted test provider, not an online model; these are not new online service acceptance results.
- Installation validation used the production template and identical payload, with a separate test installation identity and adjusted display names. It does not cover directly installing the public EXE on every clean-machine environment. Test uninstallation passed, and the original installation's file fingerprints were unchanged.

## Known scope

Windows uses WebView2 and is affected by the local environment. Existing online AI evidence is from OpenAI and small single-Form applications. Other services, multi-Form orchestration, all component behavior, and online databases require separate validation. Android minimum-spec device testing and comprehensive native acceptance testing of the current Rust versions on Apple platforms and Linux remain incomplete. Android output is an ARM64 debug APK, not a mobile-store production package. General bridging to other programming languages is not implemented. Static identification of risky calls during approval is conservative, not a complete proof of arbitrary JavaScript safety.

## Demo and older versions

The coffee ordering video is the previous Chinese recording, approximately 3 minutes 35 seconds long. It does not demonstrate every new language-grouping or staged-approval interaction in this batch. Its phone-proportioned application runs on Windows and does not establish physical mobile-device acceptance.

The [previous icon revision](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109-logo.1) and [initial preview](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109) remain available. Their attachments and original checksums are not replaced.

## SHA-256

```text
d7e039794d68f2792ca081f6cb74314f5058b28f8f295c47193d08e3985ab18d  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
8422b55677d7ead6e9e834a0af4170b6449a067ed714d5c3e446bc99a7e51072  UUI-Studio-0.1.0-Windows-Rust.zip
```

On Windows, use `Get-FileHash -Algorithm SHA256 -LiteralPath 'path-to-downloaded-file'`. [SHA256SUMS.txt](SHA256SUMS.txt) contains the same hashes.

## Feedback

Use the [testing guide](docs/en/testing.md) to provide the build identifier, system, reproduction steps, and expected/actual results in an [Issue](https://github.com/felixdds/uui-studio/issues). Do not submit keys, connection passwords, private business data, or patient information. Use and distribution remain governed by the supplied agreements and authorization.
