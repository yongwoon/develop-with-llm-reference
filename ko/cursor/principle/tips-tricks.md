# Cursor 활용 팁

## 🚀 생산성 향상 팁

### 1. 스마트 자동완성 활용

#### 컨텍스트 기반 완성

```typescript
// 기존 패턴 학습
const UserCard = ({ user }) => {
  // Tab 키로 기존 스타일 패턴 자동 적용
  return (
    <div className="card user-card">
      <img src={user.avatar} alt={user.name} />
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
};

// 새로운 컴포넌트 작성 시 자동으로 비슷한 패턴 제안
const ProductCard = ({ product }) => {
  // Cursor가 UserCard 패턴을 학습하여 자동 제안
  return (
    <div className="card product-card">
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <p>{product.price}</p>
    </div>
  );
};
```

#### 타입 기반 자동완성

```typescript
interface User {
  id: string;
  name: string;
  email: string;
  avatar: string;
  preferences: {
    theme: "light" | "dark";
    notifications: boolean;
  };
}

function updateUser(user: User) {
  // Cursor가 User 타입을 분석하여 정확한 속성 제안
  const updatedUser = {
    ...user,
    preferences: {
      ...user.preferences,
      theme: "dark", // 자동으로 'light' | 'dark' 타입 제안
    },
  };

  return updatedUser;
}
```

### 2. 채팅 인터페이스 최적화

#### 구체적인 요청 작성

```bash
# ❌ 모호한 요청
"컴포넌트 만들어줘"

# ✅ 구체적인 요청
"사용자 프로필 카드 컴포넌트를 만들어주세요:
- Props: user (User 타입)
- 아바타 이미지 (둥근 모양)
- 이름과 이메일 표시
- 편집 버튼 (오른쪽 상단)
- Tailwind CSS 사용
- 호버 효과 포함"
```

#### 코드 컨텍스트 제공

````bash
# 기존 코드 참조
"현재 Button 컴포넌트와 같은 스타일로 Modal 컴포넌트를 만들어주세요:

```typescript
// 기존 Button 컴포넌트
const Button = ({ variant, children, onClick }) => {
  return (
    <button
      className={`btn ${variant}`}
      onClick={onClick}
    >
      {children}
    </button>
  );
};
````

Modal도 같은 디자인 시스템을 따르도록 해주세요."

````

### 3. 파일 관리 최적화

#### 관련 파일 동시 열기
```bash
# 관련 파일들을 함께 열어두면 더 정확한 제안
components/
├── UserProfile.tsx     # 메인 컴포넌트
├── UserCard.tsx        # 참조할 컴포넌트
├── Button.tsx          # 공통 컴포넌트
types/
├── User.ts            # 타입 정의
hooks/
├── useAuth.ts         # 관련 훅
utils/
├── validation.ts      # 유틸리티 함수
````

#### 파일 구조 일관성

```typescript
// 일관된 파일 구조로 더 나은 제안 받기
// components/UserProfile/index.tsx
export { UserProfile } from "./UserProfile";
export { UserCard } from "./UserCard";
export { UserForm } from "./UserForm";

// components/UserProfile/UserProfile.tsx
import { UserCard } from "./UserCard";
import { UserForm } from "./UserForm";
```

## 🎯 고급 기능 활용

### 1. 코드 편집 (Cmd+K) 마스터하기

#### 선택적 리팩토링

```typescript
// 기존 코드
function calculateTotal(items) {
  let total = 0;
  for (let i = 0; i < items.length; i++) {
    total += items[i].price;
  }
  return total;
}

// Cmd+K로 선택 후 "TypeScript로 변환하고 최적화해주세요"
function calculateTotal(items: Item[]): number {
  return items.reduce((total, item) => total + item.price, 0);
}
```

#### 에러 처리 추가

```typescript
// 기존 코드
async function fetchUser(id: string) {
  const response = await fetch(`/api/users/${id}`);
  return response.json();
}

// Cmd+K로 선택 후 "에러 처리 추가해주세요"
async function fetchUser(id: string): Promise<User | null> {
  try {
    const response = await fetch(`/api/users/${id}`);

    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }

    return await response.json();
  } catch (error) {
    console.error("Failed to fetch user:", error);
    return null;
  }
}
```

### 2. 멀티커서와 AI 조합

#### 반복 작업 자동화

```typescript
// 여러 줄 선택 후 패턴 적용
const user1 = { id: "1", name: "John" };
const user2 = { id: "2", name: "Jane" };
const user3 = { id: "3", name: "Bob" };

// Cmd+K로 "각 사용자에 대해 validation 함수 생성"
const validateUser1 = (user: User) => user.id === "1" && user.name === "John";
const validateUser2 = (user: User) => user.id === "2" && user.name === "Jane";
const validateUser3 = (user: User) => user.id === "3" && user.name === "Bob";
```

### 3. 프로젝트 전체 분석 활용

#### 코드베이스 패턴 학습

```typescript
// Cursor가 프로젝트 전체에서 패턴 학습
// 1. 기존 API 호출 패턴
const useUser = (id: string) => {
  return useQuery(["user", id], () => fetchUser(id));
};

// 2. 새로운 훅 생성 시 자동으로 같은 패턴 제안
const useProduct = (id: string) => {
  return useQuery(["product", id], () => fetchProduct(id));
};
```

## 🛠 워크플로우 최적화

### 1. 개발 단계별 활용

#### 프로토타이핑 단계

```bash
# 빠른 컴포넌트 생성
"간단한 로그인 폼을 만들어주세요:
- 이메일과 비밀번호 입력
- 로그인 버튼
- 기본 스타일링
- 상태 관리는 useState 사용"
```

#### 구현 단계

```bash
# 상세한 기능 구현
"로그인 폼을 다음과 같이 개선해주세요:
- React Hook Form 사용
- Zod 스키마 validation
- 로딩 상태 표시
- 에러 메시지 표시
- 자동 포커스 기능"
```

#### 최적화 단계

```bash
# 성능 최적화
"현재 컴포넌트의 성능을 최적화해주세요:
- 불필요한 리렌더링 방지
- 메모이제이션 적용
- 번들 크기 최적화
- 접근성 개선"
```

### 2. 팀 협업 워크플로우

#### 컨벤션 통일

```markdown
# .cursorrules 파일로 팀 컨벤션 통일

You are an expert developer following our team conventions.

## Code Style

- Use functional components only
- Follow ESLint rules strictly
- Use TypeScript interfaces over types
- Implement proper error boundaries

## Naming Conventions

- Components: PascalCase
- Functions: camelCase
- Constants: UPPER_CASE
- Files: kebab-case
```

#### 코드 리뷰 최적화

```bash
# 코드 리뷰용 설명 생성
"이 함수가 하는 일을 설명하고,
잠재적인 문제점과 개선 방안을 제시해주세요"

# 테스트 코드 생성
"이 컴포넌트에 대한 Jest 테스트를 작성해주세요:
- 렌더링 테스트
- 사용자 상호작용 테스트
- 에러 상황 테스트"
```

### 3. 디버깅 워크플로우

#### 에러 분석

```typescript
// 에러 발생 코드
const UserList = ({ users }) => {
  return (
    <div>
      {users.map(user => (
        <UserCard key={user.id} user={user} />
      ))}
    </div>
  );
};

// Cursor에게 에러 분석 요청
"이 코드에서 'Cannot read property map of undefined' 에러가 발생합니다.
원인과 해결 방법을 알려주세요"
```

#### 로그 추가

```bash
# 디버깅용 로그 추가
"이 함수에 적절한 로그를 추가해주세요:
- 함수 진입/종료 로그
- 중요한 변수 상태 로그
- 에러 발생 시 상세 로그"
```

## 🎨 코드 품질 향상

### 1. 자동 리팩토링

#### 코드 클린업

```typescript
// 복잡한 코드
const processUserData = (users) => {
  const result = [];
  for (let i = 0; i < users.length; i++) {
    if (users[i].active) {
      if (users[i].email && users[i].email.includes("@")) {
        result.push({
          id: users[i].id,
          name: users[i].name,
          email: users[i].email,
        });
      }
    }
  }
  return result;
};

// Cmd+K로 "이 코드를 더 깔끔하게 리팩토링해주세요"
const processUserData = (users: User[]): ProcessedUser[] => {
  return users
    .filter((user) => user.active && user.email?.includes("@"))
    .map((user) => ({
      id: user.id,
      name: user.name,
      email: user.email,
    }));
};
```

### 2. 타입 안전성 강화

#### 타입 가드 생성

```typescript
// 기존 코드
function handleUserData(data: unknown) {
  // 타입 검증 없이 사용
  console.log(data.name);
}

// Cursor에게 "타입 안전성을 위한 타입 가드 추가"
function isUser(data: unknown): data is User {
  return (
    typeof data === "object" &&
    data !== null &&
    "id" in data &&
    "name" in data &&
    "email" in data
  );
}

function handleUserData(data: unknown) {
  if (isUser(data)) {
    console.log(data.name); // 타입 안전
  }
}
```

### 3. 성능 최적화

#### 메모이제이션 적용

```typescript
// 최적화 전
const ExpensiveComponent = ({ data, filters }) => {
  const processedData = processData(data, filters);

  return (
    <div>
      {processedData.map((item) => (
        <ItemCard key={item.id} item={item} />
      ))}
    </div>
  );
};

// Cmd+K로 "성능 최적화 적용"
const ExpensiveComponent = React.memo(({ data, filters }) => {
  const processedData = useMemo(
    () => processData(data, filters),
    [data, filters]
  );

  return (
    <div>
      {processedData.map((item) => (
        <ItemCard key={item.id} item={item} />
      ))}
    </div>
  );
});
```

## 🔧 트러블슈팅 가이드

### 1. 자동완성이 작동하지 않을 때

#### 체크 리스트

```bash
# 1. 네트워크 연결 확인
curl -I https://api.cursor.sh/health

# 2. 파일 확장자 확인
.js, .jsx, .ts, .tsx 등 지원하는 확장자인지 확인

# 3. 프로젝트 루트 확인
package.json이나 .git 폴더가 있는 디렉토리에서 작업

# 4. 메모리 사용량 확인
큰 파일이나 복잡한 프로젝트의 경우 메모리 부족 가능성
```

#### 해결 방법

```bash
# 1. Cursor 재시작
Cmd+Shift+P → "Reload Window"

# 2. 캐시 클리어
Cmd+Shift+P → "Clear Cache"

# 3. 설정 초기화
~/.cursor/User/settings.json 삭제 후 재시작
```

### 2. 부정확한 제안이 나올 때

#### 컨텍스트 개선

```bash
# 1. .cursorrules 파일 업데이트
더 구체적인 프로젝트 규칙 추가

# 2. 관련 파일 열기
참조할 파일들을 에디터에서 열어두기

# 3. 타입 정의 명확화
TypeScript 타입을 더 정확하게 정의
```

### 3. 성능 문제 해결

#### 최적화 설정

```json
// settings.json
{
  "cursor.ai.maxTokens": 2000,
  "cursor.ai.temperature": 0.3,
  "cursor.ai.contextWindow": 8000
}
```

#### 리소스 관리

```bash
# 1. 불필요한 파일 제외
.gitignore에 대용량 파일 추가

# 2. 프로젝트 크기 최적화
node_modules, dist, build 등 제외

# 3. 파일 개수 제한
너무 많은 파일을 동시에 열지 않기
```

## ✅ 효율성 체크리스트

### 기본 설정

- [ ] .cursorrules 파일 작성
- [ ] 프로젝트 구조 정리
- [ ] 필수 단축키 숙지
- [ ] 관련 파일 그룹화

### 작업 방식

- [ ] 구체적인 요청 작성
- [ ] 컨텍스트 파일 미리 열기
- [ ] 단계별 접근 방식 사용
- [ ] 정기적인 코드 리뷰

### 품질 관리

- [ ] 타입 안전성 확인
- [ ] 에러 처리 구현
- [ ] 테스트 코드 작성
- [ ] 성능 최적화 적용

### 팀 협업

- [ ] 컨벤션 문서화
- [ ] 공통 규칙 설정
- [ ] 코드 리뷰 프로세스
- [ ] 지식 공유 세션

---

[← 이전: Claude Code vs Cursor 비교](./comparison.md) | [처음으로 →](./README.md)
