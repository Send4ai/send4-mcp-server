# Connect ChatGPT

Back to the [list of assistants](../../README.md#supported-assistants).

## Before you start

- AI assistants are on for your workspace unless a Client Admin has switched them off, under
  **Settings → Integrations → AI assistants**. See [permissions](../permissions.md).
- You need ChatGPT Business or Enterprise.

## Connect

On Business, an admin or owner adds it:

1. Open `chatgpt.com/plugins`, select the plus button, then **Add custom MCP server**.
2. Name it `Send4`, choose **Public endpoint** and enter `https://mcp.send4.ai/mcp`.
3. Select **I understand and want to continue**, then **Create as a plugin**.
4. Sign in to Send4 when asked.
5. In a new conversation, type `@` and choose Send4.

ChatGPT's menus change often. If yours look different, see
[OpenAI's guide to custom MCP servers](https://help.openai.com/en/articles/12584461-connecting-custom-mcp-servers-in-chatgpt).

## Choose what it may do

Send4 shows the account you're signed in to, and only the choices your role and your workspace
allow, already ticked. Untick what ChatGPT shouldn't do, then select **Connect**.

If you leave a box unticked, ChatGPT can't do that. Before it launches a campaign, switches a flow
on or off, or invites someone, Send4 makes it show you a summary and wait for your yes. Whether
ChatGPT asks before other changes depends on ChatGPT's own settings.

## Disconnect

Open **Settings → Integrations → AI assistants** in Send4 and select **Disconnect** beside ChatGPT.
Its access ends immediately.
