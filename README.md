<p align="center"><img src="logo.png" width="120" height="120" alt="Build to Launch"></p>

# Build to Launch MCP

Connect your AI agent to 300+ methods and 100+ live tools.

Build to Launch MCP is a remote MCP server. It gives AI agents such as Claude, ChatGPT, Cursor and Codex 300+ methods, workflows and examples for building with AI, sorted into 10 jobs, plus 100+ live tools for keywords, SEO, trends and social data.

Ask your agent for a job in your own words. It opens the right item and works through it with you, one step at a time. Made by Jenny Ouyang, who writes the [Build to Launch](https://buildtolaunch.ai/) newsletter.

## Server facts

| Field | Value |
|---|---|
| URL | `https://mcp.buildtolaunch.ai` |
| Transport | Streamable HTTP (not SSE) |
| Sign-in | OAuth with dynamic client registration. Your app opens a browser page. No API key. |
| Registry name | `io.github.jenny-ouyang/build-to-launch-mcp` ([server.json](server.json)) |

Anyone can connect. Without a membership, you get the free items in full, and search lists only those items. A membership gives you the full library.

## Install

The fastest way: ask your agent to read `mcp.buildtolaunch.ai/install` and connect Build to Launch for you. The guide has steps for each app.

### Claude (claude.ai, Desktop, mobile)

Open [Connect to Claude](https://mcp.buildtolaunch.ai/claude-install) and follow the steps. A connector that you add on claude.ai also shows in Claude Desktop, the mobile app and Claude Code.

### Claude Code

```bash
claude mcp add --transport http buildtolaunch --scope user https://mcp.buildtolaunch.ai
```

Then type `/mcp` and choose Authenticate.

### Cursor

Add this entry to the `mcpServers` object in `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "buildtolaunch": { "url": "https://mcp.buildtolaunch.ai" } } }
```

### VS Code (GitHub Copilot)

Run "MCP: Open User Configuration" from the Command Palette and add this to the `servers` object:

```json
{ "servers": { "buildtolaunch": { "type": "http", "url": "https://mcp.buildtolaunch.ai" } } }
```

### Codex

```bash
codex mcp add buildtolaunch --url https://mcp.buildtolaunch.ai
```

### Gemini CLI

```bash
gemini mcp add --transport http --scope user buildtolaunch https://mcp.buildtolaunch.ai
```

### Cline

See [llms-install.md](llms-install.md).

## Sign in

1. Start the sign-in when your app asks (Connect, Authenticate, Allow or Sign in).
2. Type your email on the Build to Launch sign-in page. If you have a membership, use the email of your membership.
3. Open the sign-in link that arrives by email, in the same browser.
4. Click Authorize on the "Connect to ..." page.

## Tools

| Tool | What it does |
|---|---|
| `search_btl_resources` | Finds guides, prompts, workflows and live tools by keyword |
| `use_btl_resource` | Opens one item by its slug and works through it |
| `manage_feedback` | Asks Jenny for feedback on your work, and reads her answers |
| `manage_my_skill` | Adds, updates and deletes your own skills |
| `read_my_skills` | Reads and lists your own skills |
| `btl_canva_host` | Hosts a filled Canva kit page so Canva can import it (members) |

## First question

After you connect, ask: "Build to Launch, what can you do for me, and where should I start?"

## Links

- [Library](https://mcp.buildtolaunch.ai/library): the 300+ items, sorted into 10 jobs
- [Live tools](https://mcp.buildtolaunch.ai/buddies): the live research tools for keywords, SEO, trends and social data
- [Connect to Claude](https://mcp.buildtolaunch.ai/claude-install)
- [Build to Launch](https://buildtolaunch.ai/): the newsletter, the community and the tools

## About this repository

This repository holds the listing files for MCP directories: this README, `server.json`, `llms-install.md`, `glama.json` and the logo. The server runs as a hosted service at `mcp.buildtolaunch.ai`; its source is not in this repository.

## License

[MIT](LICENSE) for the files in this repository.
