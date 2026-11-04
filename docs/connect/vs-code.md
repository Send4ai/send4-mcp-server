# Connect VS Code

Back to the [list of assistants](../../README.md#connect).

## Before you start

A Client Admin must have turned on **Allow AI assistants** for your workspace, under
**Settings → Integrations → AI assistants**. See [permissions](../permissions.md).

## Connect

1. Open the Command Palette and run **MCP: Add Server**.
2. Choose **HTTP**, enter `https://mcp.send4.ai/mcp` and name it `send4`.
3. Use it from Copilot Chat in agent mode, and sign in to Send4 when asked.

Or add it to `.vscode/mcp.json`:

```json
{
  "servers": {
    "send4": { "type": "http", "url": "https://mcp.send4.ai/mcp" }
  }
}
```

The Send4 screen says you'll return to "an app on this computer". That app is VS Code.

VS Code's menus change often. If yours look different, see
[VS Code's guide to MCP servers](https://code.visualstudio.com/docs/copilot/customization/mcp-servers).

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow. Tick what the assistant may do, then select **Connect**.

If you leave a box unticked, the assistant can't do that. Before it launches a campaign, switches
a flow on or off, or invites someone, Send4 makes it show you a summary and wait for your yes.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside the
assistant. Its access ends immediately.
