---
description: This workflow helps review Pull Requests by generating a diff against the main/master branch and collecting context from the user.
auto_execution_mode: 3
---

# PR Review Workflow

This workflow provides a comprehensive review of Pull Requests by analyzing code changes, collecting context, and evaluating multiple aspects of the implementation. You may also occasionally leave open questions to the user if you spot some issue and let the user guess what the issue is, as a learning experience.

## Step 1: Generate Diff Against Base Branch

First, we'll generate a diff against the main/master branch to understand what changes are being proposed.

```bash
# Check if main branch exists, fallback to master
echo "Checking for available base branches..."

if git show-ref --verify --quiet refs/heads/main; then
    BASE_BRANCH="main"
elif git show-ref --verify --quiet refs/remotes/origin/main; then
    BASE_BRANCH="origin/main"
elif git show-ref --verify --quiet refs/heads/master; then
    BASE_BRANCH="master"
else
    BASE_BRANCH="origin/master"
fi

echo "Selected base branch: $BASE_BRANCH"

# Get current branch name
CURRENT_BRANCH=$(git branch --show-current)

# Find merge base
MERGE_BASE=$(git merge-base $BASE_BRANCH $CURRENT_BRANCH)
echo "Merge base commit: $MERGE_BASE"

# Generate diff against base branch
git diff $MERGE_BASE $CURRENT_BRANCH
```

## Step 2: Collect PR Context if not already provided by user. Skip if provided already

Please provide any of the following context about this Pull Request:

1. **PR Summary**: Brief description of what this PR accomplishes
2. **Ticket/Issue Description**: Link to or description of the related ticket/issue
3. **Business Context**: Why is this change needed?
4. **Breaking Changes**: Are there any breaking changes in this PR?
5. **Testing Strategy**: How was this change tested?

## Step 3: Analyze Code Changes

Based on the diff and context provided, analyze the PR across multiple dimensions:

### 3.1 Algorithmic Complexity Analysis

- Review time and space complexity of new algorithms
- Identify potential performance bottlenecks
- Check for inefficient loops, nested operations, or recursive calls
- Evaluate database query efficiency and N+1 problems

### 3.2 Testing Coverage Analysis

- Verify adequate unit test coverage for new code
- Check for integration tests where appropriate
- Evaluate test quality and edge case coverage
- Ensure mocks and fixtures are properly implemented
- Validate table-driven tests for comprehensive scenarios

### 3.3 Code Consistency Review

- Check adherence to existing code patterns and conventions
- Verify consistent error handling patterns
- Evaluate logging consistency and appropriate log levels
- Review naming conventions and code organization
- Ensure proper dependency injection patterns

### 3.4 Security Analysis

- Identify potential security vulnerabilities
- Check for proper input validation and sanitization
- Review authentication and authorization implementations
- Evaluate data exposure risks
- Check for hardcoded secrets or credentials
- Assess SQL injection and other injection attack vectors

### 3.5 Error Handling & Reliability

- Verify comprehensive error handling
- Check for proper context propagation
- Evaluate graceful degradation scenarios
- Review timeout and retry mechanisms
- Assess potential race conditions or concurrency issues

### 3.6 Architecture & Design Patterns

- Evaluate adherence to established architectural patterns
- Check for proper separation of concerns
- Review interface design and abstraction levels
- Assess maintainability and extensibility
- Validate dependency management and coupling

### 3.7 Performance Considerations

- Review memory usage patterns
- Check for potential memory leaks
- Evaluate concurrency management and lifecycle
- Assess database connection pooling
- Review caching strategies where applicable

### 3.8 Documentation & Maintainability

- Check for adequate code comments (without over-commenting)
- Verify API documentation updates
- Evaluate code readability and self-documentation
- Review configuration changes and documentation

## Step 4: Generate Review Summary

Based on the analysis, I'll provide:

1. **Overall Assessment**: High-level evaluation of the PR quality
2. **Critical Issues**: Must-fix issues that block merge
3. **Recommendations**: Suggested improvements for code quality
4. **Positive Highlights**: Well-implemented aspects worth noting
5. **Risk Assessment**: Potential risks and mitigation strategies

## Step 5: Action Items

I'll categorize findings into:

- **Blocking Issues**: Must be addressed before merge
- **High Priority**: Should be addressed before merge
- **Medium Priority**: Consider addressing in this PR or follow-up
- **Low Priority**: Nice-to-have improvements for future consideration

---

**Note**: This workflow focuses on code review and suggestions only. No changes will be applied to the codebase during the review process.
