# Codex Long-Run Workflow

This project uses a repo-backed memory workflow for long Codex runs.

It is not literally unlimited tokens. The approach is to keep the important state in GitHub files so every Codex session can reload the project state from disk and continue with a small next action.

## Why

The Shamela language-books translation is too large to keep in one chat context.

Instead of depending on chat history, the repo stores:

- the goal
- the current scope
- the next action
- the queue rules
- completed work
- session logs
- output schemas
- validation rules

## Session Loop

Every Codex session should follow this loop:

1. Read `codex/CONTEXT_PACK.md`
2. Read `codex/NEXT_ACTION.md`
3. Read only the files needed for the next chunk
4. Do exactly one useful chunk
5. Save the output
6. Update `codex/SESSION_LOG.md`
7. Update `codex/NEXT_ACTION.md`
8. Commit and push changes

## Rules

- Keep each chunk small enough to review.
- Never rely on memory from the previous chat if a repo file should contain it.
- Write decisions into `codex/PROJECT_MEMORY.md`.
- Write progress into `codex/SESSION_LOG.md`.
- Write the next concrete task into `codex/NEXT_ACTION.md`.
- Keep large dataset outputs out of GitHub.
- Link local output paths or external dataset storage from GitHub Issues.

## Practical Meaning

Codex can work for a long time because it always has a compact project state to reload.

That gives an "unlimited-token style" workflow without pretending the model context window is actually unlimited.

