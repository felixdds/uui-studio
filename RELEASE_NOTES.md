# UUI Studio Windows 测试版发行说明

简体中文 · [English](RELEASE_NOTES.en.md)

版本：0.1.0。构建批次：2026-11-10-locale-approval.1。性质：预览测试版，翻译与审批修订1。

[查看本次发行](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

[下载安装包（推荐）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [便携 ZIP（可选）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [1080P 中英字幕演示](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-Localization-Approval-1080p-zh-en.mp4) · [校验文件](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/SHA256SUMS.txt)

## 下载选择

推荐独立安装包 `UUI-Studio-0.1.0-Windows-Rust-Setup.exe`，57,289,602 字节（54.64 MiB）；可选便携包 `UUI-Studio-0.1.0-Windows-Rust.zip`，88,405,074 字节（84.31 MiB）。二者任选其一，Setup 不依赖 ZIP。文件名保持不变，请用构建批次和 SHA-256 区分新旧包。

## 本次更新

- 语言编辑器按“已从源文移除、待更新、已更新”分组，空组隐藏，显示筛选计数；保存后重新分组，已更新的目标译文仍可编辑。
- 清理先确认该语言全部已确认移除的条目，不只处理搜索结果。修复旧随包译文在合并后重新出现的问题；同名源文重新加入仍可出现，不误删活动翻译。
- AI 批准入口改为 SplitButton，主按钮批准，下拉选择按任务或按实施阶段；旧工程默认按任务。逐项策略初次批准覆盖总计划与第一阶段，后续阶段暂停等待批准；当前已批范围内普通修复可以继续。
- 批准关联计划、范围、输入版本和一次性原生授权；越界和版本变化会阻止旧批准继续使用。原生审批记录在现有消息区查看，写入失败或容量上限阻止新授权；历史聊天不能授权。没有新增 shell、文件删除或依赖安装工具。
- 附件入口为输入框前“＋”，当前附加图片；会话列表标题两行显示，过长省略并提示全文。中英文内置帮助同步以上操作。

## 安装与升级

关闭 Studio 和相关 APP，先备份自己的工程与数据。Setup 按向导安装。便携版完整解压到可写目录，运行 `UUI Studio.exe`，保持配套文件完整；升级时建议解压到新目录，再打开自己的工程。

运行 Studio 和构建用户 APP 不需要 Python 或安装 Rust 编译器。包内保留中英文离线帮助及十个可编辑示例。AI 使用自己的服务和 API Key，费用与模型可用性由服务方决定。事件模块继续保留 `UUI` 三参旧协议和 `uui` v2，不要仅通过改名迁移旧代码。详见[测试指南](测试指南.md)。

## 本批次验证

- 完整 44 项产品契约检查；新包完整文件哈希、运行文件白名单、工具依赖闭包及六组 SDK 清单。
- 新便携包和同载荷隔离安装：实际启动、隐藏开发菜单、拒绝开发专用打包／迁移入口、新建 v2 工程、编辑保存、独立 Windows APP 构建与启动／重开；便携包另检查 BMI 计算 24.1 和重置。
- 两种交付形态的隔离副本均检查语言分组、搜索、保存后重分组、完成译文继续编辑、清理和完整进程重启后的持久化；均通过 11 项真实 WebView 审批界面／原生接口检查。
- 原生翻译存储 7 项与审批 15 项测试通过，包括两种审批模式、计数器失败修复和真实检查、BMI 构建、阶段暂停、篡改／越权拒绝、取消及原生日志。模型响应来自脚本化测试提供器，不调用在线模型，不把它写成新增在线服务验收。
- 隔离安装验证使用正式模板和相同载荷，仅调整测试安装身份及显示名称等；不是在所有干净机器上直接安装公开 EXE 的覆盖。测试卸载通过，原有安装文件指纹不变。

## 验证边界

Windows 使用 WebView2，受本机环境影响。既有在线 AI 证据来自 OpenAI 单 Form 小应用；其他服务、多 Form 编排、所有组件业务及在线数据库仍需分别验证。Android 最低设备、当前 Rust 的 Apple/Linux 全面原生验收仍未完成；Android 输出为 ARM64 调试 APK，不是商店正式包。通用其他语言桥接尚未实现。审批中的危险调用识别是保守静态检查，不是任意 JavaScript 的完整安全证明。

## 演示与旧版

新增[1080P 中英字幕演示](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261110-locale-approval.1/UUI-Studio-Localization-Approval-1080p-zh-en.mp4)，约 2 分 34 秒，展示翻译分组与两种审批方式。它使用真实 OpenAI 单 Form 实录，包含第二阶段的原生待批；这是新增演示证据，与上文安装包发布前的离线专项测试分开。[字幕与范围说明](docs/demo-1080p.md)。软件包及原校验值不变。

咖啡点餐视频沿用之前约 3 分 35 秒的中文录制，不演示本批次全部新增的语言分组和阶段审批；其手机比例窗口运行于 Windows，不代表手机真机验收。

[上一批次 新图标修订1](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109-logo.1)与[最初预览版](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261109)继续保留，旧附件与原校验值不替换。

## SHA-256

```text
d7e039794d68f2792ca081f6cb74314f5058b28f8f295c47193d08e3985ab18d  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
8422b55677d7ead6e9e834a0af4170b6449a067ed714d5c3e446bc99a7e51072  UUI-Studio-0.1.0-Windows-Rust.zip
```

Windows 可用 `Get-FileHash -Algorithm SHA256 -LiteralPath '下载文件路径'` 核对。[SHA256SUMS.txt](SHA256SUMS.txt)提供相同摘要。

## 反馈

按[测试指南](测试指南.md)提供构建批次、系统、复现步骤及预期／实际结果，在 [Issues](https://github.com/felixdds/uui-studio/issues)反馈。不要提交密钥、连接口令、私密业务或患者资料。使用与分发范围仍以软件随附协议及授权为准。
