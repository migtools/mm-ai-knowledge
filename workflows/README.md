# Workflows

Multi-step workflows that combine prompts, commands, and agents to accomplish complex tasks.

## Structure

- `development/` - Software development workflows (CI/CD, testing, deployment)
- `content/` - Content creation and management workflows
- `automation/` - Task automation and process workflows

## What is a Workflow?

A workflow is a series of steps that combine multiple AI tools and commands to complete a complex task. Workflows can orchestrate:
- Multiple agents working together
- Sequential or parallel task execution
- Conditional logic and branching
- Integration with external tools

## Workflow Format

Workflows can be defined in JSON or YAML:

### Example Workflow (YAML)

```yaml
name: pr-review-workflow
description: Automated pull request review workflow

steps:
  - name: analyze-changes
    agent: code-analyzer
    inputs:
      - pr_diff

  - name: security-scan
    agent: security-scanner
    depends_on: analyze-changes

  - name: run-tests
    agent: test-runner
    parallel: true

  - name: generate-summary
    agent: summarizer
    depends_on:
      - security-scan
      - run-tests
    output: pr_comment

triggers:
  - event: pull_request_opened
  - event: pull_request_updated
```

## Using Workflows

```bash
# Copy workflow to your project
cp workflows/development/pr-review-workflow.yaml .claude/workflows/

# Reference in your CI/CD or development process
```

## Creating Workflows

1. **Define Clear Steps**: Each step should have a specific purpose
2. **Handle Dependencies**: Specify which steps depend on others
3. **Consider Parallelization**: Run independent steps in parallel
4. **Add Error Handling**: Define what happens if a step fails
5. **Document Inputs/Outputs**: Clearly specify data flow

## Workflow Components

- **Triggers**: What initiates the workflow
- **Steps**: Individual tasks to execute
- **Agents**: Specialized agents used in steps
- **Conditions**: Logic for branching
- **Outputs**: What the workflow produces

## Best Practices

- Keep workflows focused on a single end goal
- Make steps reusable
- Include rollback procedures
- Test workflows thoroughly
- Document expected outcomes
