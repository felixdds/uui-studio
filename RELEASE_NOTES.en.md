# UUI Studio 0.1.0 — Whole-window zoom and Android release builds

Batch: 2026-11-11-motion-android.1 (Windows preview).

[Installer (recommended)](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [Portable ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/SHA256SUMS.txt)

## Fixes and features

- **Restored Windows main-window zoom in/out on opening and closing.** The title bar, border and workspace scale together while the actual window and WebView size stay unchanged. Existing speed, disabled-motion and reduced-motion settings apply. Cancelling a close does not trigger exit zoom.
- **The existing Android build dialog now offers Debug APK or Release AAB + APK.** Debug remains the default. Release uses the current project package, version, icon and dependencies, disables debugging, and creates or reuses the package's upload key.
- Build-mode and SDK-license dialogs keep a normal pointer; waiting begins after confirmation starts the actual build.
- AI is a primary button. The Windows Build menu offers the installer only; Run APP / F5 generates and starts the Windows application automatically.
- English/Chinese offline help, downloads and testing instructions are updated. Motion preflight checks and UDM/WebView responsibility boundaries are documented. Language groups, task/stage approval and contextual help remain included.

## Installation and upgrades

The installer is standalone (58,414,894 bytes); the ZIP is optional (89,303,195 bytes). Close Studio and back up projects and Data first. Fully extract the ZIP into a new directory rather than overwriting edited examples. Older downloads do not acquire this fix automatically.

**Securely back up Studio Data/Signing and its private recovery instructions; never publish signing credentials.** Missing or unreadable existing credentials stop the build instead of replacing the key. Building an AAB does not imply Google Play approval.

> **Windows SmartScreen:** This preview has no trusted code-signing certificate. Windows may show “Windows protected your PC” or “Unknown publisher.” Verify the official project Release and SHA-256 checksums. If you have verified the source and choose to trust it, use “More info → Run anyway” when Windows offers that option. Do not disable system protection. Stop and report any specific malware detection.

## Validation and limits

All 44 product contracts and positive/negative motion checks passed. Release payload hashes, six SDK inventories and source identity passed. Tests cover isolated install/uninstall, actual WebView2 AI/menu/Android-dialog behavior, a standalone Windows APP with BMI calculation/reset, and signed Android Release AAB + APK built by the packaged Studio. Actual intermediate DWM projection geometry, stable source-window dimensions and cleanup were checked.

This does not establish minimum Android10/WebView120 or iOS/iPadOS17 device acceptance, online database acceptance, or expanded Apple/Linux native support. Android remains ARM64.

[Previous release](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261111-help-locale.1) · [1080p bilingual demo](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

```text
e38663558f6f053cbb232bcddfaba262a53695a114cfa392faf782b91cf101e5  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
fc650b5f221e5a557ac40afd34ee96ea2f8fcff8a84efebf67bb3fe9d1817ad6  UUI-Studio-0.1.0-Windows-Rust.zip
```
