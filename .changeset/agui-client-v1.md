---
"@assistant-ui/react-ag-ui": patch
---

feat(react-ag-ui): move to `@ag-ui/client` 1.0

- depend on `@ag-ui/client` `^1.0.0`; the client now expands `TEXT_MESSAGE_CHUNK` / `TOOL_CALL_CHUNK` and upgrades `THINKING_*` to `REASONING_*` before subscribers see them, so the adapter drops its handlers for those retired events
