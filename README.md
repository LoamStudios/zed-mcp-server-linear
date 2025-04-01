# Linear MCP Server Extension for Zed

This extension integrates [Linear MCP Server](https://github.com/odgrim/linear-mcp) as a context server for
Zed's Assistant.

Several were analyzed and this one worked the best in practice.

You'll need to grab a Linear access token for your account.

https://linear.app/<your-org>/settings/account/security

```
"context_servers": {
    "mcp-server-linear": {
      "settings": {
        "linear_api_key": "<LINEAR_API_KEY>"
      }
    }
  },
```
