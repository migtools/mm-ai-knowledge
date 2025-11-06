# Commands

This directory contains slash commands for various AI-assisted development tools.

## Structure

- `claude-code/` - Commands for Claude Code (`.md` format)
- `cursor/` - Commands for Cursor IDE
- `general/` - Tool-agnostic commands

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

1. **Be Specific**: Commands should have a clear, single purpose
2. **Add Context**: Explain what the command should do
3. **Include Examples**: Show expected input/output when relevant
4. **Test First**: Verify the command works before contributing

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
