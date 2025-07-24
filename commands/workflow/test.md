---
allowed-tools: [Read, Edit, MultiEdit, Write, Bash, Grep, Glob, LS, TodoWrite]
description: Implements features following explore, plan, code, test workflow
argument-hint: <feature description>
---

Please follow the "Explore, Plan, Code, Test" workflow to implement: $ARGUMENTS

## Explore

Use parallel subagents to find and read all files useful for implementing the feature: similar components/features as examples, files that need modification, architecture patterns (config, routing, state management), test patterns, existing dependencies, and potential conflicts. The subagents should return relevant file paths, code patterns, architectural decisions, and any constraints or standards discovered.

## Plan

Write a detailed implementation plan considering edge cases, error handling, performance implications, and backwards compatibility. Include tests, UI components, and documentation based on repo standards. Estimate complexity and determine if this should be split into multiple phases. Use parallel subagents for web research on missing technical details only - they should return actionable information, not general concepts. If critical questions remain unanswered, pause here to ask the user before continuing.

## Code

Implement the feature following existing codebase patterns and conventions. Prioritize clarity over clever code and simplicity over complexity. Write clean, readable code that matches the project's style. Commit incrementally with meaningful messages as you complete each logical piece. Run linting and type checking after significant changes. Apply autoformatting and fix reasonable linter warnings before finalizing.

## Test

Use parallel subagents to run all tests and ensure they pass. Test the happy path, error states, edge cases, and integration points. Verify no regressions in existing functionality. For significant UX changes, manually test in the browser covering user workflows, accessibility, and responsive behavior. If testing reveals problems, revisit the planning stage to address fundamental issues.

## Write up your work

When you are happy with your work, write up a short report that could be used as the PR description. Include what you set out to do, the choices you made with their brief justification, and any commands you ran in the process that may be useful for future developers to know about.