---
description: Generate technical PR summary using conversation context
---

# PR Summary Generation Workflow

This workflow generates a technical PR summary by analyzing changes from the current conversation context for developers and DevOps teams.

## Step 1: Analyze Changes from Context

Extract technical information from conversation history:

- **Files Modified**: Source code, tests, config, documentation changes
- **Code Metrics**: Lines added/removed, functions/methods modified
- **Architecture Impact**: New modules, interface changes, breaking changes
- **Dependencies**: Package manager updates, new libraries

## Step 2: Generate Technical PR Summary

## PR Summary: [Title]

### What Changed

**One-line technical summary**: [Brief description of the core change]

**Concrete deltas** (2-4 bullets):

- Added: [specific functionality/files added]
- Modified: [specific components changed]
- Removed: [specific items deleted]
- Fixed: [specific issues resolved]

**Rationale**: [One sentence explaining why this change was made and any scope/rollout considerations]

### Files Modified

- **Core Changes**: X files (+Y, -Z lines)
- **Tests**: Unit/integration tests added/modified
- **Config**: Configuration or deployment changes
- **Dependencies**: Package updates or additions

<!-- Optional machine-friendly tokens:
files_changed: {{files_changed}}
lines_added: {{lines_added}}
lines_deleted: {{lines_deleted}}
test_files_modified: {{test_files_modified}}
config_files_modified: {{config_files_modified}}
dependency_files_modified: {{dependency_files_modified}}
-->

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

**Note**: Use `/pr-review` for detailed code analysis and feedback.
