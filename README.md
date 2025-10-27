# cli_api_Local-location

各种CLI的api/mcp server/官方配置文档地址（精确到子选项）等文件 本地具体位置/详情/链接
claude code、gemini、codex、droid、


---

## 📋 MCP 服务器列表

| MCP | 更新 | IDE | JSON 配置 | 说明 |
|:---|:---:|:---:|:---|:---|
| **[Claude code](https://docs.claude.com/en/docs/claude-code/settings)** | `01-15` | **api** | `"C:\Users\Administrator\.claude\settings.json"` | Mac: `/Users/Name/Docs`<br>Win: `C:\Users\Name\Docs` |
|  |  | **mcp servers** | `"C:\Users\Administrator\AppData\Roaming\Claude\claude_desktop_config.json"` | 路径用双反斜杠 `\\` |
|  |  | **备注** | `{"mcpServers":{`<br>`"filesystem":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`filesystem",`<br>`"${workspace`<br>`Folder}"]}}}` | 支持 `${workspaceFolder}` |
| **[codex](https://github.com/modelcontextprotocol/servers/tree/main/src/github)** | `01-15` | **Claude Desktop** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"ghp_xxx"}}}}` | 🔑 [获取 Token](https://github.com/settings/tokens) |
|  |  | **Cline** | `{"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"${env:`<br>`GITHUB_TOKEN}"},`<br>`"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{`<br>`"github":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`github"],`<br>`"env":{"GITHUB_`<br>`PERSONAL_ACCESS_`<br>`TOKEN":"${env:`<br>`GITHUB_TOKEN}"}}}}` | 同上 |
| **[gemini](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive)** | `01-10` | **Claude Desktop** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"/path/`<br>`to/credentials.json"}}}}` | 🔐 [Google Cloud 凭据](https://console.cloud.google.com/) |
|  |  | **Cline** | `{"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"${env:`<br>`GOOGLE_CREDENTIALS}"},`<br>`"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{`<br>`"gdrive":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`gdrive"],`<br>`"env":{"GOOGLE_`<br>`APPLICATION_`<br>`CREDENTIALS":"${env:`<br>`GOOGLE_CREDENTIALS}"}}}}` | 同上 |
| **[droid](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search)** | `01-12` | **Claude Desktop** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":`<br>`"your_api_key"}}}}` | 🔑 [Brave API](https://brave.com/search/api/) |
|  |  | **Cline** | `{"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":"${env:`<br>`BRAVE_API_KEY}"},`<br>`"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{`<br>`"brave-search":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`brave-search"],`<br>`"env":{"BRAVE_`<br>`API_KEY":"${env:`<br>`BRAVE_API_KEY}"}}}}` | 同上 |
| **[PostgreSQL](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres)** | `01-14` | **Claude Desktop** | `{"mcpServers":{`<br>`"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"postgresql://`<br>`user:pwd@localhost:`<br>`5432/db"],"env":{}}}}` | 格式: `postgresql://[user]:[pwd]@[host]:[port]/[db]` |
|  |  | **Cline** | `{"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"${env:DATABASE_`<br>`URL}"],`<br>`"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{`<br>`"postgres":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`postgres",`<br>`"${env:DATABASE_`<br>`URL}"]}}}` | 同上 |
| **[Slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack)** | `01-08` | **Claude Desktop** | `{"mcpServers":{`<br>`"slack":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`slack"],`<br>`"env":{"SLACK_`<br>`BOT_TOKEN":`<br>`"xoxb-xxx",`<br>`"SLACK_TEAM_ID":`<br>`"T0123"}}}}` | 🤖 [创建 Slack App](https://api.slack.com/apps) |
|  |  | **Cline** | `{"slack":{`<br>`"command":"npx",`<br>`"args":["-y",`<br>`"@modelcontext`<br>`protocol/server-`<br>`slack"],`<br>`"env":{"SLACK_`<br>`BOT_TOKEN":"${env:`<br>`SLACK_BOT_TOKEN}",`<br>`"SLACK_TEAM_ID":`<br>`"${env:SLACK_`<br>`TEAM_ID}"},`<br>`"disabled":false}}` | 🔒 用环境变量 |
