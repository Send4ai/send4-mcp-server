# Connect Claude

Back to the [list of assistants](../../README.md#supported-assistants).

## Before you start

AI assistants are on for your workspace unless a Client Admin has switched them off, under
**Settings → Integrations → AI assistants**. See [permissions](../permissions.md).

## Claude on the web and Claude Desktop

On Pro or Max:

1. Open **Customize → Connectors**, select **+ Add**, then **Add custom connector**.
2. Name it `Send4`, enter `https://mcp.send4.ai/mcp` and select **Continue**.
3. Sign in to Send4 when asked.

On Team or Enterprise, an owner adds it once under **Organization settings → Connectors**. Each
person then selects **Connect** under **Customize → Connectors** and signs in as themselves.

Claude's menus change often. If yours look different, see
[Anthropic's guide to custom connectors](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-MCP).

## Claude Code

```sh
claude mcp add --transport http send4 https://mcp.send4.ai/mcp
```

Then run `/mcp` inside Claude Code and sign in to Send4. The Send4 screen says you'll return to
"an app on this computer". That app is Claude Code.

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow, already ticked. Untick what Claude shouldn't do, then select **Connect**.

If you leave a box unticked, Claude can't do that. Before it launches a campaign, switches a flow
on or off, or invites someone, Send4 makes it show you a summary and wait for your yes. Whether
Claude asks before other changes depends on Claude's own settings.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside Claude.
Its access ends immediately.
