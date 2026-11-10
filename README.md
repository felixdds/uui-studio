# UUI Studio

简体中文 · [English](README.en.md)

[中文故事](stories/README.md) · [English stories](stories/en/README.md) · [Developer commentary in English](docs/en/review.md)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/brand/uui-studio-horizontal-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/brand/uui-studio-horizontal-light.svg">
  <img alt="UUI Studio" src="assets/brand/uui-studio-horizontal-light.svg" width="760">
</picture>

统一用户界面工作室是一套支持可视化设计与 AI 协作的应用开发工具。人通过设计器编辑，AI 通过协议操作，共同维护同一份可编辑工程；生成后仍能继续调整界面、检查业务代码并追加需求。

本次介绍对应的 Windows 测试版本为 **0.1.0，2026-11-09-logo.1 构建批次（新图标修订1）**。欢迎开发者试用、反馈，并探讨联合技术验证与产品合作。

![咖啡点餐应用实际运行](assets/咖啡点餐_会员九折.png)

## 从需求到可维护的应用

用日常语言描述目标，也可附加截图参考。AI 先说明理解、实施步骤和验证计划，经用户在 Studio 批准后才创建组件、编写事件、保存、构建和检查。范围内的问题可继续修复和复测，扩大修改范围需要重新批准。

人工与 AI 可以交替接手同一套组件、属性、事件绑定及关联 JavaScript 模块。已有组件移动时保留身份；属性可恢复默认或继承行为。平台提供统一布局、主题、语言及数据接口，专业开发者仍可检查和编写业务代码。

## 演示与下载

**Windows 预览测试版现已开放下载。** [查看本次发行](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109-logo.1)。

[下载安装包（推荐）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [便携 ZIP（可选）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [中文演示视频](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/UUI-Studio-AI-Cafe-Demo-zh-CN.mp4) · [校验文件](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261109-logo.1/SHA256SUMS.txt)

[下载与演示](下载与演示.md) · [本次发行说明](RELEASE_NOTES.md) · [快速上手与测试反馈](测试指南.md)

咖啡点餐实录约3分35秒：从空白工程开始，生成点餐界面，追加会员九折，经人工复核修正配色，再在实际 Windows APP 中检查结算。视频配有中文解说与字幕，等待与执行加速处有标注。手机比例窗口是在 Windows 运行，不代表本次已完成手机真机验收。

| 文件 | 用途 | 大小 |
| --- | --- | --- |
| UUI-Studio-0.1.0-Windows-Rust-Setup.exe | 推荐，独立安装，无需另下 ZIP | 54.60 MiB |
| UUI-Studio-0.1.0-Windows-Rust.zip | 可选，解压完整目录后运行 | 84.26 MiB |

安装包与便携版均使用 Rust 宿主，界面和业务脚本使用 HTML/CSS/JavaScript。运行 Studio 和构建用户 APP 不需要 Python 或安装 Rust 编译器。包含中英文离线帮助和十个可编辑示例。AI 需要自行配置服务与 API Key，调用费用及可用模型取决于服务方。

## 本次更新

- 本次下载为新图标修订1：Setup、便携 ZIP、窗口与 EXE 图标同步；业务代码和 SDK 未变。

- 计划审批、工程内 AI 历史及截图需求参考。
- 统一75项事件契约和 uui 公共接口；新模块采用 v2，保留旧三参事件模块兼容。
- 完善组件默认值、创建初值与 Dock 空间不足的布局规则。
- 同步中英文离线帮助，以及 Windows 运行、用户 APP 构建和隔离安装验证。

## 当前验证范围

Windows Studio 与独立 APP 已有真实运行及构建证据；AI 在线闭环证据来自 OpenAI 与单 Form 小应用。完整组件契约已公开给 AI，但不表示所有组件业务均完成在线验收。其他模型服务、AI 跨 Form 编排及在线数据库需要分别验证。

Android 当前为 Rust ARM64，最低系统目标为 Android10/API29，WebView120为待最低设备验收的候选下限。macOS、Linux 和 iOS 的当前 Rust 版本尚未完成全面原生验收；iOS/iPadOS17是目标范围。通用其他编程语言桥接仍为后续方向。

## UUI Studio 的故事

UUI Studio 由一名牙医提出构想并主导架构设计，需求、规则与交互判断由人负责，实现代码由 Codex 生成。项目在日常工作间隙逐步推进：AI 能干的事情，就尽量交给 AI，各取所长，不否定别人，也不否定自己。

[从一个跨平台构想开始](stories/01-origin.md) · [五个月的见缝插针式开发](stories/02-between-patients.md) · [一个属性旁边的小叉](stories/03-inline-properties.md)

[中文故事目录](stories/README.md) · [English stories](stories/en/README.md)

[软件开发者视角的评述](docs/review.md) · [Developer commentary in English](docs/en/review.md)

## 联合验证与合作

希望与开发工具、研发效能及应用开发团队交流，由架构设计者与专业工程师共同选择一个小型业务场景，验证工程可维护性、AI 增量修改、构建与问题定位，再讨论产品完善、发行及推广合作。欢迎通过[Issues](https://github.com/felixdds/uui-studio/issues) 提出技术交流意向，请勿在公开反馈中提交密钥或业务私密资料。

本仓库用于产品展示与测试分发，未附 Studio 完整 Rust 源码。公开资料和测试包的提供不构成开源许可；使用与分发范围以软件随附协议及权利方授权为准。
