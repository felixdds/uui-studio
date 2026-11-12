# Motion behavior

The Windows Studio window uses whole-window zoom in/out, including the title bar and border. A live DWM projection scales while the real window and WebView keep their size. Opening scales from 0.05 to 1 with ease-out; closing reverses it with ease-in. Studio motion speed settings apply; disabled or reduced motion skips the effect.

Saving and every close confirmation precede the reverse zoom. Cancelling a close keeps the window open. Dialogs retain shared zoom; existing local slide/fade effects retain their roles. Maintainers must read the contract and inspect current behavior, run the preflight, then modify and rerun checks. Native changes also require actual intermediate projection geometry, stable source-window size, handoff and cleanup validation; elapsed time alone is insufficient.
