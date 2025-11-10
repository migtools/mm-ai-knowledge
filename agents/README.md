# Agents

This directory contains **generic agent configuration templates and examples** for autonomous task handling.

## Scope

**This directory is for educational templates and generic patterns.** For production-ready, domain-specific agents (e.g., OpenShift debugging, JIRA automation), see specialized repositories like [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Structure

- `specialized/` - Generic agent templates (code-reviewer, tester, documentation writer, etc.)
- `workflows/` - Multi-agent workflow configuration examples
- `templates/` - Reusable, generic agent templates

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
3. **Configuration**: Complete configuration file (template form)
4. **Usage Example**: How to use the agent
5. **Keep It Generic**: Avoid tight coupling to specific APIs, services, or organizations

### Examples of Appropriate Agents

✅ **Good (Generic Templates):**
- Code review agent template with common review patterns
- Test generator agent with generic testing principles
- Documentation writer agent with standard doc formats

❌ **Not Appropriate (Domain-Specific):**
- JIRA bug triage agent (better for ai-helpers)
- OpenShift cluster health monitor agent
- AWS deployment automation agent

## Best Practices

- **Single Responsibility**: Each agent should do one thing well
- **Clear Instructions**: Provide unambiguous directions
- **Error Handling**: Consider edge cases
- **Documentation**: Explain parameters and options
