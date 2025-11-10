# Repository Scope and Differentiation

This document clarifies the scope of `mm-ai-knowledge` and how it differs from related repositories, particularly [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers).

## Quick Reference

| Aspect | mm-ai-knowledge | openshift-eng/ai-helpers |
|--------|----------------|--------------------------|
| **Purpose** | Generic AI knowledge base and learning resource | OpenShift-specific development automation |
| **Target Audience** | Anyone learning AI tools, any domain | OpenShift developers and engineers |
| **Content Type** | Templates, examples, educational content | Production-ready plugins and commands |
| **Integration Level** | Conceptual examples, patterns | Full API integrations (JIRA, Sippy, Gangway) |
| **Maintenance** | Community-contributed templates | Actively maintained production tools |
| **Deployment** | Copy and adapt to your needs | Install via Claude Code plugin marketplace |

## mm-ai-knowledge: Generic Knowledge Base

### What Belongs Here

**Educational Content:**
- Prompt engineering tutorials and examples
- Best practices guides for AI tools
- Generic templates that can be adapted to any domain
- Conceptual workflow patterns
- Example agent configurations (templates only)

**Generic Patterns:**
- Code review prompt templates (no specific tool integration)
- Documentation generation examples
- Test case writing patterns
- Refactoring approach templates
- General MCP server configuration examples

**Cross-Platform Examples:**
- Tool-agnostic command examples
- Generic workflow structures
- Platform-independent automation patterns
- Reusable prompt libraries

### What Does NOT Belong Here

**Domain-Specific Production Code:**
- JIRA API integrations
- OpenShift CI/CD automation
- Kubernetes operator commands
- Organization-specific workflows
- Production-ready plugins for specific platforms

**Tightly Coupled Integrations:**
- Must-gather analysis scripts
- Sippy API clients
- Gangway job triggers
- OLM-specific commands

## openshift-eng/ai-helpers: OpenShift Automation

### What It Provides

**Production-Ready Tools:**
- Complete Claude Code plugin marketplace
- JIRA workflow automation (`/jira:solve`, `/jira:create`)
- OpenShift CI integration (`/ci:trigger-periodic`, `/ci:ask-sippy`)
- OLM operator management (`/olm:install`, `/olm:diagnose`)
- Must-gather analysis tools (`/must-gather:analyze`)
- Git workflow automation for OpenShift repos

**Active Integrations:**
- JIRA API for bug tracking
- Sippy for test result queries
- Gangway for CI job triggering
- GitHub for OpenShift repository management
- Prow for job status monitoring

**Domain Expertise:**
- OpenShift development best practices
- Red Hat engineering workflows
- OpenShift CI/CD pipeline knowledge
- OLM and operator lifecycle expertise

## Decision Tree: Where Should I Contribute?

```
Are you contributing...

├─ Generic, reusable AI pattern?
│  └─ ✅ mm-ai-knowledge
│
├─ Educational template or example?
│  └─ ✅ mm-ai-knowledge
│
├─ OpenShift-specific automation?
│  └─ ✅ ai-helpers
│
├─ Production plugin with API integration?
│  ├─ For OpenShift? → ✅ ai-helpers
│  └─ For other domain? → Create domain-specific repo
│
└─ Generic prompt or agent template?
   └─ ✅ mm-ai-knowledge
```

## Examples

### Example 1: Code Review

**mm-ai-knowledge would have:**
```markdown
# Generic Code Review Prompt

Review this code for:
1. Correctness and logic errors
2. Code style and readability
3. Performance considerations
4. Security concerns

Focus on: [SPECIFY YOUR FOCUS AREAS]
Code style guide: [LINK TO YOUR STYLE GUIDE]
```

**ai-helpers would have:**
```markdown
# /git:suggest-reviewers

Analyzes git blame and OWNERS files in OpenShift repositories to suggest 
appropriate reviewers for a PR, then optionally requests reviews via GitHub API.
```

### Example 2: JIRA Integration

**mm-ai-knowledge would have:**
```markdown
# JIRA Bug Report Template

When analyzing a bug, consider:
- Steps to reproduce
- Expected vs actual behavior
- Environment details
- Impact assessment

[Generic template for structuring bug information]
```

**ai-helpers would have:**
```markdown
# /jira:solve <issue-key> <base-branch>

Fetches JIRA issue details via API, analyzes the problem, creates a PR with 
fix, runs tests, and updates JIRA with PR link and status.
```

### Example 3: Testing Workflows

**mm-ai-knowledge would have:**
```yaml
# Generic Test Generation Workflow Pattern

steps:
  - analyze-code
  - identify-test-scenarios
  - generate-test-cases
  - review-coverage
```

**ai-helpers would have:**
```markdown
# /openshift:new-e2e-test

Generates complete Ginkgo-framework E2E tests for OpenShift, including proper
imports, BeforeEach setup, test assertions, and validation against OpenShift
test suite conventions.
```

## When in Doubt

**Ask yourself:**
1. Could this be used outside of OpenShift/my specific domain? → `mm-ai-knowledge`
2. Does this integrate with specific APIs or services? → Domain-specific repo
3. Is this a template or a production tool? → Template = `mm-ai-knowledge`, Tool = domain-specific
4. Does it require maintaining external integrations? → Domain-specific repo

## Repository Coordination

To prevent duplication and overlap:

1. **Cross-reference**: Both repos should link to each other where appropriate
2. **Clear boundaries**: Generic templates stay in mm-ai-knowledge, implementations go to domain repos
3. **Contribution guidance**: Clear documentation on where to contribute what
4. **Regular review**: Periodically review content to ensure it's in the right place

## Questions?

- **"I have a generic prompt but it mentions OpenShift as an example"**
  → Fine for mm-ai-knowledge if it's adaptable to other domains. Use OpenShift as one example among many.

- **"I have an OpenShift command that could be useful elsewhere"**
  → Keep the working implementation in ai-helpers. Create a generic template version for mm-ai-knowledge if applicable.

- **"I want to create commands for another domain (AWS, Azure, etc.)"**
  → Create a domain-specific repo following the ai-helpers model, and link to mm-ai-knowledge for generic patterns.

## Summary

- **mm-ai-knowledge**: Generic, educational, template-focused
- **ai-helpers**: OpenShift-specific, production-ready, integration-focused
- Both repositories serve different but complementary purposes
- Clear differentiation prevents duplication and user confusion
