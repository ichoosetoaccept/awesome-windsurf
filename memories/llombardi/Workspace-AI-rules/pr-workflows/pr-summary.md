---
description: Generate technical PR summary using conversation context
---

# PR Summary Generation Workflow

This workflow generates a technical PR summary by analyzing changes from the current conversation context for developers and DevOps teams.

## Step 1: Analyze Changes from Context

Extract technical information from conversation history:

- **Files Modified**: Source code, tests, config, documentation changes
- **Code Metrics**: Lines added/removed, functions/methods modified
- **Architecture Impact**: New packages, interface changes, breaking changes
- **Dependencies**: go.mod updates, new libraries

## Step 2: Generate Technical PR Summary

## PR Summary: [Title]

### What Changed

Brief technical description of the implementation.

### Files Modified

- **Core Changes**: X files (+Y, -Z lines)
- **Tests**: Unit/integration tests added/modified
- **Config**: Configuration or deployment changes
- **Dependencies**: Package updates or additions

### Technical Impact

- **Breaking Changes**: API/interface modifications
- **Performance**: Expected impact on system performance
- **Security**: Security considerations or improvements
- **Architecture**: Design pattern or structural changes

### Testing

- **Coverage**: New tests added, existing tests modified
- **Manual Testing**: Key scenarios verified
- **Edge Cases**: Boundary conditions tested

### Notes

- **Migration**: Database or config migrations required
- **Environment**: New environment variables or settings
- **Breaking Changes**: API/interface modifications
- **Performance**: Expected impact on system performance
- **Security**: Security considerations or improvements
- **Architecture**: Design pattern or structural changes

**Note**: Use `/pr-review` for detailed code analysis and feedback.
