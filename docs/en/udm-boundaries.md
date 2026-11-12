# UDM and WebView responsibilities

**WebView handles complexity; UDM selects the necessary semantics. UDM does not duplicate WebView capabilities: it defines the minimal application semantics and maps them to capabilities the browser already implements.**

| Layer | Owns | Does not own |
| --- | --- | --- |
| UDM | Application structure, component semantics, permitted properties/values and event contracts | The entire CSS feature set |
| Translation and projection | Mapping valid UDM to DOM/CSS/JS | Reimplementing a browser layout engine |
| WebView | HTML/CSS/JS, inheritance, precedence, layout, painting and interaction | Deciding which properties UDM exposes |

For a property whose contract permits Width = 900px, the translation layer can express the corresponding CSS width and delegate layout to WebView. This does not automatically expose every CSS unit or alter the existing schema. Rust processing and existing JavaScript Adapters cooperate within their established ownership; this is not a claim that every shared rule has moved to Rust. Platform-specific semantics and controlled transactions remain owned by the platform. Generated DOM/CSS do not become the authoritative application definition.
