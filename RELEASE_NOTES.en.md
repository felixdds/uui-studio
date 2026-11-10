# UUI Studio Windows Preview Release Notes

[简体中文](RELEASE_NOTES.md) · English

Version: 0.1.0. Build: 2026-11-09-logo.1. Status: preview test version, new icon revision 1.

This preview is available on [GitHub Releases](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109-logo.1).

[Installer (recommended)](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [Portable ZIP (optional)](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [Demo video in Chinese](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-AI-Cafe-Demo-zh-CN.mp4) · [Checksums](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/SHA256SUMS.txt)

## Choose a download

The recommended standalone installer is `UUI-Studio-0.1.0-Windows-Rust-Setup.exe`, 57,250,833 bytes (54.60 MiB). The optional portable package is `UUI-Studio-0.1.0-Windows-Rust.zip`, 88,355,186 bytes (84.26 MiB). Choose either one; the installer does not depend on the ZIP.

The filenames are the same as those used for the previous version. Distinguish packages by build identifier and SHA-256 to avoid confusing an older package with this revision.

## This icon revision

The installer, portable ZIP, window, and EXE use the new UUI Studio icon, supplied in nine sizes. Compared with the initial ZIP, only the icon SVG, ICO, EXE icon resources, and package manifest changed. Business logic and the SDK are unchanged. Checks covered portable operation, isolated installation, user application builds, application launch and reopening, and uninstallation. The original installation files were left unchanged.

The [original preview archive](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109) remains available. The demo video content is unchanged.

## Retained product capabilities

- Synchronized Windows runtime files, native plan approval, project-local AI history, and screenshot references for requirements. Within an approved scope, AI can move existing components and restore default property behavior.
- A unified set of 75 event contracts and the public `uui` entry points. New modules use v2, while existing three-argument `UUI` modules remain compatible. User business logic is not rewritten in bulk.
- Updated component defaults, initial values at creation, and rules for insufficient Dock space. Edge controls retain their sizes, and the remaining space has a minimum of zero.
- Synchronized event examples and interface documentation in Chinese and English offline help.

## Installation and upgrades

Close Studio and related applications, and back up your projects and data first. Follow the setup wizard for the installer. For the portable version, extract the full package into a writable directory and run `UUI Studio.exe`, keeping all accompanying files intact. When upgrading the portable version, extract it to a new directory and then open your own projects.

After creating a project or opening an example, you can edit properties, save, and run the application. Configure your own API key before using AI. Event protocol upgrades preserve compatibility with old modules. Do not migrate existing code merely by renaming `UUI` to `uui`. Consult the software's Chinese or English built-in help and the [testing guide](docs/en/testing.md) for details.

## Existing validation

Records for this release batch include complete contract checks, ZIP payload and SDK verification, portable-package project creation, editing and saving, user application builds and reopening, BMI behavior checks, and operation and uninstallation after an isolated installation.

The installation checks used the same payload and installer template as the published package, with a separate test installation identity to protect the original installation registration. They do not cover every clean-machine environment. The AI demo is an existing Windows recording using OpenAI and a single Form. The release checks do not mean all online AI scenarios were rerun individually.

## Known scope

- Windows uses WebView2 and is affected by the local environment.
- Current online AI evidence focuses on small OpenAI applications using a single Form. Other services, AI orchestration across Forms, and all component behavior require separate acceptance testing. Screenshot processing requires a model with image support.
- Online database acceptance testing is deferred. Android minimum-spec device validation and comprehensive native acceptance testing of the current Rust versions on Apple platforms and Linux are incomplete.
- Android output is an ARM64 debug APK, not a production mobile-store release package.
- General bridging to other programming languages has not been implemented.

## SHA-256

```text
03a9e68bdc88bd737e8bc6721d618d42cbf56f92adfe2d84f797fa21293ff64e  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
b2d21120824c065a862b6e16e0768bf97578da78b41f52909bf1521f779b7b10  UUI-Studio-0.1.0-Windows-Rust.zip
```

On Windows, check a downloaded file using `Get-FileHash -Algorithm SHA256 -LiteralPath 'path-to-downloaded-file'`. [SHA256SUMS.txt](SHA256SUMS.txt) contains the same hashes.

## Feedback

Use the [testing guide](docs/en/testing.md) to record your system, build identifier, reproduction steps, and expected and actual results, then submit a repository [Issue](https://github.com/felixdds/uui-studio/issues). Testing scope and permission to use or distribute the software are governed by the accompanying agreements and actual authorization.

[English product homepage](README.en.md) · [Downloads and demo](docs/en/downloads.md)
