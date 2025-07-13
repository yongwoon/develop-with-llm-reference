# Cursor 기본 사용법

## 📥 설치 및 초기 설정

### 1. Cursor 설치

```bash
# macOS
brew install --cask cursor

# 또는 공식 웹사이트에서 다운로드
# https://cursor.sh/
```

### 2. 초기 설정

#### 계정 연결

- Cursor 실행 후 계정 생성 또는 로그인
- GitHub 계정 연동 권장 (프로젝트 컨텍스트 향상)

#### 기본 설정

- **Language**: 한국어 설정 (선택사항)
- **Theme**: 선호하는 테마 선택
- **Font**: 코딩 폰트 설정 (Fira Code, JetBrains Mono 등)

## 🎯 핵심 기능

### 1. AI 자동완성 (Tab)

```typescript
// 타이핑 중 Tab 키로 AI 제안 수용
function calculateTotal(items: Product[]) {
  // Tab 키 - AI가 자동으로 완성
  return items.reduce((sum, item) => sum + item.price, 0);
}
```

### 2. 채팅 인터페이스 (Cmd+L)

```bash
# 채팅창에서 자연어로 요청
"Create a React component for user profile card with avatar, name, and bio"

# 코드 설명 요청
"Explain this function and suggest improvements"

# 버그 수정 요청
"Fix the performance issue in this component"
```

### 3. 코드 편집 (Cmd+K)

```bash
# 선택한 코드 블록 수정
"Convert this to TypeScript"
"Add error handling"
"Optimize for performance"
"Add comprehensive comments"
```

## ⌨️ 필수 단축키

### 기본 단축키

- **Cmd+L**: 새 채팅 시작
- **Cmd+K**: 인라인 코드 편집
- **Cmd+I**: 코드 생성 (작업 중인 파일에)
- **Tab**: AI 제안 수용
- **Esc**: AI 제안 취소

### 고급 단축키

- **Cmd+Shift+L**: 채팅 히스토리
- **Cmd+/**: 빠른 질문
- **Cmd+Enter**: 선택 영역을 채팅에 추가
- **Cmd+Shift+Enter**: 전체 파일을 채팅에 추가

## 🔧 프로젝트 설정

### 1. 프로젝트 루트에 .cursorrules 파일 생성

```bash
# .cursorrules 파일 예시
You are an expert TypeScript and React developer.

## Project Context
- Framework: Next.js 14 with App Router
- Language: TypeScript with strict mode
- Styling: Tailwind CSS
- State Management: Zustand
- Database: PostgreSQL with Prisma

## Code Style
- Use functional components with hooks
- Prefer const assertions and type safety
- Use descriptive variable names
- Add JSDoc comments for public functions
- Follow Next.js best practices

## File Structure
src/
├── app/           # Next.js App Router
├── components/    # Reusable UI components
├── hooks/         # Custom React hooks
├── lib/           # Utility functions
├── types/         # TypeScript type definitions
└── utils/         # Helper functions
```

### 2. 프로젝트별 설정

#### package.json 확인

```json
{
  "name": "my-project",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "test": "jest",
    "lint": "eslint .",
    "type-check": "tsc --noEmit"
  }
}
```

#### tsconfig.json 최적화

```json
{
  "compilerOptions": {
    "strict": true,
    "noImplicitAny": true,
    "strictNullChecks": true,
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

## 💬 효과적인 프롬프트 작성법

### 1. 구체적인 요구사항

```bash
# ❌ 모호한 요청
"Make a login form"

# ✅ 구체적인 요청
"Create a React login form component with:
- Email and password fields
- Form validation using Zod
- Submit handler with loading state
- Error message display
- Tailwind CSS styling
- TypeScript types"
```

### 2. 컨텍스트 제공

```bash
# 현재 프로젝트 구조 설명
"Given our Next.js project structure with:
- App Router
- Prisma for database
- NextAuth for authentication

Create a protected route wrapper component that:
- Checks authentication status
- Redirects to login if not authenticated
- Shows loading spinner during check"
```

### 3. 예시 코드 제공

````bash
# 기존 코드 스타일 참조
"Following the pattern used in components/ui/Button.tsx:

```typescript
// 기존 Button 컴포넌트 스타일
````

Create a similar Input component with validation states"

````

## 🎨 인터페이스 이해

### 1. 편집기 영역
- **메인 에디터**: 코드 작성 및 편집
- **AI 제안 오버레이**: 실시간 자동완성 표시
- **인라인 편집**: Cmd+K로 활성화되는 편집 모드

### 2. 사이드바
- **파일 탐색기**: 프로젝트 파일 구조
- **검색**: 파일 및 코드 검색
- **Git 연동**: 버전 관리 상태

### 3. 채팅 패널
- **대화 히스토리**: 이전 채팅 기록
- **코드 블록**: 생성된 코드 미리보기
- **적용 버튼**: 제안된 코드 적용

## 🚀 시작하기 워크플로우

### 1. 새 프로젝트 설정
```bash
# 1. 프로젝트 생성
npx create-next-app@latest my-project --typescript --tailwind --app

# 2. Cursor로 프로젝트 열기
cursor my-project

# 3. .cursorrules 파일 생성
# 4. 프로젝트 구조 설명 채팅
````

### 2. 첫 번째 컴포넌트 생성

```bash
# 채팅에서 요청
"Create a header component with:
- Logo on the left
- Navigation menu in the center
- User profile dropdown on the right
- Responsive design
- TypeScript with proper types"
```

### 3. 기능 구현

```bash
# 점진적 기능 추가
"Add search functionality to the header:
- Search input with icon
- Dropdown with search results
- Keyboard navigation (arrow keys, enter)"
```

## 📋 설정 체크리스트

Cursor 사용 전 확인사항:

- [ ] Cursor 설치 및 로그인
- [ ] 프로젝트 열기 및 구조 파악
- [ ] .cursorrules 파일 생성
- [ ] 개발 환경 설정 (Node.js, Git 등)
- [ ] 필수 단축키 숙지
- [ ] 첫 번째 채팅 테스트
- [ ] 자동완성 기능 테스트
- [ ] 코드 편집 기능 테스트

## 🔍 문제 해결

### 일반적인 문제들

1. **자동완성이 작동하지 않음**

   - 인터넷 연결 확인
   - Cursor 재시작
   - 계정 로그인 상태 확인

2. **채팅 응답이 느림**

   - 네트워크 상태 확인
   - 복잡한 요청을 작은 단위로 분해
   - 불필요한 컨텍스트 제거

3. **코드 제안이 부정확함**
   - .cursorrules 파일 점검
   - 프로젝트 구조 설명 추가
   - 더 구체적인 요구사항 제공

---

다음: [Cursor Rules 설정 가이드](./cursor-rules.md) →
