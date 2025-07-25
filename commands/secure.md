---
allowed-tools: [Read, Edit, MultiEdit, Write, Bash, Grep, Glob, LS, TodoWrite]
description: Secures features by first discovering and applying existing project security patterns
argument-hint: <feature or functionality to secure>
---

You are securing: $ARGUMENTS

## Pattern-First Security Approach

**Step 1: Discover Existing Security Patterns**

Before implementing anything, analyze how THIS project handles security:

### Authentication Patterns
Search the codebase for authentication-related terms and patterns. Use tools like Grep to find:
- Authentication implementations (login, authenticate, auth tokens)
- Authentication middleware or guards
- Session or token management

**Analyze discovered patterns:**
- What authentication mechanism does the project use?
- Where are authentication checks enforced?
- How is user identity maintained across requests?

### Authorization Patterns  
Search for role and permission management in the existing code:
- Role-based access control implementations
- Permission checking logic
- Admin-only feature protection

**Analyze discovered patterns:**
- How does the project determine user permissions?
- Where are authorization checks performed?
- What does the user/role data structure look like?

### Input Validation Patterns
Look for existing validation approaches in the codebase:
- Input validation libraries and schemas
- ID format validation (UUID, numeric, custom)
- Data sanitization implementations

**Analyze discovered patterns:**
- What validation approach does the project use?
- How are different data types validated?
- Where does validation occur in the request flow?

### Data Protection Patterns
Search for security measures already implemented:
- Password hashing and encryption
- Data sanitization and escaping
- Database query construction methods

**Analyze discovered patterns:**
- How does the project protect sensitive data?
- What encryption or hashing methods are used?
- How are database queries constructed safely?

## Step 2: Apply Project Patterns

Based on discovered patterns, implement security CONSISTENTLY:

### Admin Access Control Pattern
If you discover the project has admin-only features (dashboards, management interfaces), analyze:
- How are admin routes protected? 
- What role checking logic is used?
- Where are these checks implemented?

**Apply the same pattern:** When adding new admin functionality, use the exact same access control mechanism. Don't create a new way to check admin permissions - follow the established pattern.

### ID Validation Pattern  
If you find the project validates identifiers in a specific format (UUIDs, numeric IDs, custom formats):
- What validation rules are applied?
- Which validation library or method is used?
- Where does this validation occur?

**Apply the same pattern:** When your new feature accepts IDs, use the identical validation approach. If existing features validate UUIDs, your feature should too.

### Authentication Flow Pattern
If you discover how the project handles user authentication:
- What authentication mechanism is used?
- How are protected routes secured?
- What middleware or guards are applied?

**Apply the same pattern:** New features requiring authentication should use the same flow, middleware, and security checks as existing protected features.

## Step 3: Pattern Consistency Check

After implementation, verify consistency:

### Authentication Consistency
- [ ] Uses same auth mechanism as existing admin features
- [ ] Follows same token/session validation pattern
- [ ] Implements same auth error handling

### Authorization Consistency  
- [ ] Uses same role/permission checking logic
- [ ] Follows same access control patterns
- [ ] Implements same authorization error responses

### Validation Consistency
- [ ] Uses same validation library and patterns
- [ ] Follows same ID format validation (UUID, etc.)
- [ ] Implements same input sanitization approach

### Error Handling Consistency
- [ ] Returns same error format as existing endpoints
- [ ] Uses same status codes for security violations
- [ ] Follows same logging pattern for security events

## Step 4: Fill Pattern Gaps

**Only if no existing patterns found**, implement these fallbacks:

### Missing Auth Pattern
- Choose and implement a consistent authentication mechanism
- Add protection for routes requiring authentication
- Create user context management

### Missing Authorization Pattern  
- Design role-based or permission-based access control
- Implement consistent permission checking
- Add protection for admin or privileged features

### Missing Validation Pattern
- Choose input validation approach and library
- Implement consistent ID format validation
- Add data sanitization for user inputs

### Missing Data Protection
- Implement secure password handling
- Use parameterized database queries
- Add protection against common web vulnerabilities

## Deliverables

1. **Pattern Analysis Report** - document discovered security patterns
2. **Consistent Implementation** - code that follows existing patterns exactly
3. **Pattern Gap Documentation** - areas where new patterns were needed
4. **Security Test Suite** - tests that verify pattern compliance
5. **Pattern Compliance Checklist** - verification that implementation matches existing code

## Red Flags - Pattern Violations

- Using different authentication mechanism than existing protected features
- Implementing different validation approach than rest of project  
- Creating new security patterns instead of following established ones
- Adding conflicting security libraries or dependencies
- Bypassing existing security middleware or protection mechanisms