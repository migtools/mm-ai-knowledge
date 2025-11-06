# mm-ai-knowledge

A collaborative repository for sharing AI customizations, prompts, commands, agents, workflows, and configurations. This repo serves as a knowledge base for AI productivity tools and best practices.

## Table of Contents

- [Directory Structure](#directory-structure)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Usage Examples](#usage-examples)

## Directory Structure

```
mm-ai-knowledge/
├── prompts/                    # System prompts and prompt templates
│   ├── system/                # System-level prompts for AI behavior
│   ├── task-specific/         # Task-oriented prompts (coding, writing, analysis)
│   └── examples/              # Example prompts with use cases
│
├── commands/                   # Slash commands and CLI commands
│   ├── claude-code/           # Claude Code specific commands (.md format)
│   ├── cursor/                # Cursor IDE commands
│   └── general/               # General-purpose commands
│
├── agents/                     # Agent configurations and definitions
│   ├── specialized/           # Domain-specific agents (code-reviewer, tester, etc.)
│   ├── workflows/             # Multi-agent workflow configurations
│   └── templates/             # Agent templates for common use cases
│
├── workflows/                  # Multi-step workflow definitions
│   ├── development/           # Software development workflows
│   ├── content/               # Content creation workflows
│   └── automation/            # Task automation workflows
│
├── tools/                      # Custom tools and integrations
│   ├── mcp-servers/           # MCP (Model Context Protocol) server configs
│   ├── scripts/               # Utility scripts and tools
│   └── integrations/          # Third-party integrations (GitHub, Jira, etc.)
│
├── configs/                    # Configuration files
│   ├── claude-code/           # Claude Code settings
│   ├── api/                   # API configurations
│   └── templates/             # Configuration templates
│
├── examples/                   # Complete usage examples
│   ├── use-cases/             # Real-world use case demonstrations
│   ├── tutorials/             # Step-by-step tutorials
│   └── best-practices/        # Best practice guides
│
├── docs/                       # Documentation
│   ├── guides/                # How-to guides
│   ├── references/            # Reference documentation
│   └── tips/                  # Tips and tricks
│
└── templates/                  # Reusable templates
    ├── projects/              # Project templates
    ├── documents/             # Document templates
    └── code/                  # Code templates
```

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd mm-ai-knowledge
```

### 2. Browse by Category

Navigate to the relevant directory based on what you're looking for:

- **Need a prompt?** → Check `prompts/`
- **Want to add a command?** → Look in `commands/`
- **Looking for agent configs?** → Explore `agents/`
- **Need a workflow?** → Browse `workflows/`

### 3. Use the Templates

Each directory contains a `README.md` with:
- Description of the category
- How to use the contents
- Contribution guidelines specific to that category

## Contributing

We welcome contributions! Here's how to add your knowledge:

### Adding New Content

1. **Choose the Right Directory**: Place your content in the appropriate category
2. **Follow Naming Conventions**: Use descriptive, lowercase names with hyphens (e.g., `code-review-agent.md`)
3. **Include Documentation**: Add a header comment or README explaining:
   - What it does
   - How to use it
   - Any dependencies or requirements
   - Example usage

### Contribution Guidelines

- **Be Descriptive**: Use clear names and add comments
- **Test Your Content**: Ensure prompts/commands/configs work as expected
- **Add Examples**: Include usage examples when possible
- **Update Documentation**: If adding a new category, update this README

### File Naming Conventions

- Prompts: `{purpose}-prompt.md` (e.g., `code-review-prompt.md`)
- Commands: `{command-name}.md` (e.g., `refactor.md`)
- Agents: `{agent-type}-agent.{json|yaml|md}` (e.g., `test-runner-agent.yaml`)
- Workflows: `{workflow-name}-workflow.{json|yaml}` (e.g., `ci-cd-workflow.yaml`)

## Usage Examples

### Using a Prompt

```bash
# Copy a prompt from the prompts directory
cat prompts/task-specific/code-review-prompt.md

# Use it in your AI tool of choice
```

### Installing a Command (Claude Code)

```bash
# Create .claude/commands directory if it doesn't exist
mkdir -p .claude/commands

# Copy command to your project
cp commands/claude-code/refactor.md .claude/commands/

# Use in Claude Code
/refactor
```

### Setting Up an Agent

```bash
# Copy agent configuration
cp agents/specialized/code-reviewer-agent.yaml .claude/agents/

# Reference in your workflow
```

## Categories Explained

### Prompts
System prompts, task-specific prompts, and prompt engineering templates that can be used across different AI tools.

### Commands
Slash commands and CLI commands for tools like Claude Code, Cursor, and other AI-assisted development environments.

### Agents
Specialized agent configurations for autonomous task handling (code review, testing, documentation, etc.).

### Workflows
Multi-step processes that combine prompts, commands, and agents to accomplish complex tasks.

### Tools
Custom integrations, MCP servers, and utility scripts that extend AI capabilities.

### Configs
Configuration files for various AI tools and platforms.

### Examples
Real-world examples, tutorials, and use cases demonstrating how to combine different components.

### Templates
Reusable templates for projects, documents, and code that incorporate AI best practices.

## Best Practices

1. **Version Control**: Tag major versions of prompts/configs
2. **Documentation**: Always explain the "why" not just the "what"
3. **Testing**: Test your contributions before submitting
4. **Organization**: Keep related files together
5. **Privacy**: Never commit API keys, tokens, or sensitive data

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [MCP Protocol Specification](https://modelcontextprotocol.io/)
- [Prompt Engineering Guide](https://www.promptingguide.ai/)

## License

[Specify your license here]

## Maintainers

[Add maintainer information]

---

**Happy Sharing!** 🚀
