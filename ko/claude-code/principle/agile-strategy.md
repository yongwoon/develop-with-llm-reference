# 애자일 개발 전략

## 🌊 불확실성 관리

### User Story 기반 접근

#### 기술 명세 대신 가치 중심으로

```bash
# 기술 중심 접근 (피하기)
"Create a PostgreSQL table with user fields and indexes"

# User Story 중심 접근 (권장)
"As a user, I want to create an account
so that I can save my preferences and order history

Acceptance Criteria:
- User can sign up with email/password
- Email verification is required
- Profile is created automatically after signup"
```

#### Claude에게 해결책 제안 요청

```bash
"Given this user story: [User Story 내용]
Suggest:
1. Technical implementation approach
2. Required components
3. Potential challenges
4. MVP vs full feature comparison"
```

### MVP(Minimum Viable Product) 우선

#### 단계별 기능 확장

```markdown
## Sprint 1: Basic Authentication (MVP)

"Create simple email/password login:

- No social login
- Basic session management
- Simple error messages"

## Sprint 2: Enhanced Security

"Add to existing auth:

- Password strength requirements
- Account lockout after failed attempts
- Session timeout"

## Sprint 3: User Experience

"Enhance auth flow:

- Social login options
- Remember me functionality
- Password reset flow"
```

### 탐색적 프로토타이핑

```bash
# 불확실한 요구사항 탐색
"Create 3 different UI prototypes for the dashboard:
1. Card-based layout with summary metrics
2. Table-focused design for data analysis
3. Visual charts and graphs approach

Each should handle the same data but present differently"

# 기술적 접근 방법 탐색
"Implement user notifications using 3 approaches:
1. WebSocket implementation
2. Server-Sent Events
3. Polling mechanism

Include pros/cons and resource usage for each"
```

## 📅 스프린트 계획 및 실행

### Sprint 0: Discovery & Setup

```markdown
## Week 1: Discovery Sprint

### Day 1-2: 기술 검증

"Create proof of concepts for:

- Authentication flow with NextAuth
- Database connection with Prisma
- Real-time updates with Socket.io"

### Day 3-4: UI/UX 탐색

"Create wireframes for main user flows:

- Onboarding process
- Main dashboard
- Key feature interactions"

### Day 5: 아키텍처 결정

"Based on POCs, create:

- System architecture diagram
- Technology stack decision document
- Development environment setup guide"
```

### Sprint 1-2: 핵심 기능 구현

```markdown
## Sprint 1: Foundation (Week 2-3)

### User Authentication Epic

Day 1-3: "Implement basic auth:

- Registration with email verification
- Login/logout functionality
- Protected route wrapper"

Day 4-5: "Add user profile:

- Profile creation after registration
- Basic profile edit functionality
- Avatar upload"

### Sprint Review & Planning

"Create demo for:

- User registration flow
- Login and access protected area
- Basic profile management"
```

### 일일 스탠드업 활용

```bash
# Yesterday's Work
"Implemented user registration API endpoint
Blocker: Email service configuration"

# Today's Plan - Claude Request
"Help me implement email service:
- Use SendGrid API
- Template for verification emails
- Queue system for reliability
- Error handling and retry logic"

# Impediments Resolution
"The email service is failing with rate limit errors
Suggest solutions for:
- Implementing queue with Bull
- Rate limiting strategy
- Fallback email provider"
```

## 🔄 반복적 개선 전략

### 기능별 점진적 개선

```markdown
## Task List Feature Evolution

### Iteration 1: Basic Functionality

"Create a simple task list component:

- Add new tasks
- Display task list
- Delete tasks"

### Iteration 2: Task Status

"Enhance task list with:

- Checkbox to mark complete
- Visual distinction for completed tasks
- Task count summary"

### Iteration 3: Task Organization

"Add task management features:

- Priority levels (High, Medium, Low)
- Due dates
- Category tags"

### Iteration 4: Advanced Features

"Implement productivity features:

- Drag-and-drop reordering
- Bulk operations
- Keyboard shortcuts
- Task templates"
```

### 스파이크를 통한 기술 탐색

```bash
# 기술적 불확실성 해결
"Research spike: Implement real-time collaboration
Time-boxed to 1 day, explore:
- Operational Transformation approach
- CRDT implementation
- Simple locking mechanism

Provide recommendation with POC code"
```

## 📊 스토리 포인트 및 추정

### 작업 크기 기준

```markdown
## Story Point Reference

### 1 Point - 2-4 hours

- Simple UI component
- Basic CRUD endpoint
- Utility function
- Minor bug fix

Example: "Create a LoadingSpinner component"

### 2 Points - 4-8 hours

- Complex component with state
- API endpoint with validation
- Integration between components
- Unit test suite

Example: "Implement form with validation"

### 3 Points - 1-2 days

- Complete feature slice
- Multiple integrated components
- Database schema changes
- Complex business logic

Example: "User profile management"

### 5 Points - 2-3 days

- Multi-step workflows
- Third-party integrations
- Performance optimizations
- System refactoring

Example: "Payment processing integration"

### 8 Points - 3-5 days

- Major architectural changes
- Complex features with many edge cases
- Full subsystem implementation

Example: "Real-time notification system"
```

## 🎯 불확실성 대응 패턴

### 1. 인터페이스 우선 설계

```typescript
// 구현 전 인터페이스 정의
"Define TypeScript interfaces for a user management system:
- User entity
- Repository interface
- Service layer interface
- API response types

Don't implement yet, just define contracts"
```

### 2. Mock 데이터 활용

```bash
"Create mock API responses for:
- User CRUD operations
- Product catalog
- Order processing

Use realistic data that covers edge cases
Include delay simulation for loading states"
```

### 3. Feature Toggle 구현

```bash
"Implement feature toggle system:
- Environment-based flags
- User-specific flags
- Gradual rollout capability
- Runtime toggle without deploy"
```

### 4. A/B 테스트 준비

```bash
"Set up A/B testing framework:
- User segmentation logic
- Metric tracking
- Results analysis
- Easy experiment creation"
```

## 🔍 피드백 루프 최적화

### 빠른 프로토타입 → 검증 → 개선

```markdown
## Rapid Prototyping Cycle

### Hour 1-2: Quick Prototype

"Create basic working version of [feature]
Focus on happy path only"

### Hour 3: User Feedback

- Demo to stakeholders
- Collect immediate feedback
- Identify missing requirements

### Hour 4-8: Iterate

"Based on feedback:

- Add error handling
- Improve UX
- Handle edge cases"
```

### 지속적 개선 요청

```bash
# Week 1: Basic Implementation
"Create user dashboard with mock data"

# Week 2: Real Data Integration
"Connect dashboard to actual API endpoints"

# Week 3: Performance
"Optimize dashboard rendering:
- Implement virtual scrolling
- Add pagination
- Cache API responses"

# Week 4: Polish
"Add finishing touches:
- Loading skeletons
- Error boundaries
- Empty states
- Animations"
```

## ✅ 애자일 실천 체크리스트

스프린트별 확인사항:

### Sprint Planning

- [ ] User stories가 명확한 가치를 제공하는가?
- [ ] Acceptance criteria가 테스트 가능한가?
- [ ] 기술적 불확실성을 식별했는가?
- [ ] 스파이크가 필요한 항목을 정했는가?

### Daily Execution

- [ ] 작은 단위로 작업을 분해했는가?
- [ ] 매일 배포 가능한 증분을 만들었는가?
- [ ] 블로커를 빠르게 해결했는가?
- [ ] 팀과 진행상황을 공유했는가?

### Sprint Review

- [ ] 작동하는 소프트웨어를 시연했는가?
- [ ] 사용자 피드백을 수집했는가?
- [ ] 다음 우선순위를 조정했는가?
- [ ] 개선사항을 문서화했는가?

---

다음: [작업 단위 가이드](./task-units.md) →
