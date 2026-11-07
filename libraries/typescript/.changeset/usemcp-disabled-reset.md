---
"@mcp-use/client": patch
---

`useMcp` now clears the previous server's tools, resources, prompts, server info, capabilities and instructions when `enabled` turns false or `url` is cleared. Before, the hook closed the connection and reported `state: "discovering"` but kept returning the old server's data, so a UI kept rendering tools for a server it was no longer connected to.
