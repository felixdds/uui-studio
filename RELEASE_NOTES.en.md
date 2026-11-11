# UUI Studio Windows Preview release notes

**Help and Simplified Chinese revision: 2026-11-11-help-locale.1.** Thirteen operational dialogs share title-bar ? and F1 context help in English and Simplified Chinese; simple confirmations are excluded. Nine outdated translations are updated, with zero pending Simplified Chinese entries in a clean installation of this batch. Previous software and demonstration videos remain available.

Version: 0.1.0 · 2026-11-11-help-locale.1

[Setup](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/SHA256SUMS.txt)

## Changes

- Each operational dialog declares its help topic; a shared mechanism opens bundled offline Help with ? or F1. Existing component/property and AI help is reused.
- Closing Help restores the original dialog and focus; opening Help does not accept or cancel its draft. Nested dialogs and repeated clicks were checked in Windows WebView2.
- Nine Simplified Chinese translations now match their current source, including service-key management, saved-key status, empty Form description, search and platform labels. Source hashes are updated after reviewing the wording. Existing local overrides were handled separately.

Standalone Setup (recommended): 58,399,740 bytes. Optional portable ZIP: 89,276,497 bytes.

## Validation and scope

All 44 product contract checks passed. The pristine payload manifest and file hashes were checked. Actual Windows tests cover packaged Chinese status, help routing, focus/draft retention, nested help and simple-confirmation exclusion. This is a preview, not minimum Android/iOS device acceptance. Existing language-grouping and task/stage AI approval features remain included.

[Previous software and 1080P demonstration](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

```text
a16791a228715254b3b6b8e157e95ab3ff24a9ecf6feb13c240dd73a976e3554  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
c17457d18334689c4c46935ab0fec36c499dd443953a91e24a1fd7031bd7777c  UUI-Studio-0.1.0-Windows-Rust.zip
```
