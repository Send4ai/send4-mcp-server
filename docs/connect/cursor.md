# Connect Cursor

Back to the [list of assistants](../../README.md#supported-assistants).

## Before you start

A Client Admin must have turned on **Allow AI assistants** for your workspace, under
**Settings → Integrations → AI assistants**. See [permissions](../permissions.md).

## Connect

**One click:** [Add Send4 to Cursor](https://cursor.com/en/install-mcp?name=Send4&config=eyJ1cmwiOiJodHRwczovL21jcC5zZW5kNC5haS9tY3AifQ==), then sign in to Send4 when
Cursor asks.

**By hand:**

1. Add Send4 to `~/.cursor/mcp.json`:

   ```json
   {
     "mcpServers": {
       "send4": { "url": "https://mcp.send4.ai/mcp" }
     }
   }
   ```

2. In Cursor's MCP settings, select **Connect** beside Send4 and sign in to Send4.

The Send4 screen says you'll return to "an app on this computer". That app is Cursor.

Cursor's menus change often. If yours look different, see
[Cursor's MCP documentation](https://cursor.com/docs/context/mcp).

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow. Tick what the assistant may do, then select **Connect**.

If you leave a box unticked, the assistant can't do that. Before it launches a campaign, switches
a flow on or off, or invites someone, Send4 makes it show you a summary and wait for your yes.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside the
assistant. Its access ends immediately.
