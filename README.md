# cli_api_Local-location

各种CLI的api/mcp server/官方配置文档地址（精确到子选项）等文件 本地具体位置/详情/链接
claude code、gemini、codex、droid、


---

## 📋 MCP 服务器列表

| MCP | 更新 | IDE | JSON 配置 | 说明 |
|:---|:---:|:---:|:---|:---|
| **[Claude code](https://docs.claude.com/en/docs/claude-code/settings)** | `01-15` | **api** | `C:\Users\Administrator\AppData\Roaming\Claude\claude_desktop_config.json` | Mac: `/Users/Name/Docs`<br>Win: `C:\Users\Name\Docs` |
|  |  | **mcp servers** | `{"filesystem":{"command":"npx","args":["-y","@modelcontextprotocol/server-filesystem","C:\\Users\\Name\\Docs"],"disabled":false}}` | 路径用双反斜杠 `\\` |
|  |  | **备注** | `{"mcpServers":{"filesystem":{"command":"npx","args":["-y","@modelcontextprotocol/server-filesystem","${workspaceFolder}"]}}}` | 支持 `${workspaceFolder}` |
| **[GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/github)** | `01-15` | **Claude Desktop** | `{"mcpServers":{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"ghp_xxx"}}}}` | 🔑 [获取 Token](https://github.com/settings/tokens) |
|  |  | **Cline** | `{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"${env:GITHUB_TOKEN}"},"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"${env:GITHUB_TOKEN}"}}}}` | 同上 |
| **[Google Drive](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive)** | `01-10` | **Claude Desktop** | `{"mcpServers":{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"/path/to/credentials.json"}}}}` | 🔐 [Google Cloud 凭据](https://console.cloud.google.com/) |
|  |  | **Cline** | `{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"${env:GOOGLE_CREDENTIALS}"},"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"${env:GOOGLE_CREDENTIALS}"}}}}` | 同上 |
| **[Brave Search](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search)** | `01-12` | **Claude Desktop** | `{"mcpServers":{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"your_api_key"}}}}` | 🔑 [Brave API](https://brave.com/search/api/) |
|  |  | **Cline** | `{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"${env:BRAVE_API_KEY}"},"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"${env:BRAVE_API_KEY}"}}}}` | 同上 |
| **[PostgreSQL](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres)** | `01-14` | **Claude Desktop** | `{"mcpServers":{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","postgresql://user:pwd@localhost:5432/db"],"env":{}}}}` | 格式: `postgresql://[user]:[pwd]@[host]:[port]/[db]` |
|  |  | **Cline** | `{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","${env:DATABASE_URL}"],"disabled":false}}` | 🔒 用环境变量 |
|  |  | **Continue.dev** | `{"mcpServers":{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","${env:DATABASE_URL}"]}}}` | 同上 |
| **[Slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack)** | `01-08` | **Claude Desktop** | `{"mcpServers":{"slack":{"command":"npx","args":["-y","@modelcontextprotocol/server-slack"],"env":{"SLACK_BOT_TOKEN":"xoxb-xxx","SLACK_TEAM_ID":"T0123"}}}}` | 🤖 [创建 Slack App](https://api.slack.com/apps) |
|  |  | **Cline** | `{"slack":{"command":"npx","args":["-y","@modelcontextprotocol/server-slack"],"env":{"SLACK_BOT_TOKEN":"${env:SLACK_BOT_TOKEN}","SLACK_TEAM_ID":"${env:SLACK_TEAM_ID}"},"disabled":false}}` | 🔒 用环境变量 |
