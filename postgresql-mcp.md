# PosreSQL MCP

Official repository: https://github.com/modelcontextprotocol/servers-archived/tree/main/src/postgres

Config example:
```json
{
  "mcpServers": {
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

Replace login, passwor, host, post and db_name with your values
