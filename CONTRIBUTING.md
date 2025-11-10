# Contributing to mm-ai-knowledge

Thank you for your interest in contributing! This guide will help you understand what content belongs in this repository and how to contribute effectively.

## Quick Start

1. Read [SCOPE.md](SCOPE.md) to understand this repository's purpose
2. Check if your contribution fits the [content guidelines](#content-guidelines)
3. Follow the [contribution process](#contribution-process)

## Content Guidelines

### ✅ Content That Belongs Here

This repository focuses on **generic, reusable, and educational** AI content:

- **Generic prompt templates** that can be adapted to any domain
- **Educational examples** demonstrating AI tool usage
- **Conceptual workflow patterns** (structure, not implementation)
- **Tool-agnostic command templates**
- **Generic agent configuration examples**
- **Best practices guides** for AI-assisted development
- **Learning resources** about prompt engineering, AI tools, etc.

### ❌ Content That Does NOT Belong Here

Avoid contributing domain-specific or tightly coupled content:

- **Production-ready plugins** with API integrations
- **Organization-specific workflows** (e.g., company-specific JIRA processes)
- **Platform-specific automation** (e.g., OpenShift CI scripts, AWS CLI wrappers)
- **Tightly coupled integrations** (e.g., Sippy client, Gangway triggers)
- **Domain-specific commands** (e.g., `/olm:install`, `/jira:solve`)

**For OpenShift-specific content**, contribute to [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

**For other domain-specific content**, consider creating a dedicated repository.

## Contribution Process

### 1. Choose the Right Directory

Based on your contribution type:

- **Prompts** → `prompts/`
  - System prompts → `prompts/system/`
  - Task-specific → `prompts/task-specific/`
  - Examples → `prompts/examples/`

- **Commands** → `commands/`
  - Claude Code → `commands/claude-code/`
  - Cursor → `commands/cursor/`
  - General → `commands/general/`

- **Agents** → `agents/`
  - Agent templates → `agents/specialized/`
  - Workflow examples → `agents/workflows/`
  - Base templates → `agents/templates/`

- **Workflows** → `workflows/`
  - Development patterns → `workflows/development/`
  - Content workflows → `workflows/content/`
  - Automation patterns → `workflows/automation/`

- **Tools** → `tools/`
  - MCP examples → `tools/mcp-servers/`
  - Script templates → `tools/scripts/`
  - Integration patterns → `tools/integrations/`

- **Example Projects** → `example-ai-projects/`
  - Links to exemplary projects only

### 2. Follow Naming Conventions

- **Prompts**: `{purpose}-prompt.md` (e.g., `code-review-prompt.md`)
- **Commands**: `{command-name}.md` (e.g., `refactor-function.md`)
- **Agents**: `{agent-type}-agent.{json|yaml|md}` (e.g., `code-reviewer-agent.yaml`)
- **Workflows**: `{workflow-name}-workflow.{json|yaml}` (e.g., `pr-review-workflow.yaml`)

Use lowercase with hyphens, be descriptive but concise.

### 3. Document Your Contribution

Every contribution must include:

1. **Clear Purpose**: What does it do?
2. **Usage Instructions**: How to use it?
3. **Examples**: Show it in action
4. **Customization Guide**: How to adapt it?
5. **Prerequisites**: What's needed to use it?

### 4. Keep It Generic

Ensure your contribution is:

- **Domain-agnostic**: Works across different fields
- **Loosely coupled**: No tight API integrations
- **Adaptable**: Easy to customize for different use cases
- **Educational**: Helps users learn and understand

### 5. Test Your Contribution

Before submitting:

- Verify the content is accurate
- Ensure examples work as described
- Check that instructions are clear
- Confirm it doesn't duplicate existing content

## Example: Good vs. Bad Contributions

### Good: Generic Code Review Prompt

```markdown
# Code Review Prompt

Review the following code for:

1. **Correctness**: Logic errors, edge cases, potential bugs
2. **Readability**: Clear naming, structure, comments where needed
3. **Performance**: Inefficient algorithms, unnecessary operations
4. **Security**: Input validation, sensitive data handling
5. **Best Practices**: Follows language/framework conventions

## How to Use

Customize the focus areas based on your needs:
- For security-critical code, emphasize item 4
- For performance-sensitive code, emphasize item 3
- Add your team's specific guidelines

## Example

[Shows generic example applicable to any language]
```

**Why it's good**: Generic, adaptable, educational, no specific tool dependencies.

### Bad: OpenShift Bug Fix Command

```markdown
# /openshift:fix-bug <JIRA-ID>

Fetches bug details from JIRA, analyzes OpenShift repository, creates fix,
runs OpenShift CI tests, updates JIRA status.

## Implementation

Uses JIRA API, Sippy integration, Gangway job triggering...
```

**Why it's bad**: Specific to OpenShift, tightly coupled to JIRA/Sippy APIs, production tool (not a template). This belongs in [ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Special Guidelines

### Prompts

- Focus on prompt engineering techniques
- Provide examples with explanations
- Show how to customize for different contexts
- Avoid embedding specific tool names unless necessary

### Commands

- Provide command structure templates
- Explain what the command should accomplish
- Show adaptable examples
- Don't implement specific API calls

### Agents

- Offer configuration templates
- Document agent capabilities and limitations
- Provide customization guidance
- Keep generic, avoid domain-specific knowledge

### Workflows

- Show workflow structure and patterns
- Document step dependencies
- Provide conceptual examples
- Don't hardcode specific tools or services

## Review Process

1. **Self-review**: Check against [content guidelines](#content-guidelines)
2. **Submit PR**: Create a pull request with clear description
3. **Maintainer review**: Maintainers verify fit and quality
4. **Iteration**: Address feedback if needed
5. **Merge**: Once approved, content is merged

## Need Help?

- **Unsure if your content fits?** → Check [SCOPE.md](SCOPE.md) or open an issue to discuss
- **Looking for domain-specific repos?** → See [Related Projects](README.md#related-projects)
- **Have questions?** → Open an issue with the `question` label

## Code of Conduct

- Be respectful and constructive
- Focus on content quality
- Help maintain clear scope boundaries
- Support learning and knowledge sharing

## Recognition

Contributors are recognized in:
- Git commit history
- Release notes (for significant contributions)
- Community acknowledgments

Thank you for helping build a valuable, generic AI knowledge base! 🚀
