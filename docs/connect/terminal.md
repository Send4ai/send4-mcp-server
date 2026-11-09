# Connect from the terminal

Back to the [list of assistants](../../README.md#supported-assistants).

These tools connect to Send4 from your terminal. Each one opens your browser once so you can sign
in to Send4 and choose what it may do. The Send4 screen says you'll return to "an app on this
computer". That app is the tool you started.

## Before you start

AI assistants are on for your workspace unless a Client Admin has switched them off, under
**Settings → Integrations → AI assistants**. See [permissions](../permissions.md).

## opencode

Add this to `opencode.json`, then run `opencode mcp auth send4`:

```json
{
  "mcp": {
    "send4": { "type": "remote", "url": "https://mcp.send4.ai/mcp" }
  }
}
```

See [opencode's MCP documentation](https://opencode.ai/docs/mcp-servers/).

## Codex CLI

```sh
codex mcp add send4 --url https://mcp.send4.ai/mcp
codex mcp login send4
```

Check `codex mcp --help` if a flag is refused.

## Gemini CLI

Install Send4 as a Gemini CLI extension straight from this repository:

```sh
gemini extensions install https://github.com/send4ai/send4-mcp-server
```

Or add the server by hand:

```sh
gemini mcp add --transport http send4 https://mcp.send4.ai/mcp
```

Then run `/mcp auth send4` inside Gemini CLI. See
[Gemini CLI's MCP documentation](https://github.com/google-gemini/gemini-cli/blob/main/docs/tools/mcp-server.md).

## Claude Code

See [Connect Claude](claude.md#claude-code).

## Another tool

A tool should work if it connects to a remote MCP server over Streamable HTTP and signs in through
your browser. Give it `https://mcp.send4.ai/mcp`.

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow, already ticked. Untick what the assistant shouldn't do, then select **Connect**.

If you leave a box unticked, the assistant can't do that. Before it launches a campaign, switches
a flow on or off, or invites someone, Send4 makes it show you a summary and wait for your yes.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside the
assistant. Its access ends immediately.
