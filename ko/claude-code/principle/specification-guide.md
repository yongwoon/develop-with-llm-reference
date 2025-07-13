# 기능 명세서 작성법

## 📂 문서 구조화 전략

### 계층적 문서 구조

```
/specifications
├── /overview (전체 개요)
│   ├── product-vision.md
│   ├── system-architecture.md
│   ├── tech-stack.md
│   └── api-standards.md
│
├── /domains (도메인별 명세)
│   ├── /user-management
│   │   ├── README.md (모듈 개요)
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
├── /integrations (외부 연동)
│   ├── payment-gateway.md
│   ├── shipping-providers.md
│   └── analytics-services.md
│
└── /technical (기술 문서)
    ├── database-schema.md
    ├── api-documentation.md
    └── deployment-guide.md
```

## 📄 문서 템플릿

### 제품 전체 개요 템플릿

```markdown
# [제품명] Product Specification Overview

## Vision Statement

[제품의 비전과 목적을 1-2문단으로 설명]

## Target Users

- **Primary Users**: [주요 사용자 그룹]
- **Secondary Users**: [부가 사용자 그룹]

## Core Features

1. **[기능명]**: [간단한 설명]
2. **[기능명]**: [간단한 설명]
3. **[기능명]**: [간단한 설명]

## System Architecture

[아키텍처 다이어그램 또는 설명]

## Technology Stack

- **Frontend**: [기술 스택]
- **Backend**: [기술 스택]
- **Database**: [기술 스택]
- **Infrastructure**: [기술 스택]

## Project Timeline

- **Phase 1**: [일정] - [목표]
- **Phase 2**: [일정] - [목표]
- **Phase 3**: [일정] - [목표]

## Success Metrics

- [측정 가능한 성공 지표]
- [측정 가능한 성공 지표]
```

### 모듈별 개요 템플릿

````markdown
# [모듈명] Module Specification

## Module Overview

[모듈의 목적과 범위를 설명]

## Dependencies

- **Internal**: [내부 의존성]
- **External**: [외부 의존성]

## Key Features

| Feature  | Description | Priority        |
| -------- | ----------- | --------------- |
| [기능명] | [설명]      | High/Medium/Low |

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

[다른 모듈과의 상호작용 다이어그램]

## Security Considerations

- [보안 고려사항]
- [인증/인가 요구사항]

````

### 기능 상세 명세 템플릿

```markdown
# Feature: [기능명]

## Status
- **Status**: Draft | Review | Approved | Development | Complete
- **Version**: 1.0
- **Last Updated**: YYYY-MM-DD
- **Owner**: [담당자]

## Overview
[기능에 대한 간단한 설명 - 1문단]

## User Story
````

As a [user type]
I want to [action]
So that [benefit/value]

````

## Acceptance Criteria
- [ ] [검증 가능한 조건 1]
- [ ] [검증 가능한 조건 2]
- [ ] [검증 가능한 조건 3]

## User Flow
1. User navigates to [page/section]
2. User clicks on [button/link]
3. System displays [response]
4. User enters [data]
5. System validates and [action]

## UI/UX Requirements
### Desktop View
[와이어프레임 또는 목업]

### Mobile View
[와이어프레임 또는 목업]

### Component List
- `[ComponentName]`: [용도]
- `[ComponentName]`: [용도]

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

1. [비즈니스 규칙 1]
2. [비즈니스 규칙 2]

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

- [ ] [미결정 사항 1]
- [ ] [미결정 사항 2]

## Change Log

| Date       | Version | Changes       | Author |
| ---------- | ------- | ------------- | ------ |
| YYYY-MM-DD | 1.0     | Initial draft | [Name] |

````

## 📏 문서 크기 가이드라인

### 권장 문서 크기

| 문서 타입 | 권장 크기 | 페이지 수 | 단어 수 |
|----------|----------|-----------|---------|
| 제품 개요 | 간결함 | 2-3 | 500-1,000 |
| 모듈 명세 | 상세함 | 5-10 | 1,500-3,000 |
| 기능 상세 | 중간 | 3-5 | 800-1,500 |
| API 명세 | 기술적 | 1-2/endpoint | 200-400/endpoint |

### 문서 분할 기준

```markdown
## 새 문서로 분리해야 할 때:

1. **크기 기준**
   - 단일 문서가 10페이지 초과
   - 3,000 단어 초과
   - 5개 이상의 독립적 섹션

2. **범위 기준**
   - 독립적으로 개발 가능한 기능
   - 다른 팀이 담당하는 영역
   - 별도 스프린트 구현 예정

3. **변경 빈도**
   - 자주 업데이트되는 부분
   - 안정적인 부분과 분리
````

## 🔄 Claude Code와의 연동

### 점진적 상세화 예시

```markdown
## Sprint 1: 기본 명세

### User Login

- Basic email/password authentication
- Session management
- Error messages

## Sprint 3: 상세 추가

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

### Claude 프롬프트용 컨텍스트

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

## 📑 문서 관리 시스템

### 버전 관리

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

### 상호 참조

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

## 🎯 효과적인 명세 작성 팁

### 1. 명확성

```markdown
❌ 나쁜 예:
"사용자는 로그인할 수 있어야 한다"

✅ 좋은 예:
"사용자는 등록된 이메일과 비밀번호를 입력하여 로그인할 수 있어야 한다.

- 이메일은 대소문자 구분 없이 검증
- 5회 실패 시 15분간 계정 잠금
- 성공 시 대시보드로 리다이렉트"
```

### 2. 측정 가능성

```markdown
❌ 나쁜 예:
"빠른 응답 시간"

✅ 좋은 예:
"API 응답 시간:

- 95 percentile: < 200ms
- 99 percentile: < 500ms
- Maximum: < 1000ms"
```

### 3. 완전성

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

## ✅ 문서 품질 체크리스트

### 작성 완료 시 확인사항

- [ ] 모든 요구사항이 명확하고 모호하지 않은가?
- [ ] 기술적 구현이 가능한가?
- [ ] 의존성이 명확히 정의되었는가?
- [ ] 성공 기준이 측정 가능한가?
- [ ] 엣지 케이스가 고려되었는가?
- [ ] 보안 요구사항이 포함되었는가?
- [ ] 관련 팀의 리뷰를 받았는가?

---

[← 이전: 작업 단위 가이드](./task-units.md) | [처음으로 →](./README.md)
