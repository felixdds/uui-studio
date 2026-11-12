# Getting Started and Test Feedback

**Updated batch: 2026-11-11-bridge-help.1.** Unified help icons, sizes and hover/pressed/focus feedback; restored AI window controls to the right; standardized native bridges on UUI naming and removed retired runtime remnants. Packaged Windows, independent APP builds and execution, and all 44 product contracts passed.

[简体中文](../../测试指南.md) · English

## First run

1. Install the setup package or fully extract the portable package, then launch UUI Studio. The Windows host uses WebView2. If startup fails, record the actual error.
2. Open a bundled example or create a separate project, and save it to your own directory.
3. Change a component's text, size, or layout. Save, close, and reopen the project to confirm the change was retained.
4. Use **Run APP** or **F5** to run it and check the actual interactions. Then build a standalone Windows application.
5. Read the event and public-interface documentation in the built-in help before adding business logic. Maintain older three-argument modules and new `uui` v2 modules according to their respective protocols.

## Try AI collaboration

Use the menu beside the approval button to select task approval (default) or approval by implementation stage. Task approval permits implementation, checks, and ordinary repairs within the declared scope to continue. Stage approval pauses before subsequent stages until the current stage is approved. The policy cannot change while a task is running or a plan awaits approval. The main button approves; selecting a policy does not itself authorize execution.

Configure your own service and API key in **Connection**. You can request a small counter or an ordering interface on the current Form, optionally including screenshots as references. Review AI's understanding, plan, and scope of changes before clicking **Approve and execute** (批准并执行 in the Chinese interface).

After running the application, check its layout and business logic, then request an incremental change. Verify that existing components and behavior are retained and remain editable in the designer. Visibility of the complete contracts does not guarantee correct generation every time. Online services, models, and image capabilities depend on your actual configuration.

Project sessions are saved in the project's `.uui` directory. Keep that directory when copying a project to continue working on it. On a new machine, use your own key. Before sharing a project, check whether its business content and history are suitable for public disclosure.

## Try the language editor

Open Studio's language editor and select an editable target language. Check the groups for entries removed from source, entries needing an update, and updated entries. Counts should follow the current filter; empty groups are hidden.

Save a translation needing an update and check its regrouping, then edit an updated translation. Close and reopen the editor to confirm persistence. Source-language and legacy review-data read-only protections remain unchanged.

When confirmed removed entries exist, the cleanup action asks for confirmation and applies to all such entries in that language, not just the search results. Check the count in the confirmation dialog first. After restarting, check that cleanup persists and active translations remain correct. Do not delete valid translations merely to test this behavior.

## Issue report template

- Studio version and build identifier:
- Installer or portable package, and its SHA-256:
- Windows version, display scaling, and WebView2 version, if available:
- Minimal steps to reproduce:
- Expected result:
- Actual result and error text:
- Screenshots, logs, or a minimal example suitable for public sharing:
- For AI-related issues, the service, model, and task stage involved:

Do not submit API keys, connection passwords, or private business data. If you only want to discuss a technical topic, describe the scenario in an [Issue](https://github.com/felixdds/uui-studio/issues); there is no need to publish your personal phone number.

For the scope of existing checks and pending validation, see the [release notes](../../RELEASE_NOTES.en.md#known-scope) and [product validation summary](../../README.en.md#current-validation-scope).

[English product homepage](../../README.en.md) · [Downloads and demo](downloads.md) · [Release notes](../../RELEASE_NOTES.en.md)

## Context help and translation check

Open New Project or Settings, choose ? or press F1, then close Help: focus and draft input should return. In AI Workspace, test Help inside Manage AI keys as well. Simple yes/no confirmations have no Help button. Open the Simplified Chinese language editor: this batch has no missing or outdated source entries in a clean profile. Existing locally customized translations may still require review.
