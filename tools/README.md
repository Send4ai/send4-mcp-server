# Tool definitions

There is one file per tool on the Send4 MCP server. Each file is exactly what the server sends a
connected assistant about that tool, its entry in `tools/list`:

- `name`, `title` and `description`
- `inputSchema`: the inputs it takes
- `annotations`: its safety hints, explained below
- `_meta`: for a few tools, the in-chat view they open

The server generates these files, and every update replaces them whole. Please don't edit them by
hand. If a description is wrong, [open an issue](https://github.com/send4ai/send4-mcp-server/issues/new/choose).

Which of these tools an assistant actually sees depends on three things: the workspace's switches,
what you ticked when you connected, and your role. See [docs/tools.md](../docs/tools.md) and
[docs/permissions.md](../docs/permissions.md).

## The safety hints

| Hint | When it's `true` |
| --- | --- |
| `readOnlyHint` | The tool changes nothing. |
| `destructiveHint` | It overwrites, removes or sends something that can't be taken back. |
| `idempotentHint` | Calling it twice with the same inputs changes nothing more. |
| `openWorldHint` | It reaches a person outside the workspace, by email or SMS. |

Assistants use these hints to decide what to ask you before calling a tool. Some steps always wait
for your yes regardless of the hints. Those are launching a campaign, adding people to one,
switching a flow on or a live flow off, inviting someone, and texting a number you typed. Before
any of them, Send4 gives the assistant a summary to show you.
