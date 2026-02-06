# Linear MCP Server Extension for Zed

> [!IMPORTANT]
> Linear has an [official MCP Server](https://linear.app/docs/mcp).
> It is a remote server and doesn't need to be installed. See the [config](#official-linear-mcp-server-configuration) below.
> You should use that one instead.

This extension integrates [(Unofficial) Linear MCP Server](https://github.com/odgrim/linear-mcp) as a context server for [Zed's](https://zed.dev) [Agent Panel.](https://zed.dev/docs/ai/overview)

Several were analyzed and this one worked the best in practice.

You'll need to grab a Linear access token for your account.

Visit: `https://linear.app/<your-org>/settings/account/security`

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

Linear has an official MCP and it's easy to customize and doesn't require an extension to help with the installation.

```json
"context_servers": {
  "mcp-server-linear": { // name can be whatever you want
    "url": "https://mcp.linear.app/mcp",
    "headers": { // optional, if you don't want to use the OAuth flow
      "Authorization": "Bearer <your linear token>"
    }
  }
}
```
