# Commands

This directory contains **generic, educational examples** of slash commands for various AI-assisted development tools.

## Scope

**This directory is for generic command templates and examples.** For production-ready, domain-specific commands (e.g., OpenShift, JIRA integration, CI/CD automation), see specialized repositories like [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Structure

- `claude-code/` - Generic command examples for Claude Code (`.md` format)
- `cursor/` - Generic command examples for Cursor IDE
- `general/` - Tool-agnostic command templates

## Claude Code Commands

Claude Code commands are markdown files placed in `.claude/commands/` directory.

### Format

```markdown
Brief description of what this command does

You can include:
- Instructions for the AI
- Context about the task
- Expected output format
- Any specific requirements
```

### Installation

```bash
# Copy to your project's .claude/commands directory
cp commands/claude-code/your-command.md /path/to/project/.claude/commands/

# Use in Claude Code
/your-command
```

## Creating New Commands

1. **Keep It Generic**: Commands should be applicable across projects and domains
2. **Focus on Education**: Provide templates and examples, not production code
3. **Be Specific**: Commands should have a clear, single purpose
4. **Add Context**: Explain what the command should do
5. **Include Examples**: Show expected input/output when relevant
6. **Avoid Tight Coupling**: Don't integrate with specific APIs or services (use examples instead)

### Examples of Appropriate Commands

✅ **Good (Generic):**
- `/refactor-function` - Template for requesting code refactoring
- `/explain-code` - Generic code explanation prompt
- `/generate-tests` - Template for test generation requests

❌ **Not Appropriate (Domain-Specific):**
- `/jira:create-bug` - JIRA API integration (better for ai-helpers)
- `/deploy-to-staging` - Environment-specific deployment
- `/trigger-ci-job` - Specific CI system integration

## Naming Convention

- Use lowercase with hyphens: `analyze-performance.md`
- Be descriptive but concise
- Avoid generic names like `help.md` or `do-thing.md`

## Example Command Structure

```markdown
# Quick Command Description (first line)

Detailed instructions for the AI assistant:
1. What to analyze
2. How to process it
3. What format to return

## Context
Additional context the AI needs to know

## Output Format
Specify the expected output format
```
