# 효율적인 개발 단계

## 🚀 개발 프로세스 개요

### 1단계: 작은 단위로 시작

#### 기본 원칙

- 전체 프로젝트를 한 번에 요청하지 않기
- 독립적으로 테스트 가능한 컴포넌트부터 시작
- 각 단계별로 검증 후 진행

#### 예시: Express 서버 구축

```bash
# 나쁜 예
"Create a complete e-commerce backend with user management,
product catalog, order processing, and payment integration"

# 좋은 예 - 단계별 접근
Step 1: "Create a basic Express server with a health check endpoint"
Step 2: "Add middleware for CORS, body parsing, and error handling"
Step 3: "Implement user registration endpoint with validation"
Step 4: "Add JWT authentication middleware"
```

### 2단계: 점진적 기능 추가

#### 기존 코드베이스 위에 구축

```bash
# 컨텍스트 제공과 함께 요청
"Given the existing Express server in app.js,
add a user authentication middleware that:
- Validates JWT tokens
- Attaches user info to req.user
- Returns 401 for invalid tokens"
```

#### 통합 테스트 포함

```bash
"Add unit tests for the authentication middleware
using Jest and supertest, covering:
- Valid token scenarios
- Expired token handling
- Malformed token handling"
```

### 3단계: 컨텍스트 제공

#### 프로젝트 구조 설명

```bash
"Project structure:
- src/models/User.js contains Mongoose user schema
- src/middleware/ for all middleware functions
- Using ES6 modules (import/export)

Create a user controller with CRUD operations
following this structure and coding style"
```

### 4단계: 테스트 주도 개발

```bash
# 테스트 먼저 작성 요청
"Write Jest tests for a UserService class that should:
- Create new users with hashed passwords
- Validate unique email addresses
- Handle database errors gracefully

Then implement the UserService to pass these tests"
```

## 📝 효과적인 프롬프트 작성법

### 1. 구체적인 요구사항

#### ❌ 나쁜 예시

```
"Make a login page"
"Add authentication"
"Create a dashboard"
```

#### ✅ 좋은 예시

```
"Create a React login component with:
- Email and password input fields
- Client-side validation (email format, password minimum 8 chars)
- Loading state during submission
- Error message display
- Submit handler that posts to /api/auth/login
- Redirect to /dashboard on success
Using Tailwind CSS for styling and React Hook Form for form handling"
```

### 2. 기술적 제약사항 명시

```bash
"Implement the password reset feature:
- Use TypeScript with strict mode
- Follow existing ESLint configuration
- Compatible with Node.js 18+
- Use Prisma ORM for database operations
- Include JSDoc comments for all public methods
- Handle errors using the existing error middleware pattern"
```

### 3. 예상 결과 설명

```bash
"Create a data fetching hook that:
- Returns { data, error, isLoading } object
- Handles race conditions with cleanup
- Implements exponential backoff for retries
- Caches results for 5 minutes
- TypeScript generic for type safety

Example usage:
const { data, error, isLoading } = useAPI<User[]>('/api/users')"
```

## 🔄 반복적 개선 프로세스

### 초기 구현 → 리팩토링 → 최적화

#### Phase 1: 작동하는 코드

```bash
"Create a function that fetches user data from the API"
```

#### Phase 2: 에러 처리 추가

```bash
"Add error handling to the user fetching function:
- Network errors
- 404 responses
- Timeout after 10 seconds"
```

#### Phase 3: 성능 최적화

```bash
"Optimize the user fetching function:
- Add caching with 5-minute TTL
- Implement request deduplication
- Add loading and error states"
```

#### Phase 4: 타입 안정성

```bash
"Add TypeScript types to the user fetching function:
- Generic type for response data
- Proper error types
- Type guards for runtime validation"
```

## 🏗 실제 워크플로우 예시

### Full-Stack 기능 구현 (User Profile)

#### Step 1: 데이터 모델

```bash
"Create a Prisma schema for user profiles with:
- Basic info (name, bio, avatar)
- Social links (optional)
- Privacy settings
- Timestamps (createdAt, updatedAt)"
```

#### Step 2: API 엔드포인트

```bash
"Create Express routes for user profile:
GET /api/profile/:userId - Public profile view
GET /api/profile - Get own profile (authenticated)
PUT /api/profile - Update own profile
Include validation middleware and error handling"
```

#### Step 3: 프론트엔드 컴포넌트

```bash
"Create a ProfileForm React component:
- Form fields matching the profile schema
- Image upload for avatar
- Real-time validation
- Optimistic updates
- Success/error notifications"
```

#### Step 4: 통합 및 테스트

```bash
"Create integration tests for the profile feature:
- Test complete flow from form submission to database
- Test validation errors
- Test authorization (can only edit own profile)
- Test image upload handling"
```

## 🛡 코드 품질 관리

### 1. 코드 리뷰 요청

```bash
"Review this authentication middleware for:
- Security vulnerabilities
- Performance issues
- Error handling completeness
- Code style consistency
Suggest improvements with explanations"
```

### 2. 리팩토링 요청

```bash
"Refactor this component to:
- Extract business logic to custom hooks
- Improve type safety
- Reduce cognitive complexity
- Follow SOLID principles
Maintain all existing functionality"
```

### 3. 성능 최적화

```bash
"Optimize this React component for performance:
- Identify unnecessary re-renders
- Implement proper memoization
- Lazy load heavy dependencies
- Optimize bundle size
Provide before/after comparison"
```

## 📊 진행 상황 추적

### Git 커밋 전략

```bash
# 기능별 브랜치
git checkout -b feature/user-authentication

# 의미있는 커밋 메시지
git commit -m "feat: add JWT authentication middleware"
git commit -m "test: add auth middleware unit tests"
git commit -m "docs: update API documentation for auth endpoints"
```

### 문서화 요청

```bash
"Add comprehensive documentation:
- JSDoc comments for all functions
- README with setup instructions
- API endpoint documentation
- Architecture decision records (ADRs)"
```

## ✅ 개발 단계 체크리스트

각 기능 구현 시 확인사항:

- [ ] 요구사항 명확히 정의
- [ ] 작은 단위로 작업 분해
- [ ] 각 단계별 테스트 작성
- [ ] 코드 리뷰 수행
- [ ] 문서화 완료
- [ ] 성능 최적화 검토
- [ ] 보안 취약점 점검
- [ ] 에러 처리 확인

---

다음: [애자일 개발 전략](./agile-strategy.md) →
