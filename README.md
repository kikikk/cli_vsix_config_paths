# cli_api_Local-location

各种CLI/插件的api/mcp server/官方配置文档地址（精确到子选项）等文件 本地具体位置/详情/链接
claude code、gemini、codex、droid、


---

## 📋 MCP 服务器列表

| IDE | MCP | JSON 配置 | 说明 |
|:---|:---:|:---|:---|
| **[Claude code](https://docs.claude.com/en/docs/claude-code/settings)** | **api** | `"C:\Users\Administrator\.claude\settings.json"  ` | Mac: `/Users/Name/Docs`<br>Win: `C:\Users\Name\Docs` |
|  | **mcp server** | ` "C:\Users\ａ\AppData\Roaming\Claude\claude_desktop_config.json"  "C:\Users\ａ\.claude.json"` | 支持 `${workspaceFolder}` |
| **[codex](https://developers.openai.com/codex/local-config/)** | **api** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"ghp_xxx"}}}}` | 🔑 [获取 Token](https://github.com/settings/tokens) |
|  | **备注** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"${env:`<br>`GITHUB_TOKEN}"}}}}` | 同上 |
| **[gemini](https://geminicli.com/docs/)** | **api** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"/path/`<br>`to/credentials.json"}}}}` | 🔐 [Google Cloud 凭据](https://console.cloud.google.com/) |
|  | **备注** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"${env:`<br>`GOOGLE_CREDENTIALS}"}}}}` | 同上 |
| **[droid](https://docs.factory.ai/cli/getting-started/overview)** | **api** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":`<br>`"your_api_key"}}}}` | 🔑 [Brave API](https://brave.com/search/api/) |
|  | **备注** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":"${env:`<br>`BRAVE_API_KEY}"}}}}` | 同上 |
| **[augment](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres)** | **api** | `{"mcpServers":{`<br>`"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"postgresql://`<br>`user:pwd@localhost:`<br>`5432/db"],"env":{}}}}` | 格式: `postgresql://[user]:[pwd]@[host]:[port]/[db]` |
|  | **mcp server** | `"C:\Users\ａ\AppData\Roaming\Code\User\globalStorage\augment.vscode-augment\augment-global-state\mcpServers.json"` | 同上 |
| **[Antigravity](https://github.com/modelcontextprotocol/servers/tree/main/src/slack)** | **mcp** | `"C:\Users\ａ\.gemini\antigravity\mcp_config.json"` | 🤖 [创建 Slack App](https://api.slack.com/apps) |
|  | **备注** |  |  |
