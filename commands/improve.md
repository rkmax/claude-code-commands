---
allowed-tools: [Read, Edit, MultiEdit, Write, Bash, Grep, Glob, LS, TodoWrite]
description: Improves code quality, performance, and maintainability by first discovering and applying existing project patterns
argument-hint: <feature or functionality to improve>
---

You are improving: $ARGUMENTS

## Pattern-First Improvement Approach

**Step 1: Discover Existing Project Patterns**

Before implementing improvements, analyze how THIS project handles quality, performance, and maintenance:

### Code Quality Patterns
Search the codebase for quality-related patterns. Use tools like Grep to find:
- Error handling implementations (try/catch, error boundaries, result types)
- Logging and monitoring patterns
- Testing approaches and utilities
- Code organization and structure patterns

**Analyze discovered patterns:**
- What error handling mechanism does the project use?
- How are errors logged and monitored?
- What testing framework and patterns are established?
- What's the preferred code organization structure?

### Performance Patterns
Search for existing performance optimizations in the code:
- Caching implementations (memory, Redis, CDN)
- Database query optimization patterns
- Lazy loading and code splitting approaches
- Memory management and resource cleanup

**Analyze discovered patterns:**
- What caching strategies are already implemented?
- How does the project optimize database interactions?
- What performance monitoring tools are used?
- How are expensive operations handled?

### Maintenance Patterns
Look for maintainability approaches in the codebase:
- Configuration management patterns
- Dependency injection or service patterns
- Documentation standards and conventions
- Code reuse and modularization approaches

**Analyze discovered patterns:**
- How is configuration managed across environments?
- What dependency management patterns exist?
- What documentation format is used (JSDoc, inline comments, etc.)?
- How are common utilities and services organized?

### Best Practice Patterns
Search for established best practices already implemented:
- Type safety and validation approaches
- Security practices and patterns
- Code style and formatting conventions
- CI/CD and development workflow patterns

**Analyze discovered patterns:**
- What type system and validation library is used?
- How are dependencies and versions managed?
- What linting and formatting tools are configured?
- What development and deployment processes exist?

## Step 2: Apply Project Patterns

Based on discovered patterns, implement improvements CONSISTENTLY:

### Error Handling Pattern
If you discover the project has established error handling:
- How are exceptions caught and processed?
- What error logging and reporting mechanism is used?
- Where are error boundaries or handlers implemented?

**Apply the same pattern:** When improving error handling, use the exact same error types, logging format, and handling mechanism. Don't introduce a new error handling approach.

### Performance Optimization Pattern  
If you find the project has performance optimizations:
- What caching layer or strategy is implemented?
- Which database optimization techniques are used?
- How are expensive operations optimized?

**Apply the same pattern:** When adding performance improvements, use the same caching solution, query optimization approach, and monitoring tools as existing optimized code.

### Testing Pattern
If you discover how the project structures tests:
- What testing framework and utilities are used?
- How are test data and mocks organized?
- What testing patterns (unit, integration, e2e) are established?

**Apply the same pattern:** New tests should follow the identical structure, naming conventions, and testing approaches as existing test suites.

### Code Organization Pattern
If you find established organizational patterns:
- How are files and directories structured?
- What naming conventions are used?
- How are shared utilities and services organized?

**Apply the same pattern:** Improved code should follow the same file organization, naming patterns, and service structure as the rest of the project.

## Step 3: Pattern Consistency Check

After implementation, verify consistency:

### Code Quality Consistency
- [ ] Uses same error handling mechanism as existing code
- [ ] Follows same logging and monitoring patterns
- [ ] Implements same testing approach and structure
- [ ] Maintains same code organization principles

### Performance Consistency  
- [ ] Uses same caching strategy as existing optimized code
- [ ] Follows same database optimization patterns
- [ ] Implements same resource management approach
- [ ] Uses same performance monitoring tools

### Maintenance Consistency
- [ ] Uses same configuration management pattern
- [ ] Follows same dependency injection approach
- [ ] Implements same documentation standards
- [ ] Maintains same modularization principles

### Best Practice Consistency
- [ ] Uses same type safety and validation approach
- [ ] Follows same security implementation patterns
- [ ] Implements same code style and formatting
- [ ] Maintains same development workflow standards

## Step 4: Fill Pattern Gaps

**Only if no existing patterns found**, implement these fallbacks:

### Missing Quality Pattern
- Choose and implement consistent error handling mechanism
- Add comprehensive logging and monitoring
- Establish testing framework and patterns
- Create code organization standards

### Missing Performance Pattern  
- Design caching strategy appropriate for the project
- Implement database optimization patterns
- Add performance monitoring and profiling
- Create resource management guidelines

### Missing Maintenance Pattern
- Implement configuration management system
- Design dependency injection or service pattern
- Establish documentation standards
- Create modular code organization

### Missing Best Practice Pattern
- Add type safety and input validation
- Implement security best practices
- Configure code formatting and linting
- Establish development and deployment workflows

## Improvement Focus Areas

### Code Quality Improvements
1. **Error Handling**: Comprehensive error catching, logging, and user-friendly error messages
2. **Input Validation**: Type safety, data validation, and sanitization
3. **Code Readability**: Clear naming, documentation, and structure
4. **Testing Coverage**: Unit tests, integration tests, and edge case handling

### Performance Improvements
1. **Query Optimization**: Efficient database queries, indexing, and caching
2. **Resource Management**: Memory usage, connection pooling, and cleanup
3. **Load Optimization**: Lazy loading, code splitting, and asset optimization
4. **Monitoring**: Performance metrics, profiling, and alerting

### Maintainability Improvements
1. **Code Organization**: Clear separation of concerns and modular structure
2. **Configuration**: Environment-specific settings and feature flags
3. **Documentation**: API docs, inline comments, and setup instructions
4. **Dependency Management**: Version pinning, security updates, and compatibility

### Best Practice Improvements
1. **Security**: Input sanitization, authentication, and authorization
2. **Reliability**: Graceful degradation, retry logic, and circuit breakers
3. **Scalability**: Horizontal scaling, load balancing, and resource allocation
4. **Development Experience**: Tooling, automation, and developer workflows

## Deliverables

1. **Pattern Analysis Report** - document discovered improvement patterns
2. **Consistent Implementation** - code that follows existing patterns exactly
3. **Pattern Gap Documentation** - areas where new patterns were established
4. **Improvement Test Suite** - tests that verify pattern compliance and improvements
5. **Pattern Compliance Checklist** - verification that improvements match existing code style

## Red Flags - Pattern Violations

- Using different error handling mechanism than existing code
- Implementing different performance optimization approach than rest of project  
- Creating new improvement patterns instead of following established ones
- Adding conflicting libraries or dependencies for the same purpose
- Bypassing existing quality, performance, or maintenance mechanisms
- Introducing inconsistent coding standards or practices