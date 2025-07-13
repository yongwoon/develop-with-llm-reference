# Feature Specification Writing Guide

## 📂 Document Structure Strategy

### Hierarchical Document Structure

```
/specifications
├── /overview (Overall Overview)
│   ├── product-vision.md
│   ├── system-architecture.md
│   ├── tech-stack.md
│   └── api-standards.md
│
├── /domains (Domain-specific Specifications)
│   ├── /user-management
│   │   ├── README.md (Module Overview)
│   │   ├── user-registration.md
│   │   ├── authentication.md
│   │   ├── authorization.md
│   │   └── profile-management.md
│   │
│   ├── /product-catalog
│   │   ├── README.md
│   │   ├── product-listing.md
│   │   ├── search-filtering.md
│   │   └── inventory-management.md
│   │
│   └── /order-processing
│       ├── README.md
│       ├── shopping-cart.md
│       ├── checkout-flow.md
│       └── payment-integration.md
│
├── /integrations (External Integrations)
│   ├── payment-gateway.md
│   ├── shipping-providers.md
│   └── analytics-services.md
│
└── /technical (Technical Documentation)
    ├── database-schema.md
    ├── api-documentation.md
    └── deployment-guide.md
```

## 📄 Document Templates

### Product Overview Template

```markdown
# [Product Name] Product Specification Overview

## Vision Statement

[Describe the product's vision and purpose in 1-2 paragraphs]

## Target Users

- **Primary Users**: [Primary user group]
- **Secondary Users**: [Secondary user group]

## Core Features

1. **[Feature Name]**: [Brief description]
2. **[Feature Name]**: [Brief description]
3. **[Feature Name]**: [Brief description]

## System Architecture

[Architecture diagram or description]

## Technology Stack

- **Frontend**: [Technology stack]
- **Backend**: [Technology stack]
- **Database**: [Technology stack]
- **Infrastructure**: [Technology stack]

## Project Timeline

- **Phase 1**: [Timeline] - [Goal]
- **Phase 2**: [Timeline] - [Goal]
- **Phase 3**: [Timeline] - [Goal]

## Success Metrics

- [Measurable success indicator]
- [Measurable success indicator]
```

### Module Overview Template

````markdown
# [Module Name] Module Specification

## Module Overview

[Describe the module's purpose and scope]

## Dependencies

- **Internal**: [Internal dependencies]
- **External**: [External dependencies]

## Key Features

| Feature        | Description   | Priority        |
| -------------- | ------------- | --------------- |
| [Feature Name] | [Description] | High/Medium/Low |

## Data Model

```yaml
User:
  - id: UUID
  - email: String (unique)
  - createdAt: DateTime
```
````

## API Endpoints

| Method | Endpoint   | Description     |
| ------ | ---------- | --------------- |
| GET    | /api/users | List all users  |
| POST   | /api/users | Create new user |

## Module Interactions

[Interaction diagram with other modules]

## Security Considerations

- [Security considerations]
- [Authentication/authorization requirements]

````

### Feature Detail Specification Template

```markdown
# Feature: [Feature Name]

## Status
- **Status**: Draft | Review | Approved | Development | Complete
- **Version**: 1.0
- **Last Updated**: YYYY-MM-DD
- **Owner**: [Owner]

## Overview
[Brief description of the feature - 1 paragraph]

## User Story
````

As a [user type]
I want to [action]
So that [benefit/value]

````

## Acceptance Criteria
- [ ] [Verifiable condition 1]
- [ ] [Verifiable condition 2]
- [ ] [Verifiable condition 3]

## User Flow
1. User navigates to [page/section]
2. User clicks on [button/link]
3. System displays [response]
4. User enters [data]
5. System validates and [action]

## UI/UX Requirements
### Desktop View
[Wireframe or mockup]

### Mobile View
[Wireframe or mockup]

### Component List
- `[ComponentName]`: [Purpose]
- `[ComponentName]`: [Purpose]

## Technical Implementation

### API Specification
```yaml
endpoint: POST /api/[resource]
request:
  headers:
    Authorization: Bearer {token}
  body:
    field1: string (required)
    field2: number (optional)
response:
  200:
    success: true
    data: {...}
  400:
    error: "Validation error"
````

### Business Rules

1. [Business rule 1]
2. [Business rule 2]

### Validation Rules

- **Field1**: Required, min 3 chars, max 50 chars
- **Field2**: Optional, must be positive number

### Error Handling

| Error Case    | Status Code | Message                | User Action       |
| ------------- | ----------- | ---------------------- | ----------------- |
| Invalid input | 400         | "Invalid email format" | Show inline error |
| Unauthorized  | 401         | "Please login"         | Redirect to login |

## Performance Requirements

- **Response Time**: < 200ms
- **Concurrent Users**: Support 1000+
- **Data Volume**: Handle 10k records

## Security Requirements

- [ ] Input sanitization
- [ ] SQL injection prevention
- [ ] XSS protection
- [ ] Rate limiting

## Testing Scenarios

### Unit Tests

- [ ] Validation logic
- [ ] Business rule enforcement

### Integration Tests

- [ ] API endpoint functionality
- [ ] Database operations

### E2E Tests

- [ ] Complete user flow
- [ ] Error scenarios

## Dependencies

- **Internal**: [AUTH-001] Authentication Module
- **External**: SendGrid Email Service

## Non-Functional Requirements

- **Accessibility**: WCAG 2.1 Level AA
- **Browser Support**: Chrome, Firefox, Safari, Edge (latest 2 versions)
- **Localization**: Support EN, KO, JA

## Open Questions

- [ ] [Undecided item 1]
- [ ] [Undecided item 2]

## Change Log

| Date       | Version | Changes       | Author |
| ---------- | ------- | ------------- | ------ |
| YYYY-MM-DD | 1.0     | Initial draft | [Name] |

````

## 📏 Document Size Guidelines

### Recommended Document Sizes

| Document Type | Recommended Size | Page Count | Word Count |
|---------------|------------------|------------|------------|
| Product Overview | Concise | 2-3 | 500-1,000 |
| Module Specification | Detailed | 5-10 | 1,500-3,000 |
| Feature Detail | Medium | 3-5 | 800-1,500 |
| API Specification | Technical | 1-2/endpoint | 200-400/endpoint |

### Document Separation Criteria

```markdown
## When to Split into New Documents:

1. **Size Criteria**
   - Single document exceeds 10 pages
   - Exceeds 3,000 words
   - 5+ independent sections

2. **Scope Criteria**
   - Feature that can be developed independently
   - Area managed by different teams
   - Scheduled for separate sprints

3. **Change Frequency**
   - Frequently updated sections
   - Separate from stable parts
````

## 🔄 Integration with Claude Code

### Progressive Refinement Example

```markdown
## Sprint 1: Basic Specification

### User Login

- Basic email/password authentication
- Session management
- Error messages

## Sprint 3: Enhanced Details

### User Login (Enhanced)

Authentication:

- Email format validation: RFC 5322
- Password requirements:
  - Minimum 8 characters
  - At least 1 uppercase, 1 number
- Show/hide password toggle

Security:

- Max 5 login attempts
- 15-minute account lockout
- CAPTCHA after 3 failed attempts

Session:

- JWT token (15min access, 7day refresh)
- Secure httpOnly cookies
- Device fingerprinting
```

### Context for Claude Prompts

```markdown
# Context for Claude Code

## Current Implementation

- See: [user-authentication.md](./specs/user-authentication.md)
- Database: PostgreSQL with Prisma ORM
- Auth: JWT with refresh tokens

## Task

Implement the password reset flow as specified in [password-reset.md]

## Constraints

- Use existing email service (SendGrid)
- Follow project ESLint rules
- Include unit tests
```

## 📑 Document Management System

### Version Control

```markdown
# Document Header

---

id: AUTH-001
title: User Authentication
version: 2.1
status: In Development
last_updated: 2024-03-15
owner: Backend Team
reviewers:

- Security Team
- Frontend Team

---

## Version History

| Version | Date       | Changes               | Author |
| ------- | ---------- | --------------------- | ------ |
| 1.0     | 2024-01-15 | Initial specification | John   |
| 2.0     | 2024-02-20 | Added OAuth support   | Sarah  |
| 2.1     | 2024-03-15 | Security enhancements | Mike   |
```

### Cross-References

```markdown
## Related Documents

### Dependencies

- ⬆️ Depends on: [USER-001] User Model
- ⬆️ Depends on: [SEC-001] Security Standards

### Dependents

- ⬇️ Required by: [PROFILE-001] User Profile
- ⬇️ Required by: [ORDER-001] Order Processing

### See Also

- 📖 [API Documentation](../api/auth-endpoints.md)
- 🏗️ [System Architecture](../architecture/overview.md)
- 🔒 [Security Guidelines](../security/guidelines.md)
```

## 🎯 Effective Specification Writing Tips

### 1. Clarity

```markdown
❌ Bad Example:
"User should be able to login"

✅ Good Example:
"User should be able to login using registered email and password.

- Email validation is case-insensitive
- Account locked for 15 minutes after 5 failed attempts
- Redirect to dashboard on success"
```

### 2. Measurability

```markdown
❌ Bad Example:
"Fast response time"

✅ Good Example:
"API response time:

- 95 percentile: < 200ms
- 99 percentile: < 500ms
- Maximum: < 1000ms"
```

### 3. Completeness

```markdown
## Checklist for Complete Specification

- [ ] User story with clear value
- [ ] Acceptance criteria (testable)
- [ ] UI/UX mockups or wireframes
- [ ] API contracts
- [ ] Error scenarios
- [ ] Performance requirements
- [ ] Security considerations
- [ ] Testing approach
```

## ✅ Document Quality Checklist

### Items to Verify Upon Completion

- [ ] Are all requirements clear and unambiguous?
- [ ] Is technical implementation feasible?
- [ ] Are dependencies clearly defined?
- [ ] Are success criteria measurable?
- [ ] Are edge cases considered?
- [ ] Are security requirements included?
- [ ] Has it been reviewed by relevant teams?

---

[← Previous: Task Unit Guide](./task-units.md) | [Back to Home →](./README.md)
