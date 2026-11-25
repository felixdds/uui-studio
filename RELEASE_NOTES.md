# UUI Studio 0.2.0-alpha.1

这是一次底层架构迁移与跨平台构建验证的预发行。Studio 继续提供原有可视化设计和 AI 协作工作流。UCM 工程数据以 JSON 保存，生成的 APP 只带工程所需的运行代码和资源。

- Windows：独立安装包与便携 ZIP 已在隔离目录启动验证，两者均核对了中英文离线帮助。
- Android：此前已验证同一工程能生成并运行 Android ARM64 APP。本轮没有新增 Android 真机或最低环境验收。
- Windows 如提示未知发布者，请核对本页的 SHA-256 校验值。安装包可独立使用。

This prerelease validates the underlying UCM migration and cross-platform build architecture. Studio preserves its visual design and AI collaboration workflows. UCM projects use JSON, and built applications include the runtime code and resources their projects need.

- Windows: the installer and portable ZIP were launched from isolated locations. English and Simplified Chinese offline Help loaded in both.
- Android: earlier Windows/Android build and Android ARM64 runtime validation demonstrated cross-platform feasibility. This release adds no new Android device or minimum-environment validation.
- The Windows installer is self-contained. If Windows reports an unknown publisher, verify the SHA-256 checksums below.

[0.1 historical release](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261111-motion-android.1)

~~~text
e494a2afe1f55680bda1ea047dbe6d73c6f1775740f65713c5e3384fef0e8055  UUI-Studio-0.2.0-alpha.1-Windows-Setup.exe
479517354bf72425900c28959f6e7bcf075ac581bf77841ef962ef3ddd00d27a  UUI-Studio-0.2.0-alpha.1-Windows.zip
~~~

## 修复更新 / Corrected Windows packages

- 修复安装版 Run APP 缺少构建输入的问题，并验证了 BMI 的构建、启动、计算和 Reset。
- 修复 Primary 按钮文字误用禁用颜色的问题。
- Fixed missing build input in installed Studio and verified BMI build, launch, calculation, and reset. Restored Primary button text contrast.
