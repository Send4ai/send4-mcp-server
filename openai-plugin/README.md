# Send4 plugin for ChatGPT and Codex

The package submitted to OpenAI's plugin directory, which ChatGPT and Codex share. It connects
one remote MCP server, `https://mcp.send4.ai/mcp`, signed in with OAuth through dynamic client
registration. It carries no client ID and no secret.

| File | What it is |
|---|---|
| `plugin.json` | The listing: name, short and long description, links, prompts, colour, icons |
| `mcp.json` | The server and how to sign in (`streamable-http`, OAuth, `dcr`) |
| `assets/logo.svg`, `assets/icon.svg` | The Send4 mark (square, 48×48 view box). `icon.svg` is Codex's composer icon |

## Build the ZIP

From this folder, with the two manifests at the root of the archive:

```bash
zip -r -X ../send4-openai-plugin.zip plugin.json mcp.json assets
```

Upload it at [platform.openai.com/plugins](https://platform.openai.com/plugins) under the
verified developer identity. The review material (test cases, reviewer notes, release notes)
is entered in the portal, not in the package.

## Limits OpenAI checks

- `displayName` and `shortDescription`: 30 characters each. `longDescription`: 4,000.
- Icon paths start with `./` and stay under `./assets/`. Icons are square, at least 48×48 px.
- No lifecycle hooks, no `apps` / `.app.json`, one MCP server per plugin.
