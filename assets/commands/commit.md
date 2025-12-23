---
description: Create atomic commits using TDG plugin
---

# Commit - Atomic Commit Wrapper

Wrapper command that delegates to TDG's atomic-commit functionality.

## Usage

```
/commit
```

## Instructions

1. **Invoke TDG Atomic Commit**: Use `/tdg:atomic-commit` from https://github.com/chanwit/tdg
2. This command is a convenience wrapper for the TDG plugin's atomic commit feature

## What it does

- Analyzes staged/unstaged changes
- Detects mixed concerns (multiple unrelated changes)
- Helps create clean, focused atomic commits
- Each commit should be a complete unit of work

## Delegation

This command delegates to:
```
/tdg:atomic-commit
```

Simply invoke the TDG plugin's atomic-commit skill when user runs `/commit`.
