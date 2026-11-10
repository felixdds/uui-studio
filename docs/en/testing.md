# Getting Started and Test Feedback

[简体中文](../../测试指南.md) · English

## First run

1. Install the setup package or fully extract the portable package, then launch UUI Studio. The Windows host uses WebView2. If startup fails, record the actual error.
2. Open a bundled example or create a separate project, and save it to your own directory.
3. Change a component's text, size, or layout. Save, close, and reopen the project to confirm the change was retained.
4. Use **Run APP** or **F5** to run it and check the actual interactions. Then build a standalone Windows application.
5. Read the event and public-interface documentation in the built-in help before adding business logic. Maintain older three-argument modules and new `uui` v2 modules according to their respective protocols.

## Try AI collaboration

Configure your own service and API key in **Connection**. You can request a small counter or an ordering interface on the current Form, optionally including screenshots as references. Review AI's understanding, plan, and scope of changes before clicking **Approve and execute** (批准并执行 in the Chinese interface).

After running the application, check its layout and business logic, then request an incremental change. Verify that existing components and behavior are retained and remain editable in the designer. Visibility of the complete contracts does not guarantee correct generation every time. Online services, models, and image capabilities depend on your actual configuration.

Project sessions are saved in the project's `.uui` directory. Keep that directory when copying a project to continue working on it. On a new machine, use your own key. Before sharing a project, check whether its business content and history are suitable for public disclosure.

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
