# Send4 MCP server

Connect your own assistant, such as Claude, ChatGPT, Grok, Cursor or VS Code, to your
[Send4](https://send4.ai) workspace. Then ask it about your flows, campaigns, conversations and
usage in your own words. If your workspace allows it, the assistant can also make changes for you.

```
https://mcp.send4.ai/mcp
```

Send4 runs the server, so there is nothing to install. This repository holds the setup guides,
the list of tools, and the place to report a problem. The server's code isn't here.

## What you can ask

- "What does my website form flow do?"
- "Why did yesterday's conversation from the quote form stop?"
- "Which flow lost the most people this week?"
- "How much of my plan have we used this month?"
- "Build a draft flow that asks a new lead for their address and books a site visit."
- "Pause the spring campaign."

The last two need a permission your admin turns on. More in [examples/prompts.md](examples/prompts.md).

## Before you connect

1. **A plan that includes it.** Every paid plan does, and so does the 14-day trial once a card
   is on file. Starter has no campaigns, so campaign tools aren't offered there.
2. **A Client Admin switches it on.** In Send4, open **Settings → Integrations → AI assistants**
   and turn on **Allow AI assistants** under **Workspace access**. On its own, that lets assistants
   read and change nothing. Each kind of change is a separate switch, all off to begin with. See
   [docs/permissions.md](docs/permissions.md).
3. **You sign in as yourself.** Each person connects with their own Send4 login. An assistant can
   only do what that person's role allows, and only what they ticked when they connected.

## Connect

| Assistant | Guide |
| --- | --- |
| Claude (claude.ai, Claude Desktop, Claude Code) | [docs/connect/claude.md](docs/connect/claude.md) |
| ChatGPT | [docs/connect/chatgpt.md](docs/connect/chatgpt.md) |
| Grok | [docs/connect/grok.md](docs/connect/grok.md) |
| VS Code (GitHub Copilot) | [docs/connect/vs-code.md](docs/connect/vs-code.md) |
| Cursor | [docs/connect/cursor.md](docs/connect/cursor.md) |
| Le Chat (Mistral) | [docs/connect/le-chat.md](docs/connect/le-chat.md) |
| Perplexity | [docs/connect/perplexity.md](docs/connect/perplexity.md) |
| opencode, Codex CLI, Gemini CLI | [docs/connect/terminal.md](docs/connect/terminal.md) |

Another client should work too if it connects to a remote MCP server over Streamable HTTP and
signs in through your browser (OAuth with dynamic client registration). Give it the address above.

## What an assistant can do

An assistant is only told about the tools this connection can use.
[docs/tools.md](docs/tools.md) lists all of them, grouped by the permission that allows each one.

| Permission | What it allows |
| --- | --- |
| **Read flows, runs, campaigns and usage** | Every connection has this. It reads your flows, runs, campaigns, analytics and plan usage, and changes nothing. Phone numbers and email addresses are masked. |
| **Read conversation messages** | What customers and the AI said to each other, and the details a flow collected. |
| **Build and change flows** | Create flows, change their cards, rehearse them and switch them on. |
| **Create and launch campaigns** | Create campaigns, add and tag leads, and launch, pause or cancel a campaign. |
| **Reply to customers and manage conversations** | Reply, text someone first, assign, take over from the AI, and book, move or cancel meetings. |
| **Invite and manage team members** | Invite managers and agents, change their role, and deactivate them. |
| **Create email addresses** | Create new email addresses for the workspace on Send4. |

## How you stay in control

- **Your admin sets the limits, and you choose within them.** The workspace switches decide what
  any assistant may do. On the Send4 sign-in screen, you then tick what this one may do.
- **The big steps wait for your yes.** These are launching a campaign, adding people to one,
  switching a flow on or a live flow off, inviting someone, and texting a number you typed. Before
  any of them, Send4 gives the assistant a summary to show you. After your yes, only what that
  summary described runs.
- **A live flow is never edited in place.** The assistant changes a copy and rehearses it, then
  you switch the copy over.
- **No passwords in the chat.** No tool takes a mailbox password. You connect your own mailbox
  yourself, in Send4.
- **Every change is recorded.** Changes appear in your **Audit log**, marked as made through an
  AI assistant.
- **Switching off takes effect immediately.** Turning off **Allow AI assistants** disconnects
  everyone in the workspace. You can disconnect your own assistant at any time under
  **Settings → Integrations → AI assistants**.

Customers write the messages an assistant reads, and a message could try to give the assistant
instructions. Don't let an assistant that reads conversations also manage your team.

What an assistant reads goes to the company behind it, under your own account with them. Check
their terms before you allow conversation content.

## Help

- **Something not working?** Read [docs/troubleshooting.md](docs/troubleshooting.md), then
  [open an issue](https://github.com/Send4-ai/mcp/issues/new/choose). Issues are public: never
  paste access tokens, passwords, or your customers' messages, names, numbers or addresses.
- **Account, plan or workspace questions:** [support@send4.ai](mailto:support@send4.ai)
- **A security problem:** report it privately, as [SECURITY.md](SECURITY.md) describes.
- **Help centre:** [send4.ai/support/ai-assistant-tools](https://send4.ai/support/ai-assistant-tools/)

## Licence

The guides in this repository are [MIT licensed](LICENSE). Send4 itself is a commercial service,
used under its [terms](https://send4.ai/terms/).
