# Prompts

This directory contains **generic, reusable prompts and prompt templates** for various AI tools and tasks.

## Scope

**This directory is for general-purpose prompt templates** that can be adapted to any domain. For domain-specific prompts (e.g., OpenShift debugging workflows, JIRA triage patterns), see specialized repositories like [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Structure

- `system/` - Generic system-level prompts that define AI behavior and personality
- `task-specific/` - Generic prompts optimized for common tasks (coding, writing, analysis, etc.)
- `examples/` - Example prompts with detailed use cases and explanations

## How to Use

1. Browse the subdirectories for the type of prompt you need
2. Copy the prompt text
3. Paste it into your AI tool (Claude, ChatGPT, etc.)
4. Customize as needed for your specific use case

## Contributing a Prompt

When adding a new prompt, include:

```markdown
# [Prompt Name]

## Purpose
Brief description of what this prompt does

## Best Used For
- Use case 1
- Use case 2

## Prompt

[Your prompt text here]

## Example Output
[Optional: Show what kind of output to expect]

## Tips
- Any usage tips or variations
```

## Naming Convention

- Use descriptive names: `{task}-{type}-prompt.md`
- Examples: `code-review-prompt.md`, `technical-writing-prompt.md`

### Examples of Appropriate Prompts

✅ **Good (Generic):**
- Generic code review prompt template
- Technical documentation writing guide
- Test case generation prompt
- Refactoring assistance prompt

❌ **Not Appropriate (Domain-Specific):**
- OpenShift upgrade path analysis prompt
- JIRA bug report formatting prompt
- Must-gather data interpretation prompt

## Examples

See the `examples/` directory for well-documented prompt examples.
