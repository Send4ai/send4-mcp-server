# Connect Le Chat

Back to the [list of assistants](../../README.md#supported-assistants).

## Before you start

A Client Admin must have turned on **Allow AI assistants** for your workspace, under
**Settings → Integrations → AI assistants**. See [permissions](../permissions.md).

## Connect

1. In Le Chat, open **Intelligence → Connectors** and select **Add Connector**.
2. On the **Custom MCP Connector** tab, name it `Send4` and enter `https://mcp.send4.ai/mcp`.
3. Select **Connect** and sign in to Send4.

On Team and Enterprise, an admin adds the connector.

Le Chat's menus change often. If yours look different, see
[Mistral's guide to MCP connectors](https://docs.mistral.ai/vibe/work/connectors/mcp-connectors).

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow. Tick what the assistant may do, then select **Connect**.

If you leave a box unticked, the assistant can't do that. Before it launches a campaign, switches
a flow on or off, or invites someone, Send4 makes it show you a summary and wait for your yes.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside the
assistant. Its access ends immediately.
