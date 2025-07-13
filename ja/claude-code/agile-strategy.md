# アジャイル開発戦略

## 🌊 不確実性管理

### ユーザーストーリーベースアプローチ

#### 技術仕様の代わりに価値中心で

```bash
# 技術中心アプローチ（避ける）
"Create a PostgreSQL table with user fields and indexes"

# ユーザーストーリー中心アプローチ（推奨）
"As a user, I want to create an account
so that I can save my preferences and order history

Acceptance Criteria:
- User can sign up with email/password
- Email verification is required
- Profile is created automatically after signup"
```

#### Claude に解決策提案を要求

```bash
"Given this user story: [ユーザーストーリー内容]
Suggest:
1. Technical implementation approach
2. Required components
3. Potential challenges
4. MVP vs full feature comparison"
```

### MVP（Minimum Viable Product）優先

#### 段階別機能拡張

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

### 探索的プロトタイピング

```bash
# 不確実な要求事項探索
"Create 3 different UI prototypes for the dashboard:
1. Card-based layout with summary metrics
2. Table-focused design for data analysis
3. Visual charts and graphs approach

Each should handle the same data but present differently"

# 技術的アプローチ方法探索
"Implement user notifications using 3 approaches:
1. WebSocket implementation
2. Server-Sent Events
3. Polling mechanism

Include pros/cons and resource usage for each"
```

## 📅 スプリント計画と実行

### Sprint 0: Discovery & Setup

```markdown
## Week 1: Discovery Sprint

### Day 1-2: 技術検証

"Create proof of concepts for:

- Authentication flow with NextAuth
- Database connection with Prisma
- Real-time updates with Socket.io"

### Day 3-4: UI/UX 探索

"Create wireframes for main user flows:

- Onboarding process
- Main dashboard
- Key feature interactions"

### Day 5: アーキテクチャ決定

"Based on POCs, create:

- System architecture diagram
- Technology stack decision document
- Development environment setup guide"
```

### Sprint 1-2: コア機能実装

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

### 日次スタンドアップ活用

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

## 🔄 反復的改善戦略

### 機能別段階的改善

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

### スパイクによる技術探索

```bash
# 技術的不確実性解決
"Research spike: Implement real-time collaboration
Time-boxed to 1 day, explore:
- Operational Transformation approach
- CRDT implementation
- Simple locking mechanism

Provide recommendation with POC code"
```

## 📊 ストーリーポイントと見積もり

### 作業サイズ基準

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

## 🎯 不確実性対応パターン

### 1. インターフェース優先設計

```typescript
// 実装前にインターフェース定義
"Define TypeScript interfaces for a user management system:
- User entity
- Repository interface
- Service layer interface
- API response types

Don't implement yet, just define contracts"
```

### 2. モックデータ活用

```bash
"Create mock API responses for:
- User CRUD operations
- Product catalog
- Order processing

Use realistic data that covers edge cases
Include delay simulation for loading states"
```

### 3. フィーチャートグル実装

```bash
"Implement feature toggle system:
- Environment-based flags
- User-specific flags
- Gradual rollout capability
- Runtime toggle without deploy"
```

### 4. A/B テスト準備

```bash
"Set up A/B testing framework:
- User segmentation logic
- Metric tracking
- Results analysis
- Easy experiment creation"
```

## 🔍 フィードバックループ最適化

### 迅速プロトタイプ → 検証 → 改善

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

### 継続的改善要求

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

## ✅ アジャイル実践チェックリスト

スプリント別確認事項：

### Sprint Planning

- [ ] ユーザーストーリーが明確な価値を提供するか？
- [ ] 受け入れ基準がテスト可能か？
- [ ] 技術的不確実性を識別したか？
- [ ] スパイクが必要な項目を決定したか？

### Daily Execution

- [ ] 作業を小さな単位に分解したか？
- [ ] 毎日デプロイ可能な増分を作成したか？
- [ ] ブロッカーを迅速に解決したか？
- [ ] チームと進行状況を共有したか？

### Sprint Review

- [ ] 動作するソフトウェアを実演したか？
- [ ] ユーザーフィードバックを収集したか？
- [ ] 次の優先順位を調整したか？
- [ ] 改善事項を文書化したか？

---

次: [作業単位ガイド](./task-units.md) →
