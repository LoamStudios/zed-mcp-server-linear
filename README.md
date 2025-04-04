# Linear MCP Server Extension for Zed

> [!IMPORTANT]
> Linear has [released](https://linear.app/changelog/2025-05-01-mcp) an official MCP Server.
> It is a remote server and doesn't need to be installed. See the [config](#official-linear-mcp-server-configuration) below.

This extension integrates [(Unofficial) Linear MCP Server](https://github.com/odgrim/linear-mcp) as a context server for [Zed's](https://zed.dev) [Agent Panel.](https://zed.dev/docs/ai/overview)

Several were analyzed and this one worked the best in practice.

You'll need to grab a Linear access token for your account.

https://linear.app/<your-org>/settings/account/security

```json
"context_servers": {
  "mcp-server-linear": {
    "settings": {
      "linear_api_key": "<LINEAR_API_KEY>"
    }
  }
}
```

## Official Linear MCP Server Configuration

The config in the announcement blog post is incorrect.
Use the following config instead.

```json
"context_servers": {
  "mcp-server-linear": { // name can be whatever you want
    "command": {
      "path": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.linear.app/sse"
      ]
    }
  }
}
```
