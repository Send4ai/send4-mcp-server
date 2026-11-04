# Security

## Reporting a problem

Please don't report a security problem in a public issue. Report it privately instead:

- select **Report a vulnerability** on this repository's **Security** tab, or
- email [support@send4.ai](mailto:support@send4.ai) with "Security" in the subject.

Say what you found, how to reproduce it, and which address, screen or tool it affects. Don't
include real customer data. If you came across any, say so, and don't keep a copy.

## What's in scope

- The MCP server at `https://mcp.send4.ai/mcp`.
- The Send4 sign-in and consent screens an assistant opens on `app.send4.ai`.
- Anything that lets one connection, person or workspace reach data or actions it shouldn't.

Out of scope: load or denial-of-service testing, social engineering, spam, and problems in an
assistant's own product. Report those to the company that makes the assistant.

## Testing

Test only in a workspace you own. Don't read, change or delete anyone else's data.

Send4 sends real SMS and email. A flow, campaign or conversation tool can message real people, so
only use phone numbers and addresses that are yours.
