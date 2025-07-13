# 効率的な開発段階

## 🚀 開発プロセス概要

### 第 1 段階：小さな単位から始める

#### 基本原則

- プロジェクト全体を一度に要求しない
- 独立してテスト可能なコンポーネントから始める
- 各段階で検証してから進行

#### 例：Express サーバー構築

```bash
# 悪い例
"Create a complete e-commerce backend with user management,
product catalog, order processing, and payment integration"

# 良い例 - 段階的アプローチ
Step 1: "Create a basic Express server with a health check endpoint"
Step 2: "Add middleware for CORS, body parsing, and error handling"
Step 3: "Implement user registration endpoint with validation"
Step 4: "Add JWT authentication middleware"
```

### 第 2 段階：段階的機能追加

#### 既存コードベース上に構築

```bash
# コンテキスト提供と共にリクエスト
"Given the existing Express server in app.js,
add a user authentication middleware that:
- Validates JWT tokens
- Attaches user info to req.user
- Returns 401 for invalid tokens"
```

#### 統合テスト含む

```bash
"Add unit tests for the authentication middleware
using Jest and supertest, covering:
- Valid token scenarios
- Expired token handling
- Malformed token handling"
```

### 第 3 段階：コンテキスト提供

#### プロジェクト構造説明

```bash
"Project structure:
- src/models/User.js contains Mongoose user schema
- src/middleware/ for all middleware functions
- Using ES6 modules (import/export)

Create a user controller with CRUD operations
following this structure and coding style"
```

### 第 4 段階：テスト駆動開発

```bash
# テストを最初に作成要求
"Write Jest tests for a UserService class that should:
- Create new users with hashed passwords
- Validate unique email addresses
- Handle database errors gracefully

Then implement the UserService to pass these tests"
```

## 📝 効果的なプロンプト作成法

### 1. 具体的な要求事項

#### ❌ 悪い例

```
"Make a login page"
"Add authentication"
"Create a dashboard"
```

#### ✅ 良い例

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

### 2. 技術的制約事項明示

```bash
"Implement the password reset feature:
- Use TypeScript with strict mode
- Follow existing ESLint configuration
- Compatible with Node.js 18+
- Use Prisma ORM for database operations
- Include JSDoc comments for all public methods
- Handle errors using the existing error middleware pattern"
```

### 3. 期待される結果説明

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

## 🔄 反復的改善プロセス

### 初期実装 → リファクタリング → 最適化

#### Phase 1: 動作するコード

```bash
"Create a function that fetches user data from the API"
```

#### Phase 2: エラーハンドリング追加

```bash
"Add error handling to the user fetching function:
- Network errors
- 404 responses
- Timeout after 10 seconds"
```

#### Phase 3: パフォーマンス最適化

```bash
"Optimize the user fetching function:
- Add caching with 5-minute TTL
- Implement request deduplication
- Add loading and error states"
```

#### Phase 4: 型安全性

```bash
"Add TypeScript types to the user fetching function:
- Generic type for response data
- Proper error types
- Type guards for runtime validation"
```

## 🏗 実際のワークフロー例

### Full-Stack 機能実装（User Profile）

#### Step 1: データモデル

```bash
"Create a Prisma schema for user profiles with:
- Basic info (name, bio, avatar)
- Social links (optional)
- Privacy settings
- Timestamps (createdAt, updatedAt)"
```

#### Step 2: API エンドポイント

```bash
"Create Express routes for user profile:
GET /api/profile/:userId - Public profile view
GET /api/profile - Get own profile (authenticated)
PUT /api/profile - Update own profile
Include validation middleware and error handling"
```

#### Step 3: フロントエンドコンポーネント

```bash
"Create a ProfileForm React component:
- Form fields matching the profile schema
- Image upload for avatar
- Real-time validation
- Optimistic updates
- Success/error notifications"
```

#### Step 4: 統合とテスト

```bash
"Create integration tests for the profile feature:
- Test complete flow from form submission to database
- Test validation errors
- Test authorization (can only edit own profile)
- Test image upload handling"
```

## 🛡 コード品質管理

### 1. コードレビュー要求

```bash
"Review this authentication middleware for:
- Security vulnerabilities
- Performance issues
- Error handling completeness
- Code style consistency
Suggest improvements with explanations"
```

### 2. リファクタリング要求

```bash
"Refactor this component to:
- Extract business logic to custom hooks
- Improve type safety
- Reduce cognitive complexity
- Follow SOLID principles
Maintain all existing functionality"
```

### 3. パフォーマンス最適化

```bash
"Optimize this React component for performance:
- Identify unnecessary re-renders
- Implement proper memoization
- Lazy load heavy dependencies
- Optimize bundle size
Provide before/after comparison"
```

## 📊 進捗状況追跡

### Git コミット戦略

```bash
# 機能別ブランチ
git checkout -b feature/user-authentication

# 意味のあるコミットメッセージ
git commit -m "feat: add JWT authentication middleware"
git commit -m "test: add auth middleware unit tests"
git commit -m "docs: update API documentation for auth endpoints"
```

### ドキュメント化要求

```bash
"Add comprehensive documentation:
- JSDoc comments for all functions
- README with setup instructions
- API endpoint documentation
- Architecture decision records (ADRs)"
```

## ✅ 開発段階チェックリスト

各機能実装時の確認事項：

- [ ] 要求事項を明確に定義
- [ ] 作業を小さな単位に分解
- [ ] 各段階でテスト作成
- [ ] コードレビュー実施
- [ ] ドキュメント化完了
- [ ] パフォーマンス最適化検討
- [ ] セキュリティ脆弱性点検
- [ ] エラーハンドリング確認

---

次へ：[アジャイル開発戦略](./agile-strategy.md) →
