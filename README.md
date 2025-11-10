# mm-ai-knowledge

A collaborative repository for sharing **general-purpose** AI customizations, prompts, commands, agents, workflows, and configurations. This repo serves as a generic knowledge base for AI productivity tools and best practices **across various domains and use cases**.

## Scope and Purpose

This repository focuses on **generic, reusable AI patterns** that can be applied across different projects, domains, and organizations. It serves as a learning resource and template library for AI-assisted development workflows.

### When to Use This Repository

Use `mm-ai-knowledge` when you need:
- Generic prompt templates for common tasks (code review, documentation, testing)
- General-purpose AI agent configurations
- Cross-platform command examples
- Educational resources about AI tools and best practices
- Reusable workflow patterns applicable to any project
- Tool-agnostic AI integration examples

### Related Projects

**For OpenShift-specific development automation**, see [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers):
- Production-ready Claude Code plugins for OpenShift workflows
- JIRA integration for OpenShift bug tracking
- CI/CD automation for OpenShift testing (Sippy, Gangway, Prow)
- OLM (Operator Lifecycle Manager) commands
- Must-gather analysis tools
- OpenShift-specific git workflows and deployment automation

**Key Difference**: While `mm-ai-knowledge` provides generic templates and learning resources, `ai-helpers` delivers ready-to-use, OpenShift-focused automation plugins.

## Table of Contents

- [Scope and Purpose](#scope-and-purpose)
- [Directory Structure](#directory-structure)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Usage Examples](#usage-examples)
- [Avoiding Overlap with Specialized Repositories](#avoiding-overlap-with-specialized-repositories)

**📖 For detailed scope clarification, see [SCOPE.md](SCOPE.md)**

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
├── templates/                  # Reusable templates
│   ├── projects/              # Project templates
│   ├── documents/             # Document templates
│   └── code/                  # Code templates
│
└── example-ai-projects/        # Links to exemplary AI projects and implementations
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

We welcome contributions! **Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [SCOPE.md](SCOPE.md) before contributing** to ensure your content fits this repository's generic, educational focus.

### Quick Guidelines

1. **Keep It Generic**: Contributions should be adaptable across domains
2. **Focus on Education**: Provide templates and examples, not production code
3. **Avoid Tight Coupling**: Don't integrate with specific APIs or services
4. **Follow Conventions**: Use established naming patterns and structure
5. **Document Thoroughly**: Explain what, why, and how

### Adding New Content

1. **Choose the Right Directory**: Place your content in the appropriate category
2. **Follow Naming Conventions**: Use descriptive, lowercase names with hyphens (e.g., `code-review-prompt.md`)
3. **Include Documentation**: Add clear explanations of:
   - What it does and why
   - How to use and customize it
   - Prerequisites or dependencies
   - Example usage with adaptable patterns

### Before Contributing

- ✅ Is it generic and reusable across domains?
- ✅ Is it educational or a template?
- ✅ Can it be easily adapted to different use cases?
- ❌ Does it integrate with specific APIs? → Consider domain-specific repos
- ❌ Is it production-ready tooling? → See [ai-helpers](https://github.com/openshift-eng/ai-helpers) or create domain-specific repo

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
Generic slash commands and CLI command examples for tools like Claude Code, Cursor, and other AI-assisted development environments. For OpenShift-specific commands, see [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

### Agents
Generic agent configuration templates for autonomous task handling (code review, testing, documentation, etc.). For production-ready OpenShift agents, see [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

### Workflows
Multi-step processes that combine prompts, commands, and agents to accomplish complex tasks.

### Tools
Generic custom integrations, MCP server examples, and utility scripts that extend AI capabilities. For OpenShift-specific tools, see [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

### Configs
Configuration files for various AI tools and platforms.

### Examples
Real-world examples, tutorials, and use cases demonstrating how to combine different components.

### Templates
Reusable templates for projects, documents, and code that incorporate AI best practices.

### Example AI Projects
Curated links to exemplary open-source AI projects, implementations, and real-world examples that demonstrate best practices and innovative approaches.

## Best Practices

1. **Version Control**: Tag major versions of prompts/configs
2. **Documentation**: Always explain the "why" not just the "what"
3. **Testing**: Test your contributions before submitting
4. **Organization**: Keep related files together
5. **Privacy**: Never commit API keys, tokens, or sensitive data

## Avoiding Overlap with Specialized Repositories

This repository intentionally focuses on **generic, educational, and template-based** content. Avoid adding:

- **Organization-specific workflows** (e.g., OpenShift JIRA processes, specific CI/CD pipelines)
- **Production-ready plugins** for specific platforms (contribute those to focused repos like [ai-helpers](https://github.com/openshift-eng/ai-helpers))
- **Domain-specific automation** (e.g., Kubernetes operators, cloud provider CLIs)
- **Internal tooling** that's tied to specific organizations or projects

### Content Guidelines

**✅ Good for mm-ai-knowledge:**
- Generic code review prompt templates
- Example agent configurations for common tasks
- Documentation on using AI tools effectively
- Reusable workflow patterns (e.g., "PR review workflow structure")
- Educational examples of MCP server integration

**❌ Better suited for ai-helpers or similar:**
- `/jira:solve` command that integrates with JIRA API
- `/ci:trigger-periodic` for OpenShift CI
- `/olm:install` for OLM-specific operations
- Production must-gather analysis scripts

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [MCP Protocol Specification](https://modelcontextprotocol.io/)
- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [OpenShift AI Helpers](https://github.com/openshift-eng/ai-helpers) - OpenShift-specific plugins

## License

[Specify your license here]

## Maintainers

[Add maintainer information]

---

**Happy Sharing!** 🚀
