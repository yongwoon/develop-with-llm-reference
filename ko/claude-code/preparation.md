# 준비사항 및 환경설정

## 🛠 프로젝트 구조 설정

### 기본 디렉토리 구조

```
project-root/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── utils/
│   └── types/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── docs/
│   ├── api/
│   ├── architecture/
│   └── specifications/
├── scripts/
├── .github/
│   └── workflows/
├── .gitignore
├── README.md
├── package.json
└── tsconfig.json
```

### 환경 설정 파일

#### 1. `.gitignore`

```gitignore
# Dependencies
node_modules/
.pnp
.pnp.js

# Testing
coverage/
.nyc_output

# Production
build/
dist/

# Environment
.env
.env.local
.env.*.local

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db
```

#### 2. `package.json` 기본 구조

```json
{
  "name": "project-name",
  "version": "1.0.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "test": "jest",
    "lint": "eslint .",
    "format": "prettier --write ."
  }
}
```

## 📋 명확한 요구사항 정의

### 1. 기능 명세서 템플릿

```markdown
# Feature: [기능명]

## Overview

[기능에 대한 간단한 설명]

## User Story

As a [사용자 유형]
I want to [수행하고자 하는 작업]
So that [얻고자 하는 가치]

## Acceptance Criteria

- [ ] [검증 가능한 조건 1]
- [ ] [검증 가능한 조건 2]
- [ ] [검증 가능한 조건 3]

## Technical Requirements

- Framework: [사용 프레임워크]
- Dependencies: [필요한 라이브러리]
- API Integration: [연동할 API]

## Constraints

- Performance: [성능 요구사항]
- Security: [보안 요구사항]
- Browser Support: [지원 브라우저]
```

### 2. 기술 스택 문서화

```markdown
# Technology Stack

## Frontend

- Framework: Next.js 14
- Language: TypeScript 5.x
- Styling: Tailwind CSS
- State Management: Zustand
- Form Handling: React Hook Form
- Validation: Zod

## Backend

- Runtime: Node.js 18+
- Framework: Express.js
- Database: PostgreSQL
- ORM: Prisma
- Authentication: JWT

## Development Tools

- Package Manager: pnpm
- Linter: ESLint
- Formatter: Prettier
- Testing: Jest + React Testing Library
- E2E Testing: Playwright
```

### 3. API 스펙 정의

```yaml
# api-specification.yml
openapi: 3.0.0
info:
  title: Project API
  version: 1.0.0

paths:
  /api/users:
    get:
      summary: Get all users
      responses:
        "200":
          description: Successful response
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: "#/components/schemas/User"

components:
  schemas:
    User:
      type: object
      properties:
        id:
          type: string
        email:
          type: string
        name:
          type: string
```

## 🔧 개발 환경 준비

### 1. 필수 도구 설치

```bash
# Node.js (LTS 버전 권장)
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs

# pnpm 설치
npm install -g pnpm

# 프로젝트 의존성 설치
pnpm install
```

### 2. VS Code 확장 프로그램

- ESLint
- Prettier
- TypeScript and JavaScript Language Features
- Tailwind CSS IntelliSense
- GitLens
- Error Lens

### 3. Git 설정

```bash
# 기본 설정
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# 유용한 별칭 설정
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

## 📐 코딩 표준 설정

### ESLint 설정 (`.eslintrc.json`)

```json
{
  "extends": [
    "next/core-web-vitals",
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "rules": {
    "@typescript-eslint/no-unused-vars": "error",
    "@typescript-eslint/no-explicit-any": "warn",
    "prefer-const": "error",
    "no-console": ["warn", { "allow": ["warn", "error"] }]
  }
}
```

### Prettier 설정 (`.prettierrc`)

```json
{
  "semi": true,
  "trailingComma": "es5",
  "singleQuote": true,
  "printWidth": 80,
  "tabWidth": 2,
  "useTabs": false,
  "bracketSpacing": true,
  "arrowParens": "always"
}
```

## ✅ 체크리스트

프로젝트 시작 전 확인사항:

- [ ] 프로젝트 디렉토리 구조 생성
- [ ] Git 저장소 초기화
- [ ] 필수 개발 도구 설치
- [ ] 환경 설정 파일 준비
- [ ] 기술 스택 문서 작성
- [ ] 코딩 표준 설정
- [ ] CI/CD 파이프라인 구성 (선택사항)
- [ ] README.md 작성

---

다음: [효율적인 개발 단계](./development-stages.md) →
