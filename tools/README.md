# Tools

Custom tools, integrations, and extensions for AI development environments.

## Structure

- `mcp-servers/` - MCP (Model Context Protocol) server configurations
- `scripts/` - Utility scripts and automation tools
- `integrations/` - Third-party service integrations (GitHub, Jira, Slack, etc.)

## MCP Servers

MCP servers extend AI capabilities by providing additional context and functionality.

### Available MCP Servers

See the `mcp-servers/` directory for:
- Configuration files
- Setup instructions
- Usage examples

### Common MCP Integrations

- GitHub: Repository management, PR reviews
- Jira: Issue tracking, project management
- Filesystem: Enhanced file operations
- Database: Query and data access
- Web: Fetching and searching web content

## Scripts

Utility scripts that enhance AI workflows:

```bash
# Example structure
tools/scripts/
├── code-quality/
│   └── run-linters.sh
├── deployment/
│   └── deploy-to-staging.sh
└── testing/
    └── run-integration-tests.sh
```

## Integrations

Third-party service integrations that work with AI tools:

- API wrappers
- Webhook handlers
- OAuth configurations
- Service-specific commands

## Contributing Tools

When adding a tool:

1. **README**: Include setup and usage instructions
2. **Dependencies**: List all requirements
3. **Configuration**: Provide example configs
4. **Examples**: Show real-world usage
5. **Security**: Note any security considerations

## Installation Example

```bash
# MCP Server
cp tools/mcp-servers/github-config.json ~/.config/claude/mcp.json

# Script
cp tools/scripts/your-script.sh /usr/local/bin/
chmod +x /usr/local/bin/your-script.sh
```

## Security Notes

- Never commit API keys or tokens
- Use environment variables for secrets
- Document required permissions
- Include security best practices
