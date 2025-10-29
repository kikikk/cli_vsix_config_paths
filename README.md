# cli_api_Local-location

各种CLI的api/mcp server/官方配置文档地址（精确到子选项）等文件 本地具体位置/详情/链接
claude code、gemini、codex、droid、


---

## 📋 MCP 服务器列表

| MCP | IDE | JSON 配置 | 说明 |
|:---|:---:|:---|:---|
| **[Claude code](https://docs.claude.com/en/docs/claude-code/settings)** | **api** | `"C:\Users\Administrator\.claude\settings.json"` | Mac: `/Users/Name/Docs`<br>Win: `C:\Users\Name\Docs` |
|  | **备注** | `{"mcpServers":{`<br>`"filesystem":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`filesystem",`<br>`"${workspace`<br>`Folder}"]}}}` | 支持 `${workspaceFolder}` |
| **[codex](https://developers.openai.com/codex/local-config/)** | **api** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"ghp_xxx"}}}}` | 🔑 [获取 Token](https://github.com/settings/tokens) |
|  | **备注** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"${env:`<br>`GITHUB_TOKEN}"}}}}` | 同上 |
| **[gemini](https://geminicli.com/docs/)** | **api** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"/path/`<br>`to/credentials.json"}}}}` | 🔐 [Google Cloud 凭据](https://console.cloud.google.com/) |
|  | **备注** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"${env:`<br>`GOOGLE_CREDENTIALS}"}}}}` | 同上 |
| **[droid](https://docs.factory.ai/cli/getting-started/overview)** | **api** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":`<br>`"your_api_key"}}}}` | 🔑 [Brave API](https://brave.com/search/api/) |
|  | **备注** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":"${env:`<br>`BRAVE_API_KEY}"}}}}` | 同上 |
| **[PostgreSQL](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres)** | **api** | `{"mcpServers":{`<br>`"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"postgresql://`<br>`user:pwd@localhost:`<br>`5432/db"],"env":{}}}}` | 格式: `postgresql://[user]:[pwd]@[host]:[port]/[db]` |
|  | **备注** | `{"mcpServers":{`<br>`"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"${env:DATABASE_`<br>`URL}"]}}}` | 同上 |
| **[Slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack)** | **api** | `{"mcpServers":{`<br>`"slack":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`slack"],`<br>`"env":{"SLACK_`<br>`BOT_TOKEN":`<br>`"xoxb-xxx",`<br>`"SLACK_TEAM_ID":`<br>`"T0123"}}}}` | 🤖 [创建 Slack App](https://api.slack.com/apps) |
|  | **备注** |  |  |
