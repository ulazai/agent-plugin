# UlazAI Media — agent plugin

Create private AI images from your coding agent or chat assistant with a linked [UlazAI](https://ulazai.com) account. Compare models, prepare a prompt, generate the image and drop the file into your project.

## What is inside
- `mcp.json` / `.mcp.json` — connection to the hosted MCP server `https://mcp.ulazai.com/mcp` (Streamable HTTP, OAuth 2.0; the client handles login).
- `.app.json` — the registered ChatGPT/Codex connection (Codex uses this instead of `.mcp.json`, so tools are never loaded twice).
- `skills/ulazai-images` — the safe generation flow: account → model → prepare → create → fetch.

## Tools (5)
`get_ulazai_account`, `search_ulazai_models`, `prepare_ulazai_image`, `create_ulazai_image`, `get_ulazai_generation`. Only `create_ulazai_image` consumes allowance, and only after the user confirms.

## Install
- **Claude Code:** `claude plugin marketplace add ulazai/agent-plugin`, then install `ulazai-media`. Or: `claude mcp add --transport http ulazai https://mcp.ulazai.com/mcp`.
- **Codex:** `codex plugin marketplace add ulazai/agent-plugin`.
- **Cursor / Agent Plugins clients:** install this repository as a plugin; `plugin.json` + `mcp.json` follow Agent Plugins 1.1.0.
- **Grok Build:** `grok plugin install https://github.com/ulazai/agent-plugin.git`.
- **Claude.ai / Desktop:** add `https://mcp.ulazai.com/mcp` as a custom connector.

## Network and data
The plugin only talks to `https://ulazai.com`. Generated images are private to your account. Privacy: https://ulazai.com/privacy/ · Terms: https://ulazai.com/terms/

## License
MIT for this plugin package. The UlazAI service itself is covered by its own terms.
