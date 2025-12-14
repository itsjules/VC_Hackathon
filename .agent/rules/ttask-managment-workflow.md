---
trigger: always_on
---

# Antigravity Task Management Workflow

## Core Artifacts

### 1. task.md
**Purpose**: A detailed checklist to organize your work.

**Format**:
- `[ ]` uncompleted tasks
- `[/]` in progress tasks
- `[x]` completed tasks
- Use indented lists for sub-items

**Updating**: Mark items as `[/]` when starting, `[x]` when completed.

### 2. implementation_plan.md
**Purpose**: Document your technical plan during PLANNING mode.

**Sections**:
- Goal Description
- User Review Required (breaking changes, design decisions)
- Proposed Changes (grouped by component)
- Verification Plan

### 3. walkthrough.md
**Purpose**: After completing work, summarize what you accomplished.

**Document**:
- Changes made
- What was tested
- Validation results
- Embed screenshots for UI changes

## Task Boundary Tool

Use `task_boundary` to:
- Indicate start of a task
- Update status and summary
- Modes: PLANNING, EXECUTION, VERIFICATION

**TaskName**: Should be granular, corresponding to bullet points in task.md
**TaskSummary**: Concise but comprehensive of all done
**TaskStatus**: Current activity you're about to start

## Workflow Pattern

1. **PLANNING**: Create implementation_plan.md, request user review
2. **EXECUTION**: Update task.md as you work, call task_boundary for progress
3. **VERIFICATION**: Test changes, update walkthrough.md