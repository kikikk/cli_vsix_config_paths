# cli_api_Local-location

各种CLI的api/mcp server/等文件 本地具体位置/详情
---

## 📋 MCP 服务器列表

| MCP | 更新 | IDE | JSON 配置 | 说明 |
|:---|:---:|:---:|:---|:---|
| **[Filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem)** | `01-15` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"filesystem":{"command":"npx","args":["-y","@modelcontextprotocol/server-filesystem","/path/to/directory"],"env":{}}}}</pre> | Mac: `/Users/Name/Docs` Win: `C:\Users\Name\Docs` |
|  |  | **Cline** | <pre lang="json">{"filesystem":{"command":"npx","args":["-y","@modelcontextprotocol/server-filesystem","C:\\Users\\Name\\Docs"],"disabled":false}}</pre> | 路径用双反斜杠 `\\` |
|  |  | **Continue.dev** | <pre lang="json">{"mcpServers":{"filesystem":{"command":"npx","args":["-y","@modelcontextprotocol/server-filesystem","${workspaceFolder}"]}}}</pre> | 支持 `${workspaceFolder}` |
| **[GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/github)** | `01-15` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"ghp_xxx"}}}}</pre> | 🔑 [获取 Token](https://github.com/settings/tokens) |
|  |  | **Cline** | <pre lang="json">{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"${env:GITHUB_TOKEN}"},"disabled":false}}</pre> | 🔒 用环境变量 |
|  |  | **Continue.dev** | <pre lang="json">{"mcpServers":{"github":{"command":"npx","args":["-y","@modelcontextprotocol/server-github"],"env":{"GITHUB_PERSONAL_ACCESS_TOKEN":"${env:GITHUB_TOKEN}"}}}}</pre> | 同上 |
| **[Google Drive](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive)** | `01-10` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"/path/to/credentials.json"}}}}</pre> | 🔐 [Google Cloud 凭据](https://console.cloud.google.com/) |
|  |  | **Cline** | <pre lang="json">{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"${env:GOOGLE_CREDENTIALS}"},"disabled":false}}</pre> | 用环境变量 |
|  |  | **Continue.dev** | <pre lang="json">{"mcpServers":{"gdrive":{"command":"npx","args":["-y","@modelcontextprotocol/server-gdrive"],"env":{"GOOGLE_APPLICATION_CREDENTIALS":"${env:GOOGLE_CREDENTIALS}"}}}}</pre> | 同上 |
| **[Brave Search](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search)** | `01-12` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"your_api_key"}}}}</pre> | 🔑 [Brave API](https://brave.com/search/api/) |
|  |  | **Cline** | <pre lang="json">{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"${env:BRAVE_API_KEY}"},"disabled":false}}</pre> | 用环境变量 |
|  |  | **Continue.dev** | <pre lang="json">{"mcpServers":{"brave-search":{"command":"npx","args":["-y","@modelcontextprotocol/server-brave-search"],"env":{"BRAVE_API_KEY":"${env:BRAVE_API_KEY}"}}}}</pre> | 同上 |
| **[PostgreSQL](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres)** | `01-14` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","postgresql://user:pwd@localhost:5432/db"],"env":{}}}}</pre> | 格式: `postgresql://[user]:[pwd]@[host]:[port]/[db]` |
|  |  | **Cline** | <pre lang="json">{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","${env:DATABASE_URL}"],"disabled":false}}</pre> | 🔒 强烈推荐环境变量 |
|  |  | **Continue.dev** | <pre lang="json">{"mcpServers":{"postgres":{"command":"npx","args":["-y","@modelcontextprotocol/server-postgres","${env:DATABASE_URL}"]}}}</pre> | 同上 |
| **[Slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack)** | `01-08` | **Claude Desktop** | <pre lang="json">{"mcpServers":{"slack":{"command":"npx","args":["-y","@modelcontextprotocol/server-slack"],"env":{"SLACK_BOT_TOKEN":"xoxb-xxx","SLACK_TEAM_ID":"T0123"}}}}</pre> | 🤖 [创建 Slack App](https://api.slack.com/apps) |
|  |  | **Cline** | <pre lang="json">{"slack":{"command":"npx","args":["-y","@modelcontextprotocol/server-slack"],"env":{"SLACK_BOT_TOKEN":"${env:SLACK_BOT_TOKEN}","SLACK_TEAM_ID":"${env:SLACK_TEAM_ID}"},"disabled":false}}</pre> | 用环境变量 |
