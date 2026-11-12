# UDM 与 WebView 的职责边界

**WebView 负责复杂性，UDM 负责选择性。UDM 不复制 WebView 的能力，而是定义应用所需的最小语义集合，并映射到 WebView 已实现的能力。**

| 层次 | 负责 | 不负责 |
| --- | --- | --- |
| UDM | 应用结构、组件语义、允许的属性和值、事件契约 | 支持全部 CSS 功能 |
| 翻译与投影层 | 将合法 UDM 映射为 DOM/CSS/JS | 重写浏览器布局引擎 |
| WebView | HTML/CSS/JS、继承、优先级、布局、绘制和交互 | 决定 UDM 应暴露哪些属性 |

例如，若属性契约允许 Width = 900px，翻译层将它表达为对应 CSS，由 WebView 布局；这不自动开放全部 CSS 单位，也不改变现有 schema。Rust 处理实现与现有 JS Adapter 在既定所有权内协作，不表示全部共享规则已迁入 Rust。UDM 特有语义和受控事务仍由平台负责，DOM/CSS 只是生成结果，不反过来成为应用权威。
