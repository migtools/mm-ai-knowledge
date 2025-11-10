# Workflows

**Generic multi-step workflow templates** that combine prompts, commands, and agents to accomplish complex tasks.

## Scope

**This directory is for generic workflow patterns and templates.** For production-ready, domain-specific workflows (e.g., OpenShift PR review automation, JIRA-integrated bug fixing), see specialized repositories like [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Structure

- `development/` - Generic software development workflow templates (CI/CD patterns, testing approaches, deployment concepts)
- `content/` - Content creation and management workflow examples
- `automation/` - Generic task automation and process workflow patterns

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

1. **Keep It Generic**: Workflows should be adaptable to different projects and domains
2. **Define Clear Steps**: Each step should have a specific purpose
3. **Handle Dependencies**: Specify which steps depend on others
4. **Consider Parallelization**: Run independent steps in parallel
5. **Add Error Handling**: Define what happens if a step fails
6. **Document Inputs/Outputs**: Clearly specify data flow
7. **Use Placeholders**: Avoid hardcoding specific tools, APIs, or services

### Examples of Appropriate Workflows

✅ **Good (Generic Templates):**
- PR review workflow pattern (analyze → test → review → summarize)
- Documentation generation workflow template
- Generic CI/CD pipeline structure

❌ **Not Appropriate (Domain-Specific):**
- OpenShift bug fix workflow with JIRA integration
- Specific Gangway job triggering workflow
- Production OLM operator installation workflow

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
