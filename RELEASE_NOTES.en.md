# UUI Studio Windows Preview release notes

**Updated batch: 2026-11-11-bridge-help.1.** Unified help icons, sizes and hover/pressed/focus feedback; restored AI window controls to the right; standardized native bridges on UUI naming and removed retired runtime remnants. Packaged Windows, independent APP builds and execution, and all 44 product contracts passed.

Version: 0.1.0 · 2026-11-11-bridge-help.1

[Setup](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/SHA256SUMS.txt)

## Changes

- Each operational dialog declares its help topic; a shared mechanism opens bundled offline Help with ? or F1. Existing component/property and AI help is reused.
- Closing Help restores the original dialog and focus; opening Help does not accept or cancel its draft. Nested dialogs and repeated clicks were checked in Windows WebView2.
- Nine Simplified Chinese translations now match their current source, including service-key management, saved-key status, empty Form description, search and platform labels. Source hashes are updated after reviewing the wording. Existing local overrides were handled separately.

Standalone Setup (recommended): 58,400,747 bytes. Optional portable ZIP: 89,276,700 bytes.

## Validation and scope

All 44 product contract checks passed. The pristine payload manifest and file hashes were checked. Actual Windows tests cover packaged Chinese status, help routing, focus/draft retention, nested help and simple-confirmation exclusion. This is a preview, not minimum Android/iOS device acceptance. Existing language-grouping and task/stage AI approval features remain included.

[Previous software and 1080P demonstration](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

```text
96b43874c1e6ffd71b4190aad2a1e2ec0a88b64cf532cfa788ff5ef4273ffc3f  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
0768dc8497e889bc1821f47eefa32a1a1d7380263a461c3ba9e87b17879e64d9  UUI-Studio-0.1.0-Windows-Rust.zip
```
