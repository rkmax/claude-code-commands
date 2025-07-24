---
allowed-tools: [Read, Edit, MultiEdit, Write, Bash, Grep, Glob, LS, TodoWrite]
description: Implements features with iterative explore-plan-code-test workflow with failure handling
argument-hint: <feature description>
---

Please follow the iterative "Explore, Plan, Code, Test" workflow to implement: $ARGUMENTS

## Explore

Use parallel subagents to find and read all files useful for implementing the feature: similar components/features as examples, files that need modification, architecture patterns (config, routing, state management), test patterns, existing dependencies, and potential conflicts. The subagents should return relevant file paths, code patterns, architectural decisions, and any constraints or standards discovered.

**Exit Criteria:** You have identified all relevant files, understand the existing architecture, found similar implementations, and can estimate the scope. If scope is significantly larger than initially expected or requires major architectural changes, flag this immediately.

**Failure Handling:** If subagents return poor results, manually search key directories or ask user for guidance on codebase structure.

## Plan

Write a detailed implementation plan considering edge cases, error handling, performance implications, security concerns, and backwards compatibility. Include tests, UI components, and documentation based on repo standards. Estimate complexity and determine if this should be split into multiple phases. Identify any technical debt that must be addressed first. Consider dependency management and version conflicts.

Use parallel subagents for web research on missing technical details only - they should return actionable information, not general concepts. If critical questions remain unanswered, pause here to ask the user before continuing.

**Exit Criteria:** You have a detailed plan with clear phases, identified all dependencies, addressed security considerations, and have contingency plans for major risks.

**Iteration Point:** If planning reveals fundamental architectural issues or security concerns, return to exploration phase to understand constraints better.

## Code

Implement the feature following existing codebase patterns and conventions. Prioritize clarity over clever code and simplicity over complexity. Write clean, readable code that matches the project's style. Include proper input validation and security measures. 

For complex features, use parallel subagents to implement independent components simultaneously. Commit incrementally with meaningful messages as you complete each logical piece. Run linting, type checking, and security scans after significant changes. Apply autoformatting and fix reasonable linter warnings before finalizing.

**Exit Criteria:** All planned functionality is implemented, code follows project standards, security measures are in place, and all static analysis passes.

**Iteration Point:** If implementation reveals design flaws or performance issues, return to planning phase to reassess approach.

## Test

Use parallel subagents to run all tests and ensure they pass. Test the happy path, error states, edge cases, integration points, and security boundaries. Verify no regressions in existing functionality. Run performance tests if applicable. For significant UX changes, manually test in the browser covering user workflows, accessibility, responsive behavior, and cross-browser compatibility.

Test error scenarios, malicious input handling, and boundary conditions. Verify proper error messages and graceful degradation.

**Exit Criteria:** All tests pass, no regressions detected, performance benchmarks met, security tests pass, and manual testing confirms expected behavior.

**Iteration Point:** If testing reveals fundamental problems, return to planning stage to address architectural issues. For minor bugs, fix and retest.

## Write up your work

When you are happy with your work, write up a short report that could be used as the PR description. Include what you set out to do, the choices you made with their brief justification, security considerations addressed, performance implications, and any commands you ran in the process that may be useful for future developers to know about.