# The best MCP collection

## Links:

- [Context7](https://github.com/upstash/context7)
- [OpenAI GPT image generator](https://github.com/SureScaleAI/openai-gpt-image-mcp)
- [GitLab](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/gitlab)
- [GitHub](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/github)
- [Playwright](https://github.com/microsoft/playwright-mcp)
- [Supabase](https://supabase.com/docs/guides/getting-started/mcp)
- [GetStack](https://getstack.coderr.online)
- [PostgreSQL](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/postgres)

## Full json config:

```json
{
    "mcpServers": {
      "playwright": {
        "command": "npx",
        "args": [
          "@playwright/mcp@latest",
          "--vision"
        ]
      },
      "openai-gpt-image-mcp": {
        "command": "node",
        "args": [
          "/Users/olegstefanov/Base/Prog/libs/openai-gpt-image-mcp/dist/index.js" // path to the MCP server, need to be cloned from 
        ],
        "env": {
          "OPENAI_API_KEY": "..."
        }
      },
      "context7": {
        "command": "npx",
        "args": [
          "-y",
          "@upstash/context7-mcp@latest"
        ]
      },
      "supabase": {
        "command": "npx",
        "args": [
          "-y",
          "@supabase/mcp-server-supabase@latest",
          "--access-token",
          "sbp_..."
        ]
      },
      "getstack": {
        "command": "uvx",
        "args": [
          "getstack-mcp@latest"
        ],
        "description": "MCP server for getting templates"
      },
      "github": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-github"
        ],
        "env": {
          "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_..."
        }
      },
      "gitlab": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-gitlab"
        ],
        "env": {
          "GITLAB_PERSONAL_ACCESS_TOKEN": "<YOUR_TOKEN>",
          "GITLAB_API_URL": "https://gitlab.com/api/v4" // Optional, for self-hosted instances
        }
      },
      "postgres": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-postgres",
          "postgresql://login:password@host:port/db_name"
        ]
      }
    }
}
```
