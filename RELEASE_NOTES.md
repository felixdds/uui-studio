# UUI Studio Windows 测试版发行说明

版本：0.1.0。构建批次：2026-11-09。性质：预览测试版。

本次预览测试版已在 [GitHub Releases](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109) 发布。

[下载安装包（推荐）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [便携 ZIP（可选）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109/UUI-Studio-0.1.0-Windows-Rust.zip) · [中文演示视频](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109/UUI-Studio-AI-Cafe-Demo-zh-CN.mp4) · [校验文件](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109/SHA256SUMS.txt)

## 下载选择

推荐独立 Setup：`UUI-Studio-0.1.0-Windows-Rust-Setup.exe`，57,227,747字节（54.58 MiB）。可选便携版：`UUI-Studio-0.1.0-Windows-Rust.zip`，88,347,835字节（84.26 MiB）。两者任选其一；Setup 不依赖 ZIP。

文件名与此前版本相同，请以构建批次及 SHA-256 区分，避免重复发布同名旧包。

## 更新内容

- 同步当前 Windows 运行载荷、原生计划审批、AI 工程历史及截图需求参考；AI 可按批准范围移动已有组件并恢复属性默认行为。
- 统一75项事件契约及 uui 公共入口。新模块使用 v2，已有 UUI 三参模块继续兼容，不批量改写用户业务。
- 更新组件默认值、创建初始值及 Dock 空间不足规则，保留边缘控件尺寸，剩余空间最低为零。
- 同步中英文离线 Help 的事件示例和接口说明。

## 安装与升级

关闭正在运行的 Studio 与相关 APP，先备份自己的工程和数据。Setup 按向导安装；便携版完整解压至可写目录，运行 `UUI Studio.exe`，保持配套文件完整。升级便携版建议解压到新目录，再打开自己的工程。

新建或打开示例后，可编辑属性、保存并运行 APP；AI 使用前需配置自己的 API Key。事件协议升级保持旧模块兼容，勿仅将 UUI 改名为 uui 来迁移现有代码。详细操作见软件自带中英文帮助与[测试指南](测试指南.md)。

## 已有验证

本批次发行记录包含完整契约检查、ZIP载荷与SDK校验、便携版新建编辑保存、用户APP构建和重开、BMI业务检查，以及隔离安装后的运行与卸载验证。

安装验证使用与正式包相同载荷和同一安装模板，修改测试安装身份以保护原安装登记；不是对所有干净机器环境的覆盖。AI 演示来自已有 Windows OpenAI 单 Form 实录，本次发行检查不等于逐项重跑所有 AI 在线场景。

## 已知范围

- Windows 使用 WebView2，受本机环境影响。
- 当前 AI 在线证据集中于 OpenAI 单 Form 小应用；其他服务、多 Form AI 编排、所有组件业务均需分别验收。模型需支持图片才能处理截图。
- 在线数据库验收暂缓；Android最低设备及当前Rust的Apple/Linux全面原生验收未完成。
- Android输出为 ARM64 调试 APK，不作为移动商店正式发行包。
- 通用其他语言桥接尚未实现。

## SHA-256

```text
0ceedaab319e75b62653aa827184a77ee23b03f35373d1005b4c465b5464af06  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
3c51a481a36dcfb3b87cef510f174077b3f2150a9115892e31ed0181ac9760f1  UUI-Studio-0.1.0-Windows-Rust.zip
```

Windows 可用 `Get-FileHash -Algorithm SHA256 -LiteralPath '下载文件路径'` 核对。[SHA256SUMS.txt](SHA256SUMS.txt)提供相同摘要。

## 反馈

请按[测试指南](测试指南.md)记录系统、构建批次、复现步骤、期望与实际结果，在仓库 Issue 提交。测试范围、使用及分发授权以随附协议和实际授权为准。
