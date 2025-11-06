# Agents

This directory contains agent configurations and definitions for autonomous task handling.

## Structure

- `specialized/` - Domain-specific agents (code-reviewer, tester, documentation writer, etc.)
- `workflows/` - Multi-agent workflow configurations
- `templates/` - Reusable agent templates

## What is an Agent?

An agent is a specialized AI configuration designed to autonomously handle specific tasks. Agents can:
- Review code
- Run tests
- Generate documentation
- Analyze performance
- And much more

## Agent Configuration Format

Agents can be defined in various formats (JSON, YAML, Markdown) depending on the tool.

### Example Agent (YAML)

```yaml
name: code-reviewer
description: Reviews code for best practices, bugs, and improvements
capabilities:
  - code_analysis
  - security_review
  - performance_optimization
triggers:
  - on_pull_request
  - on_commit
instructions: |
  Review the code changes and provide:
  1. Security concerns
  2. Performance issues
  3. Code quality improvements
  4. Best practice violations
output_format: markdown
```

## Using Agents

Agents are typically referenced in:
- Claude Code workflows
- CI/CD pipelines
- Development automation tools
- Code review processes

## Contributing an Agent

Include:
1. **Clear Name**: Descriptive agent name
2. **Purpose**: What the agent does
3. **Configuration**: Complete configuration file
4. **Usage Example**: How to use the agent
5. **Dependencies**: Any required tools or APIs

## Best Practices

- **Single Responsibility**: Each agent should do one thing well
- **Clear Instructions**: Provide unambiguous directions
- **Error Handling**: Consider edge cases
- **Documentation**: Explain parameters and options
