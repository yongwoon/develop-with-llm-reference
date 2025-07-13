# 作業単位ガイド

## 📏 作業サイズ定義

### レベル 1：単一関数/コンポーネント（30 分-1 時間）

#### ユーティリティ関数

```javascript
// メール検証関数
"Create a function that validates email format:
- Accept email string as parameter
- Return true/false
- Handle edge cases (empty string, null)
- Follow RFC 5322 standard"

// 日付フォーマット関数
"Create a date formatting utility:
- Input: Date object or timestamp
- Output: 'YYYY-MM-DD' format
- Handle timezone considerations
- Include unit tests"
```

#### 単一 React コンポーネント

```javascript
// ボタンコンポーネント
"Create a Button component:
- Props: label, onClick, variant (primary/secondary/danger)
- Loading state support
- Disabled state
- Tailwind CSS styling
- TypeScript props interface"

// カードコンポーネント
"Create a Card component:
- Header, body, footer slots
- Optional shadow and border
- Responsive padding
- Click handler support"
```

#### 単一 API エンドポイント

```javascript
// ユーザー取得
"Create GET /api/users/:id endpoint:
- Fetch user by ID from database
- Return 404 if not found
- Include related data (profile)
- Add response caching headers"

// ステータスチェック
"Create health check endpoint:
- Check database connection
- Check external service availability
- Return status and response time
- Format: { status: 'ok', services: {...} }"
```

### レベル 2：機能モジュール（2-4 時間）

#### 認証モジュール

```javascript
// 完全な認証モジュール
"Create authentication module with:
- login(email, password) - returns token
- logout() - clears session
- isAuthenticated() - checks current status
- refreshToken() - renews expired token
- Store token securely (httpOnly cookie)
- Handle token expiration"

// ユーザーセッション管理
"Implement session management:
- Create session on login
- Session timeout after 30 min inactivity
- Refresh session on activity
- Multiple device session tracking
- Session revocation functionality"
```

#### フォームシステム

```javascript
// フォームコンポーネントセット
"Create form component system:
- FormInput with validation display
- FormSelect with search capability
- FormTextarea with character count
- FormError component
- Form wrapper with validation logic
- Integrate with React Hook Form"

// 検証システム
"Build validation system:
- Email, phone, URL validators
- Custom validation rules
- Async validation support
- Error message localization
- Validation schema builder"
```

#### データテーブル

```javascript
// テーブルコンポーネント
"Create DataTable component:
- Column configuration
- Sorting functionality
- Pagination controls
- Row selection
- Search/filter capability
- Export to CSV feature"
```

### レベル 3：完全な機能（1-2 日）

#### ユーザー管理システム

```javascript
// CRUD全体実装
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

#### ファイルアップロードシステム

```javascript
// 完全なファイルアップロード
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

#### 通知システム

```javascript
// リアルタイム通知
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

## 🎯 ストーリーポイント割り当てガイド

### 1 ポイント（2-4 時間）

```markdown
特徴：

- 単一責任
- 明確な入出力
- 外部依存性最小
- エッジケース少ない

例：

- "Add loading spinner to button"
- "Create formatCurrency utility"
- "Add validation to email field"
- "Update color scheme in header"
```

### 2 ポイント（4-8 時間）

```markdown
特徴：

- 2-3 個コンポーネント連携
- 基本的な状態管理
- API 接続含む
- 標準エラーハンドリング

例：

- "Create login form with API integration"
- "Add sorting to data table"
- "Implement search functionality"
- "Create user profile card"
```

### 3 ポイント（1-2 日）

```markdown
特徴：

- 完全な機能単位
- フロントエンド + バックエンド
- 複雑なビジネスロジック
- 様々なエラーシナリオ

例：

- "User registration flow"
- "Shopping cart functionality"
- "Comment system with replies"
- "Dashboard with multiple widgets"
```

### 5 ポイント（2-3 日）

```markdown
特徴：

- システム間統合
- 複雑な状態管理
- パフォーマンス最適化必要
- 広範囲なテスト必要

例：

- "Payment gateway integration"
- "Real-time collaboration feature"
- "Advanced search with filters"
- "Report generation system"
```

### 8 ポイント（3-5 日）

```markdown
特徴：

- アーキテクチャレベル変更
- 複数システム連携
- マイグレーション含む
- 高い複雑度

例：

- "Microservice extraction"
- "Database migration system"
- "Complete authentication overhaul"
- "Multi-tenant implementation"
```

## 📋 具体的な作業分解例

### e コマースショッピングカート機能（5 ポイント）

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

### リアルタイムチャット機能（8 ポイント）

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

## 🔧 作業サイズ見積もりツール

### 複雑度チェックリスト

```markdown
作業複雑度評価：

□ 技術的複雑度

- [ ] 新しい技術スタック必要
- [ ] 複雑なアルゴリズム実装
- [ ] パフォーマンス最適化必要
- [ ] セキュリティ考慮事項多い

□ 統合複雑度

- [ ] 外部サービス連携
- [ ] 複数システムとの通信
- [ ] データマイグレーション
- [ ] 下位互換性維持

□ ビジネス複雑度

- [ ] 複雑なビジネスルール
- [ ] 多くのエッジケース
- [ ] 規制遵守必要
- [ ] 多言語対応

□ UI/UX 複雑度

- [ ] 複雑なインタラクション
- [ ] レスポンシブデザイン
- [ ] アクセシビリティ要件
- [ ] アニメーション/トランジション効果
```

### 作業分解テンプレート

```markdown
# Feature: [機能名]

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

## 📊 ベロシティ追跡

### スプリントベロシティ記録

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

## ✅ 作業見積もりベストプラクティス

1. **過小評価防止**

   - テスト作成時間含む
   - コードレビュー時間考慮
   - デプロイ・モニタリング含む

2. **バッファ時間確保**

   - 予期しない問題対応
   - 技術的負債解決
   - ドキュメント化時間

3. **チーム合意**

   - Planning Poker 活用
   - 過去データ参照
   - 継続的調整

4. **明確な完了基準**
   - コード完成
   - テスト通過
   - ドキュメント更新
   - PR 承認
