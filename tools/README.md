# Tools

**Generic examples** of custom tools, integrations, and extensions for AI development environments.

## Scope

**This directory is for educational examples and generic patterns.** For production-ready, domain-specific tools (e.g., OpenShift CI integration, JIRA plugins, must-gather analyzers), see specialized repositories like [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Structure

- `mcp-servers/` - MCP (Model Context Protocol) server configuration examples
- `scripts/` - Generic utility script templates
- `integrations/` - Example integration patterns (not production implementations)

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

1. **Keep It Generic**: Focus on patterns and examples, not production implementations
2. **README**: Include setup and usage instructions
3. **Dependencies**: List all requirements
4. **Configuration**: Provide example configs (with placeholders, not real credentials)
5. **Examples**: Show conceptual usage patterns
6. **Security**: Note any security considerations

### Examples of Appropriate Content

✅ **Good (Generic Examples):**
- Example MCP server configuration structure
- Template for creating a custom GitHub integration
- Pattern for webhook handler implementation

❌ **Not Appropriate (Production Tools):**
- Complete JIRA MCP server (better for ai-helpers)
- Sippy API integration script
- Gangway job trigger implementation

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
