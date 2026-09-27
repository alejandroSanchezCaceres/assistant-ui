---
"@assistant-ui/react-ag-ui": patch
---

fix(react-ag-ui): keep a mid-run snapshot from splitting the turn and dropping its interrupt

- leave `MESSAGES_SNAPSHOT` records attributed to a subagent run (`subagentRunId`) out of the thread instead of rendering them as parent-agent messages
- keep a snapshot that arrives mid-run from repeating tool calls the running turn already renders, which also keeps a pending interrupt on the message holding the gated call
