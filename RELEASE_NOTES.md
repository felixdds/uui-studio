# UUI Studio 0.1.0 — 整窗 zoom 与 Android 正式构建

批次：2026-11-11-motion-android.1（Windows 预览版）。

[安装包（推荐）](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/UUI-Studio-0.1.0-Windows-Rust-Setup.exe) · [便携 ZIP](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/UUI-Studio-0.1.0-Windows-Rust.zip) · [SHA-256](https://github.com/felixdds/uui-studio/releases/download/v0.1.0-preview.20261111-motion-android.1/SHA256SUMS.txt)

## 重点修复与新增功能

- **修复 Windows 主窗口开启、关闭时丢失的 zoom in/out。** 标题栏、边框和整个工作区一起缩放；真实窗口与 WebView 尺寸保持不变。速度沿用现有设置，禁用动画或减少动态效果时跳过。取消关闭不触发退出动画。
- **Android 原有构建界面整合 Debug APK / Release AAB＋APK。** 默认 Debug，Release 使用当前工程包名、版本、图标和依赖，关闭调试；上传密钥按包名创建或复用。
- 模式选择、SDK 许可确认期间鼠标保持正常，确认开始构建后才显示等待状态。
- AI 改为 primary 主按钮。Windows 构建菜单只保留安装包入口；Run APP / F5 自动生成并启动 Windows 应用。
- 中英文离线帮助、下载与测试说明同步更新；动画执行前检查和 UDM/WebView 分工形成明确契约。既有语言分组、任务/阶段审批和上下文帮助继续保留。

## 安装与备份

Setup 可独立使用（58,414,894 字节）；ZIP 为可选便携分发（89,303,195 字节）。安装前关闭 Studio，备份工程和 Data。ZIP 请完整解压到新目录，避免覆盖自己改过的示例。旧包不会自动获得本次修复。

**请安全备份 Studio Data/Signing 及私密恢复说明，不要上传到公开仓库。** 无法使用已有签名凭据时停止构建，不自动替换密钥。AAB 构建成功不等于 Google Play 批准。

> **Windows SmartScreen 提示：** 本预览版尚未使用受信任的代码签名证书，Windows 可能显示“已保护你的电脑”或“未知发布者”。请核对来自本项目官方 GitHub Release，并验证 SHA-256；确认来源且自行信任后，可在 Windows 提供此选项时选择“更多信息 → 仍要运行”。无需关闭系统防护；若出现明确恶意软件检测，请停止运行并反馈。

## 验证与范围

44 项产品契约及动效正反检查通过。发行载荷全文件清单、六组 SDK 和源码一致性通过；隔离安装/卸载、真实 WebView2 的 AI/菜单/Android 对话框、独立 Windows APP 运行及 BMI 计算/重置、发行版 Studio 生成签名 Android Release AAB＋APK 通过。DWM 投影的实际中间尺寸、源窗口尺寸不变和清理已验证。

这不代表最低 Android10/WebView120、iOS/iPadOS17 设备或在线数据库已验收；Apple/Linux 原生范围不扩大。Android 当前为 ARM64。

[上一版本](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261111-help-locale.1) · [1080p 中英字幕演示](https://github.com/felixdds/uui-studio/releases/tag/v0.1.0-preview.20261110-locale-approval.1)

```text
e38663558f6f053cbb232bcddfaba262a53695a114cfa392faf782b91cf101e5  UUI-Studio-0.1.0-Windows-Rust-Setup.exe
fc650b5f221e5a557ac40afd34ee96ea2f8fcff8a84efebf67bb3fe9d1817ad6  UUI-Studio-0.1.0-Windows-Rust.zip
```
