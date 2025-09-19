# Essential Claude Code for Development

## MCP Servers

```
claude mcp add --transport sse context7 https://mcp.context7.com/sse
claude mcp add serena -- uvx --from git+https://github.com/oraios/serena serena start-mcp-server --context ide-assistant --project $(pwd)
claude mcp add sequential-thinking -s local -- npx -y @modelcontextprotocol/server-sequential-thinking
claude mcp add playwright npx '@playwright/mcp@latest'
git clone https://github.com/modelcontextprotocol/superdesign-mcp-claude-code.git && cd superdesign-mcp-claude-code && npm install && npm run build && cd .. && claude mcp add superdesign "node"
  "$(pwd)/superdesign-mcp-claude-code/dist/index.js"
claude mcp add docling -- uvx --from docling-mcp docling-mcp-server
```

## Slash Commands

```
Always use:
- serena for semantic code retrieval and editing tools
- context7 for up to date documentation on third party code
- sequential thinking for any decision making
- playwright for testing frontend
Read the claude.md root file before you do anything.
#$ARGUMENTS

## Sub Agents


## Coming Later
- Superdesign for mock ups

