# 작업 단위 가이드

## 📏 작업 크기 정의

### 레벨 1: 단일 함수/컴포넌트 (30분-1시간)

#### 유틸리티 함수

```javascript
// 이메일 검증 함수
"Create a function that validates email format:
- Accept email string as parameter
- Return true/false
- Handle edge cases (empty string, null)
- Follow RFC 5322 standard"

// 날짜 포맷 함수
"Create a date formatting utility:
- Input: Date object or timestamp
- Output: 'YYYY-MM-DD' format
- Handle timezone considerations
- Include unit tests"
```

#### 단일 React 컴포넌트

```javascript
// 버튼 컴포넌트
"Create a Button component:
- Props: label, onClick, variant (primary/secondary/danger)
- Loading state support
- Disabled state
- Tailwind CSS styling
- TypeScript props interface"

// 카드 컴포넌트
"Create a Card component:
- Header, body, footer slots
- Optional shadow and border
- Responsive padding
- Click handler support"
```

#### 단일 API 엔드포인트

```javascript
// 사용자 조회
"Create GET /api/users/:id endpoint:
- Fetch user by ID from database
- Return 404 if not found
- Include related data (profile)
- Add response caching headers"

// 상태 체크
"Create health check endpoint:
- Check database connection
- Check external service availability
- Return status and response time
- Format: { status: 'ok', services: {...} }"
```

### 레벨 2: 기능 모듈 (2-4시간)

#### 인증 모듈

```javascript
// 완전한 인증 모듈
"Create authentication module with:
- login(email, password) - returns token
- logout() - clears session
- isAuthenticated() - checks current status
- refreshToken() - renews expired token
- Store token securely (httpOnly cookie)
- Handle token expiration"

// 사용자 세션 관리
"Implement session management:
- Create session on login
- Session timeout after 30 min inactivity
- Refresh session on activity
- Multiple device session tracking
- Session revocation functionality"
```

#### 폼 시스템

```javascript
// 폼 컴포넌트 세트
"Create form component system:
- FormInput with validation display
- FormSelect with search capability
- FormTextarea with character count
- FormError component
- Form wrapper with validation logic
- Integrate with React Hook Form"

// 검증 시스템
"Build validation system:
- Email, phone, URL validators
- Custom validation rules
- Async validation support
- Error message localization
- Validation schema builder"
```

#### 데이터 테이블

```javascript
// 테이블 컴포넌트
"Create DataTable component:
- Column configuration
- Sorting functionality
- Pagination controls
- Row selection
- Search/filter capability
- Export to CSV feature"
```

### 레벨 3: 완전한 기능 (1-2일)

#### 사용자 관리 시스템

```javascript
// CRUD 전체 구현
"Implement complete user management:
Frontend:
- User list page with search and filters
- User detail modal
- Add/Edit user form with validation
- Bulk operations (delete, export)
- Role assignment UI

Backend:
- GET /api/users (paginated)
- GET /api/users/:id
- POST /api/users
- PUT /api/users/:id
- DELETE /api/users/:id
- Batch operations endpoint

Include error handling and loading states"
```

#### 파일 업로드 시스템

```javascript
// 완전한 파일 업로드
"Create file upload system:
- Drag & drop interface
- Multiple file selection
- Progress indicators
- File type validation
- Size restrictions (max 10MB)
- Image preview generation
- S3 integration for storage
- Database record creation
- Cleanup for failed uploads"
```

#### 알림 시스템

```javascript
// 실시간 알림
"Build notification system:
- Real-time notifications via WebSocket
- Notification types (info, warning, error)
- Persistent notification storage
- Mark as read functionality
- Notification preferences
- Email notification option
- Push notification support
- Notification history page"
```

## 🎯 스토리 포인트 할당 가이드

### 1 포인트 (2-4시간)

```markdown
특징:

- 단일 책임
- 명확한 입출력
- 외부 의존성 최소
- 엣지 케이스 적음

예시:

- "Add loading spinner to button"
- "Create formatCurrency utility"
- "Add validation to email field"
- "Update color scheme in header"
```

### 2 포인트 (4-8시간)

```markdown
특징:

- 2-3개 컴포넌트 연동
- 기본적인 상태 관리
- API 연결 포함
- 표준 에러 처리

예시:

- "Create login form with API integration"
- "Add sorting to data table"
- "Implement search functionality"
- "Create user profile card"
```

### 3 포인트 (1-2일)

```markdown
특징:

- 완전한 기능 단위
- 프론트엔드 + 백엔드
- 복잡한 비즈니스 로직
- 다양한 에러 시나리오

예시:

- "User registration flow"
- "Shopping cart functionality"
- "Comment system with replies"
- "Dashboard with multiple widgets"
```

### 5 포인트 (2-3일)

```markdown
특징:

- 시스템 간 통합
- 복잡한 상태 관리
- 성능 최적화 필요
- 광범위한 테스트 필요

예시:

- "Payment gateway integration"
- "Real-time collaboration feature"
- "Advanced search with filters"
- "Report generation system"
```

### 8 포인트 (3-5일)

```markdown
특징:

- 아키텍처 수준 변경
- 여러 시스템 연동
- 마이그레이션 포함
- 높은 복잡도

예시:

- "Microservice extraction"
- "Database migration system"
- "Complete authentication overhaul"
- "Multi-tenant implementation"
```

## 📋 구체적인 작업 분해 예시

### 이커머스 장바구니 기능 (5 포인트)

```markdown
## Main Task: Shopping Cart Implementation

### Subtask 1: Cart State Management (1 point)

"Create cart state management:

- Add/remove items
- Update quantities
- Calculate totals
- Persist to localStorage"

### Subtask 2: Cart API Endpoints (1 point)

"Create cart API:

- GET /api/cart
- POST /api/cart/items
- PUT /api/cart/items/:id
- DELETE /api/cart/items/:id"

### Subtask 3: Cart UI Components (2 points)

"Build cart components:

- CartIcon with item count
- CartDrawer slide-out panel
- CartItem component
- CartSummary with totals"

### Subtask 4: Integration & Testing (1 point)

"Complete cart integration:

- Connect UI to API
- Add optimistic updates
- Error handling
- E2E tests"
```

### 실시간 채팅 기능 (8 포인트)

```markdown
## Main Task: Real-time Chat System

### Subtask 1: WebSocket Infrastructure (2 points)

"Set up WebSocket server:

- Socket.io integration
- Connection management
- Room-based channels
- Reconnection logic"

### Subtask 2: Message Database Schema (1 point)

"Design message storage:

- Message table schema
- Indexes for performance
- Soft delete support
- Read receipts tracking"

### Subtask 3: Chat UI Components (2 points)

"Create chat interface:

- MessageList component
- MessageInput with typing indicator
- UserList sidebar
- ChatRoom container"

### Subtask 4: Real-time Features (2 points)

"Implement real-time features:

- Message delivery
- Typing indicators
- Online status
- Read receipts
- Message notifications"

### Subtask 5: History & Search (1 point)

"Add chat history features:

- Load previous messages
- Infinite scroll
- Message search
- Date separators"
```

## 🔧 작업 크기 추정 도구

### 복잡도 체크리스트

```markdown
작업 복잡도 평가:

□ 기술적 복잡도

- [ ] 새로운 기술 스택 필요
- [ ] 복잡한 알고리즘 구현
- [ ] 성능 최적화 필요
- [ ] 보안 고려사항 많음

□ 통합 복잡도

- [ ] 외부 서비스 연동
- [ ] 여러 시스템과 통신
- [ ] 데이터 마이그레이션
- [ ] 하위 호환성 유지

□ 비즈니스 복잡도

- [ ] 복잡한 비즈니스 규칙
- [ ] 많은 엣지 케이스
- [ ] 규정 준수 필요
- [ ] 다국어 지원

□ UI/UX 복잡도

- [ ] 복잡한 인터랙션
- [ ] 반응형 디자인
- [ ] 접근성 요구사항
- [ ] 애니메이션/전환효과
```

### 작업 분해 템플릿

```markdown
# Feature: [기능명]

## Total Estimate: [X] points

### Technical Tasks

- [ ] Database schema design (X points)
- [ ] API endpoint implementation (X points)
- [ ] Business logic layer (X points)

### Frontend Tasks

- [ ] UI component development (X points)
- [ ] State management setup (X points)
- [ ] API integration (X points)

### Quality Assurance

- [ ] Unit test coverage (X points)
- [ ] Integration tests (X points)
- [ ] E2E test scenarios (X points)

### Documentation

- [ ] API documentation (X points)
- [ ] User guide (X points)
- [ ] Technical documentation (X points)
```

## 📊 벨로시티 추적

### 스프린트 벨로시티 기록

```markdown
## Team Velocity Tracking

### Sprint 1

- Committed: 21 points
- Completed: 18 points
- Carry-over: 3 points
- Notes: Authentication took longer than expected

### Sprint 2

- Committed: 20 points
- Completed: 22 points
- Carry-over: 0 points
- Notes: Team getting familiar with codebase

### Sprint 3

- Committed: 22 points
- Completed: 21 points
- Carry-over: 1 point
- Notes: Stable velocity achieved

Average Velocity: 20.3 points/sprint
```

## ✅ 작업 추정 베스트 프랙티스

1. **과소평가 방지**

   - 테스트 작성 시간 포함
   - 코드 리뷰 시간 고려
   - 배포 및 모니터링 포함

2. **버퍼 시간 확보**

   - 예상치 못한 이슈 대응
   - 기술 부채 해결
   - 문서화 시간

3. **팀 합의**

   - Planning Poker 활용
   - 과거 데이터 참조
   - 지속적 조정

4. **명확한 완료 기준**
   - 코드 완성
   - 테스트 통과
   - 문서 업데이트
   - PR 승인
