# PR Workflows for Windsurf

This contribution provides comprehensive PR (Pull Request) **workflows** for Windsurf that help with code review and PR summary generation.

## What's Included

### PR Review Workflow (`pr-review.md`)

A comprehensive workflow that:

- Generates diffs against main/master branch automatically
- Collects PR context from users
- Performs multi-dimensional code analysis including:
  - Algorithmic complexity analysis
  - Testing coverage review
  - Code consistency checks
  - Security analysis
  - Error handling evaluation
  - Architecture pattern validation
  - Performance considerations
  - Documentation assessment
- Provides structured review summaries with actionable feedback

### PR Summary Workflow (`pr-summary.md`)

A technical summary generator that:

- Analyzes changes from conversation context
- Extracts file modifications and code metrics
- Identifies architecture impacts and dependencies
- Generates structured PR summaries for developers and DevOps (or any technical) teams

## Why I Created This

These workflows solve common pain points in code review processes:

- **Consistency**: Ensures all PRs are reviewed against the same comprehensive criteria
- **Efficiency**: Automates diff generation and context collection
- **Quality**: Covers security, performance, testing, and architectural concerns
- **Documentation**: Generates professional PR summaries from conversation context

## Usage

Use the slash commands in Windsurf:

- `/pr-review` - Comprehensive PR analysis and review
- `/pr-summary` - Generate technical PR summary from conversation context

## Setup

Simply copy these workflow files to your project's `.windsurf/workflows/` directory:

- `pr-review.md`
- `pr-summary.md`

## Tips and Tricks

1. **Context Matters**: The more context you provide about the PR (business requirements, testing strategy), the better the review quality
2. **Iterative Reviews**: Use the workflow multiple times as you address feedback
3. **Learning Tool**: The workflow occasionally leaves open questions to help you learn to spot issues independently
4. **Complementary**: Use `/pr-review` for detailed analysis, then `/pr-summary` for documentation

## Real-World Examples

Perfect for:

- **Enterprise Development**: Consistent review standards across teams
- **Open Source Projects**: Thorough review process for contributors
- **DevOps Teams**: Technical summaries for deployment planning
- **Code Quality Gates**: Automated quality checks before merge

## Current Limitations

- Requires Git repository with main/master branch. Indicate the base branch as context in the command if it's different from main/master.
- Manual context collection step in PR review. You may provide context in the command if you want to skip this step.
