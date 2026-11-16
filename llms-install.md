# Install Build to Launch MCP

These steps are for an AI agent, such as Cline, that installs Build to Launch MCP for a person.

Build to Launch MCP is a remote server. There is nothing to download, build or run on the computer. There is no API key. The person signs in once in the browser with OAuth.

## Server facts

- URL: `https://mcp.buildtolaunch.ai`
- Transport: Streamable HTTP (not SSE)
- Sign-in: OAuth with dynamic client registration. The app opens a browser page.

## Cline

1. Open the MCP Servers panel in Cline and choose the Remote Servers tab.
2. Fill in the form:
   - Server Name: `buildtolaunch`
   - Server URL: `https://mcp.buildtolaunch.ai`
   - Transport Type: Streamable HTTP
3. Click Add Server.

If you can edit files, you can add the same server to `cline_mcp_settings.json` instead. Keep the other servers in the file:

```json
{
  "mcpServers": {
    "buildtolaunch": {
      "type": "streamableHttp",
      "url": "https://mcp.buildtolaunch.ai"
    }
  }
}
```

## Sign in

The person must do these steps. Tell them what to click, then wait.

1. When Cline shows that the server needs authentication, click Authenticate (or Connect).
2. Type the email on the Build to Launch sign-in page. A member uses the email of their membership.
3. Open the sign-in link that arrives by email, in the same browser.
4. Click Authorize on the "Connect to ..." page.

Never ask the person for a password or an API key. Sign-in happens only in the browser.

## Check

1. Make sure the tools `search_btl_resources` and `use_btl_resource` are available.
2. Call `search_btl_resources` with the query "prompt".
3. If it returns results, the install works. Tell the person to ask: "Build to Launch, what can you do for me, and where should I start?"

## Other apps

The full guide for Claude, Claude Code, ChatGPT, Codex, Cursor, VS Code, Gemini CLI and Windsurf is at `https://mcp.buildtolaunch.ai/install`.
