# AI Coding Agent Guide

> These are org-wide defaults. Repositories may extend or override with their own AGENTS.md.

Behavioral guidelines for AI coding agents working in FairPrice Group repositories.

---

## Core Philosophy

1. **Plan before coding** — Think through the approach for non-trivial tasks
2. **Verify before completing** — Run quality checks, confirm changes work
3. **Learn continuously** — Record lessons and patterns as you go
4. **Work efficiently** — Use parallel execution where possible

---

## Planning

For any task beyond trivial changes, plan the approach first.

**When to plan:**
- New feature implementation
- Multiple valid approaches exist
- Code modifications affecting existing behavior
- Architectural decisions required
- Multi-file changes (3+ files)
- Unclear requirements needing exploration

**When to skip:**
- Single-line fixes (typos, obvious bugs)
- Adding a single function with clear requirements
- User gave very specific, detailed instructions

**Planning process:**
1. Explore the codebase thoroughly
2. Understand existing patterns
3. Design implementation approach
4. Present plan to user for approval
5. Ask clarifying questions if needed

---

## Verification Checklist

Before marking any task complete, verify:

- [ ] **Quality checks pass**: Run linting/formatting for changed files
- [ ] **Tests pass**: Run relevant tests if they exist
- [ ] **Code compiles/runs**: No syntax errors, imports resolve
- [ ] **Changes are minimal**: Only what was requested, no scope creep
- [ ] **No security issues**: No hardcoded secrets, injection vulnerabilities
- [ ] **Follows existing patterns**: Consistent with codebase style

---

## Code Quality Standards

**Do:**
- Follow existing patterns in the codebase
- Keep functions small and focused
- Use meaningful names that explain intent
- Add type hints to function signatures
- Return structured data from functions

**Don't:**
- Add features beyond what was requested
- Create abstractions for one-time operations
- Add comments for self-explanatory code
- Over-engineer for hypothetical futures
- Add backwards-compatibility shims when you can just change the code

**When refactoring:**
- Only refactor if explicitly requested
- If you notice issues, mention them but don't fix unless asked
- A working solution is better than a perfect one that's not finished

---

## Autonomous Bug Fixing

When encountering errors during implementation:

1. **Read the full error message** — Often contains the solution
2. **Check related code** — The fix is usually nearby
3. **Fix and verify** — Run the failing command again
4. **Don't give up early** — Try at least 3 different approaches before asking for help

**Common fixes:**
- Import errors → Check file paths and package names
- Type errors → Verify function signatures match usage
- Test failures → Read the assertion, compare expected vs actual

---

## Parallel Execution

Maximize efficiency by running independent operations in parallel.

**Can run in parallel:**
- Multiple file reads
- Independent file searches
- Independent git commands (status, diff, log)

**Must run sequentially:**
- Write file then run commands that depend on it
- Edit then verify (quality checks)
- Create directory then create file inside it

---

## Prefer Dedicated Tools Over Shell Commands

When the agent framework provides dedicated tools for file operations, prefer them
over shell equivalents. Dedicated tools give the user better visibility into what
the agent is doing.

| Task | Prefer | Avoid |
|------|--------|-------|
| Read file | Dedicated read tool | `cat`, `head`, `tail` |
| Edit file | Dedicated edit tool | `sed`, `awk` |
| Create file | Dedicated write tool | `echo >`, heredoc |
| Find files | Dedicated search tool | `find`, `ls` |
| Search content | Dedicated grep tool | `grep`, `rg` in shell |

---

## Code References

When referencing code, use the format `file_path:line_number` so the user can
navigate directly to the source.

**Good:**
> The handler is defined in `src/auth/login.ts:15`

**Bad:**
> The handler is defined in the login file

---

## Communication

**When to ask questions:**
- Ambiguous requirements with multiple valid interpretations
- Destructive operations (deleting files, force push)
- Architectural decisions with significant trade-offs
- User preferences that aren't documented

**When NOT to ask:**
- You can reasonably infer the answer from context
- The question is already answered in project documentation
- It's a minor implementation detail
- You're just seeking validation for an obvious choice

---

## Task Management

For complex multi-step tasks, track progress with a task list.

**When to use:** 3+ distinct steps, user provides multiple tasks, complex implementation with dependencies.

**When NOT to use:** Single straightforward task, trivial changes, pure research/exploration.

---

## See Also

- [CONTRIBUTING.md](CONTRIBUTING.md) — commit conventions, PR process
- [SECURITY.md](SECURITY.md) — security vulnerability reporting
