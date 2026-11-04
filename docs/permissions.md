# Permissions

Back to the [README](../README.md).

Three things decide what a connected assistant may do, and each one can only narrow the one before:

1. **The workspace.** A Client Admin chooses which kinds of change assistants may make at all.
2. **The connection.** When you connect, you tick what this assistant may do.
3. **Your role.** An assistant never gets past what your own Send4 role allows.

The plan sets a limit too. Every paid plan includes assistants, and so does the 14-day trial once
a card is on file. Starter has no campaigns, so no assistant can create or launch one there.

## The workspace switches

In Send4, open **Settings → Integrations → AI assistants**. Under **Workspace access**:

| Switch | Default | What it allows |
| --- | --- | --- |
| **Allow AI assistants** | Off | Anyone in the workspace can connect an assistant to their own account. It can read flows, runs, campaigns and usage, and it changes nothing unless one of the switches below is also on. |
| **Allow conversation content** | Off | Connections may also read messages and the details a flow collected. These contain your customers' personal information. |

Under **What assistants may change**:

| Switch | Default | What it allows |
| --- | --- | --- |
| **Build and change flows** | Off | Create flows, change their cards, rehearse them and switch them on. A live flow is never changed in place, and switching a flow on needs your yes. |
| **Reply to customers and manage conversations** | Off | Reply to customers, text someone first, assign conversations, take over from the AI, and book, move or cancel meetings. Replies reach your customers as soon as they're sent. |
| **Create and launch campaigns** | Off | Create campaigns, add and tag leads, and launch, pause or cancel a campaign. Before a launch, the assistant must show you a summary. |
| **Invite and manage team members** | Off | Invite managers and agents, change their role and deactivate them. Nobody can be made an admin this way. |
| **Create email addresses** | Off | Create new email addresses on Send4. Assistants never see a mailbox password: you connect your own mailbox yourself, on the **Email addresses** page. |

When you turn off **Allow AI assistants** and select **Switch off**, every assistant in the
workspace is disconnected at once. Nobody can connect one until an admin switches it on again.

## What you tick when you connect

The Send4 sign-in screen shows the account you're signed in to, and only the choices your role
and your workspace allow:

| Choice | What the assistant may then do |
| --- | --- |
| **Read flows, runs, campaigns and usage** | See your flows, how their cards are configured, why a run stopped, your campaigns and analytics, and how much of your plan you've used. Every connection has this. |
| **Read conversation messages** | See what your customers and the AI said to each other, including the details a flow collected and your leads' names. |
| **Build and change flows** | Create flows, change their cards, rehearse them and switch them on. It can also leave suggested wording on a card for you to accept. |
| **Create and launch campaigns** | Create campaigns, add and tag leads, and launch, pause or cancel a campaign. Launching sends messages to your customers and costs money, so the assistant must show you a summary first. |
| **Reply to customers and manage conversations** | Reply to customers, start conversations, assign them, take over from the AI, and book, move or cancel meetings. |
| **Invite and manage team members** | Invite people to the workspace as managers or agents, change their role, and deactivate them. |
| **Create email addresses** | Create new email addresses for the workspace on Send4. |

To change what you ticked, disconnect the assistant and connect it again.

## Who can use what

| Permission | Client Admin | Client Manager | Client Agent |
| --- | --- | --- | --- |
| Read: conversations, leads, meetings, team, numbers, performance, message usage | Yes | Yes | Yes |
| Read: flows, runs, drop-off, card types, templates, personas | Yes | No | Yes |
| Read: plan usage and campaigns | Yes | No | No |
| Read conversation messages | Yes | Yes | Yes |
| Build and change flows | Yes | No | No |
| Create and launch campaigns | Yes | No | No |
| Reply to customers and manage conversations | Yes | Yes | Yes |
| Invite and manage team members | Yes | No | No |
| Create email addresses | Yes | No | No |

[docs/tools.md](tools.md) names every tool under each permission.

## Before you allow conversation content

- What an assistant reads goes to the company behind it, under the person's own account with them.
  Check their terms first.
- Customers write the messages an assistant reads, and a message could try to give the assistant
  instructions. Don't let an assistant that reads conversations also manage your team.
