# Troubleshooting

Back to the [README](../README.md).

## "Connecting AI assistants needs a plan, or a trial with a card on file"

Your workspace has no plan that includes assistants, or its trial has no card on file yet, or it
has ended. A Client Admin can set this up under **Settings → Plan & billing**.

## The assistant says it can't connect, or can't do anything

Ask a Client Admin to check **Settings → Integrations → AI assistants**. **Allow AI assistants**
must be on before anyone can connect.

## A tool you expected isn't there

An assistant is only told about the tools its connection can use. A tool is missing when:

- the workspace switch for that kind of change is off,
- you didn't tick it when you connected,
- your role can't use it (see [who can use what](permissions.md#who-can-use-what)), or
- your plan doesn't include it. For example, Starter has no campaigns.

Ask the assistant "What can you do in Send4?". It reads `get_context`, which lists what this
connection was granted, what it wasn't, and who can allow the rest. To tick something you left
out, disconnect the assistant and connect it again.

## The Send4 screen says I'll return to "an app on this computer"

That's normal for Claude Code, VS Code, Cursor and the terminal tools. They sign in through your
own computer. Only continue if you started the connection from that app yourself.

## The assistant asks me to confirm before it acts

That's on purpose. These steps always wait for your yes: launching a campaign, adding people to
one, switching a flow on or a live flow off, inviting someone, and texting a number you typed.

## It won't change my live flow

That's on purpose too. While a flow is off, nobody answers its customers, so a live flow is never
switched off or edited in place. Ask the assistant to duplicate it, change the copy and rehearse
it. Then switch the copy on and the original off.

## Requests are refused for a few minutes

Send4 limits how many requests one connection can make in a few minutes. The refusal says when to
try again.

## Everyone was disconnected

A Client Admin switched off **Allow AI assistants**, the plan changed, or the trial ended. Once
the workspace can use assistants again, each person connects again.

## My assistant can't sign in at all

Send4 accepts sign-in from the assistants in the [README](../README.md#connect), and from tools
that sign in through your own computer. Microsoft Copilot Studio, and assistants hosted on their
own web address, can't sign in yet. If you need one of them, email
[support@send4.ai](mailto:support@send4.ai).

## Still stuck?

[Open an issue](https://github.com/Send4-ai/mcp/issues/new/choose). Say which assistant you use,
which step failed, and copy the exact error text. Issues are public, so never paste access
tokens, passwords, or your customers' messages, names, numbers or addresses.
