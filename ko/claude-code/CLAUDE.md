# CLADUE summary

## 문서, 코멘트 작성

아래의 Prompt 를 CLAUDE.md 에 추가한다.

```txt
## Documentation Writing Guidelines

When writing or updating documentation in this project:

**Language Policy:**
- Write documentation in Korean (한국어)
- Use English for technical terms and foreign words (외래어)
- Keep consistency throughout all documentation files

**Examples:**
- ✅ "Database 연결 설정" (not "데이터베이스 연결 설정")
- ✅ "API Endpoint 구현" (not "API 엔드포인트 구현")
- ✅ "Cache Directory 관리" (not "캐시 디렉토리 관리")
- ✅ "Backend Service Logic" (not "백엔드 서비스 로직")

**Technical Terms to Keep in English:**
- API, Backend, Frontend, Database, Cache, Service, Repository
- Application, Component, Module, Framework, Library
- Request, Response, Schema, Model, Controller
- Test, Debug, Deploy, Build, Configuration
- Docker, Container, Server, Client, Router, Middleware
```

- 일본어의 경우

```txt
## Documentation Writing Guidelines

When writing or updating documentation in this project:

**Language Policy:**
- Write documentation in Japanese (日本語)
- Use English for technical terms and foreign words (英語)
- Keep consistency throughout all documentation files

**Examples:**
- ✅ "Database connection 設定" (not "データベースコネクション設定")
- ✅ "API Endpoint 実装" (not "API エンドポイント実装")
- ✅ "Cache Directory 管理" (not "キャッシュディレクトリ管理")
- ✅ "Backend Service Logic" (not "バックエンドサービスロジック")

**Technical Terms to Keep in English:**
- API, Backend, Frontend, Database, Cache, Service, Repository
- Application, Component, Module, Framework, Library
- Request, Response, Schema, Model, Controller
- Test, Debug, Deploy, Build, Configuration
- Docker, Container, Server, Client, Router, Middleware
```



## Frontend Design

```txt
**Design & UX:**
- Implement responsive design that works on mobile, tablet, and desktop
- Support dark mode with proper color contrast ratios (WCAG AA compliant)
- Use semantic HTML elements for better accessibility
- Include proper ARIA labels and roles where needed
- Ensure keyboard navigation support

**Technical Implementation:**
- Use modern CSS features (flexbox, grid, custom properties)
- Implement loading states and error handling
- Add hover and focus states for interactive elements
- Optimize for performance (lazy loading, efficient re-renders)
- Follow the mobile-first approach

**Code Quality:**
- Write clean, readable code with proper naming conventions
- Include TypeScript types if using TypeScript
- Add meaningful comments for complex logic
- Structure components logically with separation of concerns

**User Experience:**
- Provide immediate visual feedback for user interactions
- Include appropriate transitions and animations
- Handle edge cases (empty states, long text, network errors)
- Ensure fast loading times and smooth interactions
```
