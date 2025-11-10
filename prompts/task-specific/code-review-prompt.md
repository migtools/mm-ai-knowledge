# Generic Code Review Prompt

## Purpose

A general-purpose prompt template for requesting AI-assisted code reviews. This template can be adapted to any programming language, framework, or domain.

## Best Used For

- Reviewing pull requests
- Analyzing code quality
- Identifying potential issues
- Learning code review best practices

## Prompt Template

```
Please review the following code with a focus on:

1. **Correctness & Logic**
   - Are there any logical errors or bugs?
   - Are edge cases handled properly?
   - Is the code doing what it's supposed to do?

2. **Code Quality & Readability**
   - Is the code easy to understand?
   - Are variable/function names clear and descriptive?
   - Is the code structure logical and well-organized?
   - Are there appropriate comments where needed?

3. **Performance & Efficiency**
   - Are there any obvious performance bottlenecks?
   - Could any algorithms be optimized?
   - Are resources (memory, CPU, I/O) used efficiently?

4. **Security Considerations**
   - Are inputs properly validated?
   - Is sensitive data handled securely?
   - Are there any potential security vulnerabilities?

5. **Best Practices & Conventions**
   - Does it follow language-specific best practices?
   - Does it follow the project's coding standards?
   - Are there any anti-patterns?

6. **Maintainability**
   - Is the code modular and reusable?
   - Would it be easy for others to modify or extend?
   - Is error handling appropriate?

Please provide:
- Specific issues found with line numbers/locations
- Severity level (critical, major, minor, suggestion)
- Recommended improvements
- Positive feedback on what's done well

[PASTE YOUR CODE HERE]
```

## Customization Guide

### Focus on Specific Areas

If you need to emphasize certain aspects, modify the prompt:

**For security-critical code:**
```
Focus especially on items 4 (Security) and provide detailed threat analysis.
```

**For performance-sensitive code:**
```
Prioritize item 3 (Performance) and suggest specific optimizations with benchmarks.
```

**For learning purposes:**
```
Provide detailed explanations of issues found and suggest learning resources.
```

### Add Language-Specific Criteria

Add language or framework-specific guidelines:

```
Additionally, please verify:
- Python: PEP 8 compliance, type hints usage
- JavaScript: ESLint rules, modern ES6+ syntax
- Java: Design patterns, SOLID principles
- Go: idiomatic Go conventions, error handling patterns
```

### Add Project-Specific Guidelines

Include your project's standards:

```
Also check against our project guidelines:
- [Link to your coding standards]
- [Link to your style guide]
- [Specific patterns or conventions your team uses]
```

## Example Usage

### Example 1: Basic Code Review

```
Please review the following code with a focus on:
[Use the full template above]

def calculate_total(prices):
    total = 0
    for price in prices:
        total = total + price
    return total
```

**Expected AI Response Type:**
- Point out lack of input validation
- Suggest using `sum()` built-in function
- Note missing type hints
- Recommend docstring

### Example 2: Security-Focused Review

```
Please review the following code with a focus on security (item 4):

[Include security-sensitive code]
```

### Example 3: Learning-Focused Review

```
Please review the following code. I'm learning [language/framework], so please:
- Explain issues in detail
- Suggest learning resources
- Show alternative implementations
- Highlight good practices I'm already using

[Include code to review]
```

## Tips for Best Results

1. **Be Specific**: If you have particular concerns, mention them upfront
2. **Provide Context**: Include relevant background about the code's purpose
3. **Include Related Code**: If the code depends on other functions/classes, include them
4. **Specify Standards**: Mention any coding standards or style guides to follow
5. **Ask for Alternatives**: Request alternative approaches if you're uncertain
6. **Iterate**: Use follow-up questions to dive deeper into issues

## Integration with Development Workflow

This prompt can be used:
- **Before Committing**: Self-review your code
- **In Pull Requests**: Add as a PR template step
- **During Pair Programming**: Quick quality checks
- **For Learning**: Analyze example code or tutorials
- **Code Refactoring**: Identify areas needing improvement

## Related Resources

- [CONTRIBUTING.md](../../CONTRIBUTING.md) - How to adapt this for your needs
- [SCOPE.md](../../SCOPE.md) - Understanding generic vs. domain-specific content
- Domain-specific alternatives: [openshift-eng/ai-helpers](https://github.com/openshift-eng/ai-helpers) for OpenShift code review patterns
