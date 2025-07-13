# Claude Memory Tips

20년 넘은 숙련된 풀스택 웹개발자로서 Claude Code를 효과적으로 사용하기 위한 메모리 구성을 제안드리겠습니다.

## 사용자 메모리 (`~/.claude/CLAUDE.md`)

_모든 프로젝트에 공통적으로 적용되는 개인 환경 설정_

### 코딩 스타일 및 선호도

- 2칸 들여쓰기 사용
- 세미콜론 항상 사용
- 함수형 프로그래밍 스타일 선호 (map, filter, reduce 등)
- async/await 사용 (Promise.then 대신)
- TypeScript 사용 선호
- ESLint와 Prettier 설정 적용

### 개인 도구 및 워크플로우

- VS Code 에디터 사용
- Git 커밋 메시지 컨벤션 (feat:, fix:, docs: 등)
- 단축키 및 스니펫 선호도
- 테스트 도구 선호도 (Jest, Vitest, Cypress 등)
- 패키지 매니저 선호도 (npm, yarn, pnpm)

### 아키텍처 및 설계 원칙

- 컴포넌트 기반 아키텍처
- 단일 책임 원칙 준수
- 의존성 주입 패턴
- 에러 핸들링 방식
- 로깅 및 모니터링 접근법

### Example

```txt
# 사용자 메모리 - 개인 개발 환경 설정

## 코딩 스타일 및 선호도

### 기본 포맷팅
- 2칸 들여쓰기 사용 (탭 대신 스페이스)
- 세미콜론 항상 사용
- 단일 따옴표 선호 ('string' 형태)
- 객체와 배열의 trailing comma 사용
- 80자 라인 길이 제한

### JavaScript/TypeScript 스타일
- 함수형 프로그래밍 스타일 선호 (map, filter, reduce 등)
- async/await 사용 (Promise.then 대신)
- TypeScript 사용 선호 (any 타입 금지)
- 화살표 함수 선호 (단, 메서드는 function 키워드 사용)
- 구조 분해 할당 적극 활용

### React 컴포넌트 스타일
- 함수형 컴포넌트 사용 (클래스 컴포넌트 금지)
- 커스텀 훅 적극 활용
- PropTypes 대신 TypeScript 인터페이스 사용
- 컴포넌트 파일명은 PascalCase

## 개인 도구 및 워크플로우

### 에디터 및 확장
- VS Code 에디터 사용
- Prettier, ESLint 자동 포맷팅 설정
- Auto Import 확장 사용
- GitLens 확장 사용

### Git 커밋 컨벤션
- feat: 새로운 기능 추가
- fix: 버그 수정
- docs: 문서 수정
- style: 코드 포맷팅
- refactor: 코드 리팩토링
- test: 테스트 코드 추가/수정
- chore: 빌드 프로세스 또는 보조 도구 수정

### 패키지 매니저
- pnpm 사용 선호 (npm, yarn 대신)
- package.json scripts 명령어 표준화
- 의존성 업데이트 주기적 실행

### 테스트 도구
- Jest + Testing Library 조합 선호
- Vitest 사용 (Vite 프로젝트에서)
- E2E 테스트는 Playwright 사용
- 테스트 커버리지 80% 이상 유지

## 아키텍처 및 설계 원칙

### 컴포넌트 설계
- 단일 책임 원칙 준수
- 재사용 가능한 컴포넌트 작성
- Props drilling 방지 (Context API 또는 상태 관리 라이브러리 사용)
- 컴포넌트 최대 200줄 제한

### 상태 관리
- 로컬 상태는 useState 사용
- 전역 상태는 Zustand 선호
- 서버 상태는 React Query/TanStack Query 사용
- 폼 상태는 React Hook Form 사용

### 에러 핸들링
- try-catch 블록 적극 사용
- 에러 바운더리 컴포넌트 구현
- 사용자 친화적인 에러 메시지 제공
- 에러 로깅 시스템 구축

### 성능 최적화
- React.memo 적절한 사용
- useMemo, useCallback 필요시에만 사용
- 코드 스플리팅 적용 (React.lazy)
- 이미지 최적화 (Next.js Image 컴포넌트 사용)

## 개발 환경 설정

### 환경 변수 관리
- .env.local 파일 사용
- 환경별 설정 분리 (.env.development, .env.production)
- 민감한 정보는 절대 커밋하지 않음

### 디버깅 도구
- React Developer Tools 사용
- Chrome DevTools 적극 활용
- console.log 대신 debugger 사용 선호
- 성능 프로파일링 도구 사용

### 개발 서버 설정
- 핫 리로딩 활성화
- 프록시 설정으로 CORS 문제 해결
- 개발 환경에서 HTTPS 사용 (mkcert 활용)

## 문서화 및 커뮤니케이션

### 코드 주석
- JSDoc 형태의 주석 사용
- 복잡한 로직에 대한 설명 추가
- TODO, FIXME 주석 활용

### 문서 작성
- README.md 파일 상세 작성
- API 문서는 OpenAPI/Swagger 사용
- 컴포넌트 Storybook 문서 작성
```

## 프로젝트 메모리 (`./CLAUDE.md`)

_특정 프로젝트에 대한 팀 공유 지침_

### 프로젝트 아키텍처

- 프로젝트 구조 및 폴더 구성
- 주요 기술 스택 (React, Next.js, Express 등)
- 데이터베이스 설계 및 연결 방식
- API 설계 원칙 (RESTful, GraphQL 등)
- 상태 관리 방식 (Redux, Zustand, Context API 등)

### 코딩 표준

- 네이밍 컨벤션 (변수, 함수, 클래스, 파일명)
- 컴포넌트 작성 규칙
- 타입 정의 방식
- 에러 처리 및 예외 상황 대응
- 코드 리뷰 체크리스트

### 개발 환경 설정

- 환경 변수 관리
- 빌드 및 배포 설정
- 테스트 환경 구성
- 로컬 개발 서버 설정
- Docker 컨테이너 설정

### 외부 서비스 연동

- 인증/인가 시스템
- 결제 시스템
- 이메일 서비스
- 클라우드 스토리지
- 써드파티 API 연동 방식

### 워크플로우 및 배포

- Git 브랜치 전략
- CI/CD 파이프라인
- 배포 환경 (개발, 스테이징, 프로덕션)
- 모니터링 및 알림 설정
- 백업 및 복구 절차

### 문서화 및 커뮤니케이션

- API 문서 작성 방식
- 코드 주석 가이드라인
- 변경사항 로그 관리
- 팀 내 커뮤니케이션 규칙

### Example

```txt
# 프로젝트 메모리 - E-Commerce 웹 애플리케이션

## 프로젝트 개요
- **프로젝트명**: ShopMate E-commerce Platform
- **기술 스택**: Next.js 14, TypeScript, Tailwind CSS, Prisma, PostgreSQL
- **배포 환경**: Vercel (Frontend), Railway (Database)
- **팀 구성**: 3명 (Frontend 2명, Backend 1명)

## 프로젝트 아키텍처

### 폴더 구조
"""
├── src/
│   ├── app/                 # Next.js 13+ App Router
│   ├── components/          # 재사용 가능한 컴포넌트
│   │   ├── ui/             # 기본 UI 컴포넌트
│   │   ├── forms/          # 폼 관련 컴포넌트
│   │   └── layout/         # 레이아웃 컴포넌트
│   ├── lib/                # 유틸리티 함수 및 설정
│   ├── hooks/              # 커스텀 훅
│   ├── types/              # TypeScript 타입 정의
│   └── store/              # 상태 관리 (Zustand)
├── prisma/                 # 데이터베이스 스키마
├── public/                 # 정적 파일
└── tests/                  # 테스트 파일
"""

### 기술 스택 상세
- **Frontend**: Next.js 14 (App Router), React 18, TypeScript 5.0
- **Styling**: Tailwind CSS 3.3, Headless UI, Radix UI
- **State Management**: Zustand (전역 상태), React Query (서버 상태)
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js with Google, GitHub providers
- **Payment**: Stripe Integration
- **Testing**: Jest, React Testing Library, Playwright

## 코딩 표준

### 네이밍 컨벤션
- **컴포넌트**: PascalCase (`UserProfile.tsx`)
- **함수/변수**: camelCase (`getUserData`)
- **상수**: UPPER_SNAKE_CASE (`API_BASE_URL`)
- **파일명**: kebab-case (`user-profile.tsx`) 또는 PascalCase (컴포넌트)
- **API 엔드포인트**: kebab-case (`/api/user-profile`)

### 컴포넌트 작성 규칙
- 최대 200줄 제한 (초과시 분리)
- Props 인터페이스 정의 필수
- 기본 props 값 설정
- 에러 바운더리 적용
- 접근성 고려 (ARIA 속성, 키보드 네비게이션)

### TypeScript 규칙
- `any` 타입 사용 금지
- 모든 API 응답에 대한 타입 정의
- 유니온 타입 적극 활용
- 제네릭 타입 활용 (재사용성 향상)

## API 설계 원칙

### RESTful API 규칙
- **GET** `/api/products` - 상품 목록 조회
- **GET** `/api/products/[id]` - 특정 상품 조회
- **POST** `/api/products` - 상품 생성
- **PUT** `/api/products/[id]` - 상품 전체 수정
- **PATCH** `/api/products/[id]` - 상품 부분 수정
- **DELETE** `/api/products/[id]` - 상품 삭제

### 응답 형식 표준화
"""typescript
interface ApiResponse<T> {
  success: boolean;
  data?: T;
  error?: string;
  message?: string;
}
"""

### 에러 처리
- HTTP 상태 코드 적절한 사용
- 일관된 에러 메시지 형식
- 개발 환경에서 상세한 에러 정보 제공
- 프로덕션 환경에서 민감한 정보 숨김

## 데이터베이스 설계

### 주요 테이블
- **User**: 사용자 정보
- **Product**: 상품 정보
- **Category**: 상품 카테고리
- **Order**: 주문 정보
- **OrderItem**: 주문 상품 상세
- **Cart**: 장바구니
- **Review**: 상품 리뷰

### Prisma 스키마 규칙
- 모든 모델에 `id`, `createdAt`, `updatedAt` 필드 포함
- 관계 설정 시 cascade 옵션 명시
- 인덱스 적절한 설정
- 소프트 삭제 구현 (`deletedAt` 필드 사용)

## 상태 관리

### Zustand 스토어 구조
"""
├── store/
│   ├── auth-store.ts       # 사용자 인증 상태
│   ├── cart-store.ts       # 장바구니 상태
│   ├── product-store.ts    # 상품 필터링 상태
│   └── ui-store.ts         # UI 상태 (모달, 로딩 등)
"""

### React Query 사용 규칙
- 서버 상태 관리 전용
- 쿼리 키 표준화 (`['products', 'list', filters]`)
- 적절한 캐싱 시간 설정
- 낙관적 업데이트 적용

## 스타일링 가이드

### Tailwind CSS 사용 규칙
- 유틸리티 클래스 우선 사용
- 커스텀 CSS는 최소화
- 컴포넌트 변형을 위한 className 조건부 적용
- 다크 모드 대응 (`dark:` 접두사 사용)

### 컴포넌트 스타일링
- 기본 컴포넌트는 `components/ui/` 디렉토리에 위치
- 비즈니스 로직과 스타일 분리
- 재사용 가능한 스타일 패턴 정의

## 인증 및 권한

### NextAuth.js 설정
- Google, GitHub OAuth 제공자 사용
- JWT 토큰 사용
- 세션 관리 및 자동 갱신
- 역할 기반 접근 제어 (RBAC)

### 보안 규칙
- 모든 API 엔드포인트에 인증 미들웨어 적용
- CSRF 토큰 사용
- XSS 공격 방지 (입력 검증 및 이스케이핑)
- 환경 변수로 민감한 정보 관리

## 결제 시스템

### Stripe 연동
- 결제 정보 안전한 처리
- 웹훅을 통한 결제 상태 동기화
- 환불 및 취소 처리 로직
- 결제 실패 시 재시도 메커니즘

## 테스트 전략

### 단위 테스트
- 모든 유틸리티 함수 테스트
- 컴포넌트 렌더링 테스트
- API 엔드포인트 테스트
- 최소 80% 코드 커버리지 유지

### 통합 테스트
- 사용자 플로우 테스트
- API 통합 테스트
- 데이터베이스 연동 테스트

### E2E 테스트
- 주요 사용자 시나리오 테스트
- 결제 플로우 테스트
- 크로스 브라우저 테스트

## 배포 및 DevOps

### 배포 전략
- **개발**: Vercel Preview 배포
- **스테이징**: 별도 Vercel 프로젝트
- **프로덕션**: 메인 도메인 배포

### CI/CD 파이프라인
- GitHub Actions 사용
- 자동 테스트 실행
- 코드 품질 검사 (ESLint, Prettier)
- 자동 배포 (테스트 통과 시)

### 모니터링
- Vercel Analytics 사용
- 에러 추적 (Sentry 연동)
- 성능 모니터링 (Web Vitals)

## 환경 설정

### 환경 변수
"""bash
# Database
DATABASE_URL=
DIRECT_URL=

# Authentication
NEXTAUTH_URL=
NEXTAUTH_SECRET=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=

# Payment
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=

# Email
RESEND_API_KEY=
"""

### 개발 환경 설정
- Node.js 18.x 이상 사용
- pnpm 패키지 매니저 사용
- VS Code 확장 프로그램 권장 목록 제공
- 개발 서버 포트: 3000번 사용

## 문서화 규칙

### README.md 필수 포함 사항
- 프로젝트 설명 및 기능
- 설치 및 실행 방법
- 환경 변수 설정 가이드
- 배포 방법
- 기여 가이드라인

### 코드 문서화
- 복잡한 비즈니스 로직에 주석 필수
- API 엔드포인트 JSDoc 작성
- 컴포넌트 PropTypes 문서화
- 데이터베이스 스키마 설명 추가
```
