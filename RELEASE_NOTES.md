# UUI Studio Windows 测试版发行说明

**帮助与简体中文修订：2026-11-11-help-locale.1。** 13 个操作窗口统一支持标题栏“？”和 F1，上下文帮助包含中英文，简单确认框不加。九项过时译文已更新；本批次干净安装的简体中文待更新为 0。旧软件和演示视频继续保留。

版本: 0.1.0 · 2026-11-11-help-locale.1

[Setup](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-help-locale.1/SHA256SUMS.txt)

## 更新内容

- 操作窗口各自声明帮助主题，通用机制通过“？”和 F1 打开随包离线帮助，复用既有属性、组件和 AI 帮助。
- 关闭帮助返回原窗口并恢复焦点；帮助操作不提交或取消原窗口草稿。已在 Windows WebView2 验证嵌套窗口与重复点击。
- 九项简体中文译文与当前源文同步，包括服务密钥管理、密钥保存状态、空白 Form、搜索及平台标签；逐条审阅后更新源文校验值。本地覆盖译文单独处理。

独立 Setup（推荐）: 58,399,740 bytes. 可选便携 ZIP: 89,276,497 bytes.

## 验证与范围

44 项产品契约检查全部通过；检查干净载荷清单及文件哈希。Windows 实测覆盖包内中文状态、帮助主题跳转、焦点与草稿保留、嵌套帮助及简单确认框排除。本版仍是预览版，不代表最低 Android/iOS 设备验收；继续包含此前的翻译分组与按任务／按阶段 AI 审批功能。

[旧软件与 1080P 演示](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

```text
a16791a228715254b3b6b8e157e95ab3ff24a9ecf6feb13c240dd73a976e3554  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
c17457d18334689c4c46935ab0fec36c499dd443953a91e24a1fd7031bd7777c  UUI-Studio-0.1.0-Windows-Rust.zip
```
