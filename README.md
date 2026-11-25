# UUI Studio

简体中文 · [English](README.en.md)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/brand/uui-studio-horizontal-dark.png">
  <img alt="UUI Studio" src="assets/brand/uui-studio-horizontal-light.png" width="760">
</picture>

UUI Studio 是一套支持可视化设计和 AI 协作的应用开发工具。人可以在设计器中编辑界面、属性和事件，AI 可以在批准的范围内操作同一份工程。应用生成后，工程和业务脚本仍可继续编辑。

## UCM 架构文件

这两份 JSON 是 Studio 使用的 UCM 源声明。Definition 定义组件、属性、事件和规则，Defaults 定义缺省值和创建时的初始内容。Studio 与构建工具通过共用入口展开紧凑的声明，工程只保存作者显式设置的值。生成 APP 时，构建器按工程使用的组件和能力选择运行代码和资源。

[查看 ucm-definition.json](architecture/ucm/ucm-definition.json) · [查看 ucm-defaults.json](architecture/ucm/ucm-defaults.json)

## 0.2.0-alpha.1

这次预发行完成了底层架构迁移，保留已有的设计和 AI 工作流。工程使用 JSON 格式的 UCM，构建器按工程抽取运行所需的组件代码和资源。同一工程的 Windows 与 Android 构建已在开发过程中验证。这个版本用于技术评估和试用。

[Windows 安装包](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.1/UUI-Studio-0.2.0-alpha.1-Windows-Setup.exe) · [便携 ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.1/UUI-Studio-0.2.0-alpha.1-Windows.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.2.0-alpha.1.ucm.1/SHA256SUMS.txt) · [发行说明](https://github.com/felixdds/uui-studio/releases/tag/v0.2.0-alpha.1.ucm.1)

安装包可独立使用。Windows 可能提示未知发布者，请确认下载来源并核对 SHA-256。便携 ZIP 请完整解压到新目录。包内包含中英文离线帮助和可编辑示例。AI 功能需要自行配置服务和 API Key。

## 寻找接手开发的团队

我是一名牙医，也是 UUI Studio 的发起人、架构设计者和项目负责人。这个项目源于我长期想解决的一个问题：如何减少跨平台 UI 开发中的重复工作，让使用者和专业开发者都能继续修改同一个应用。

我希望一家有长期投入能力的公司或专业团队接手后续开发。我愿意继续负责架构设计和项目方向，和团队一起确定优先级、审查关键设计并推进交付。团队可以接手工程实现、系统测试、跨平台兼容验证和发布维护，让项目从可运行的原型走向可靠的产品。

可以先选一个小型业务场景，一起评估工程的可维护性、AI 审批流程和跨平台构建，再讨论长期合作与交接。欢迎通过 [GitHub Issues](https://github.com/felixdds/uui-studio/issues) 提出技术交流意向。

[项目故事](stories/README.md) · [下载与演示](下载与演示.md) · [历史演示](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1) · [0.1 历史版本](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261111-motion-android.1)

本仓库用于公开介绍、测试分发和技术交流。Studio 的完整源码未在此公布，软件使用和分发以随附协议及权利人授权为准。
