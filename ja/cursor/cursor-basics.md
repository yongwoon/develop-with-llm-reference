# Cursor 基本使用法

## 📥 インストールと初期設定

### 1. Cursor インストール

```bash
# macOS
brew install --cask cursor

# または公式ウェブサイトからダウンロード
# https://cursor.sh/
```

### 2. 初期設定

#### アカウント連携

- Cursor 起動後、アカウント作成またはログイン
- GitHub アカウント連携推奨（プロジェクトコンテキスト向上）

#### 基本設定

- **Language**: 日本語設定（オプション）
- **Theme**: 好みのテーマ選択
- **Font**: コーディングフォント設定（Fira Code、JetBrains Mono など）

## 🎯 核心機能

### 1. AI 自動補完（Tab）

```typescript
// タイピング中にTabキーでAI提案を受け入れ
function calculateTotal(items: Product[]) {
  // Tabキー - AIが自動で補完
  return items.reduce((sum, item) => sum + item.price, 0);
}
```

### 2. チャットインターフェース（Cmd+L）

```bash
# チャットウィンドウで自然言語でリクエスト
"Create a React component for user profile card with avatar, name, and bio"

# コード説明リクエスト
"Explain this function and suggest improvements"

# バグ修正リクエスト
"Fix the performance issue in this component"
```

### 3. コード編集（Cmd+K）

```bash
# 選択したコードブロックを修正
"Convert this to TypeScript"
"Add error handling"
"Optimize for performance"
"Add comprehensive comments"
```

## ⌨️ 必須ショートカット

### 基本ショートカット

- **Cmd+L**: 新しいチャット開始
- **Cmd+K**: インラインコード編集
- **Cmd+I**: コード生成（作業中のファイルに）
- **Tab**: AI 提案受け入れ
- **Esc**: AI 提案キャンセル

### 高度なショートカット

- **Cmd+Shift+L**: チャット履歴
- **Cmd+/**: クイック質問
- **Cmd+Enter**: 選択範囲をチャットに追加
- **Cmd+Shift+Enter**: ファイル全体をチャットに追加

## 🔧 プロジェクト設定

### 1. プロジェクトルートに.cursorrules ファイル作成

```bash
# .cursorrulesファイル例
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

### 2. プロジェクト別設定

#### package.json 確認

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

#### tsconfig.json 最適化

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

## 💬 効果的なプロンプト作成法

### 1. 具体的な要求事項

```bash
# ❌ 曖昧なリクエスト
"Make a login form"

# ✅ 具体的なリクエスト
"Create a React login form component with:
- Email and password fields
- Form validation using Zod
- Submit handler with loading state
- Error message display
- Tailwind CSS styling
- TypeScript types"
```

### 2. コンテキスト提供

```bash
# 現在のプロジェクト構造説明
"Given our Next.js project structure with:
- App Router
- Prisma for database
- NextAuth for authentication

Create a protected route wrapper component that:
- Checks authentication status
- Redirects to login if not authenticated
- Shows loading spinner during check"
```

### 3. サンプルコード提供

````bash
# 既存コードスタイル参照
"Following the pattern used in components/ui/Button.tsx:

```typescript
// 既存Buttonコンポーネントスタイル
````

Create a similar Input component with validation states"

````

## 🎨 インターフェース理解

### 1. エディタ領域
- **メインエディタ**: コード作成・編集
- **AI提案オーバーレイ**: リアルタイム自動補完表示
- **インライン編集**: Cmd+Kで有効化される編集モード

### 2. サイドバー
- **ファイルエクスプローラー**: プロジェクトファイル構造
- **検索**: ファイル・コード検索
- **Git連携**: バージョン管理状態

### 3. チャットパネル
- **対話履歴**: 以前のチャット記録
- **コードブロック**: 生成されたコードプレビュー
- **適用ボタン**: 提案されたコード適用

## 🚀 開始ワークフロー

### 1. 新規プロジェクト設定
```bash
# 1. プロジェクト作成
npx create-next-app@latest my-project --typescript --tailwind --app

# 2. Cursorでプロジェクトを開く
cursor my-project

# 3. .cursorrulesファイル作成
# 4. プロジェクト構造説明チャット
````

### 2. 最初のコンポーネント作成

```bash
# チャットでリクエスト
"Create a header component with:
- Logo on the left
- Navigation menu in the center
- User profile dropdown on the right
- Responsive design
- TypeScript with proper types"
```

### 3. 機能実装

```bash
# 段階的機能追加
"Add search functionality to the header:
- Search input with icon
- Dropdown with search results
- Keyboard navigation (arrow keys, enter)"
```

## 📋 設定チェックリスト

Cursor 使用前の確認事項：

- [ ] Cursor インストール・ログイン
- [ ] プロジェクトオープン・構造把握
- [ ] .cursorrules ファイル作成
- [ ] 開発環境設定（Node.js、Git など）
- [ ] 必須ショートカット習得
- [ ] 最初のチャットテスト
- [ ] 自動補完機能テスト
- [ ] コード編集機能テスト

## 🔍 問題解決

### 一般的な問題

1. **自動補完が動作しない**

   - インターネット接続確認
   - Cursor 再起動
   - アカウントログイン状態確認

2. **チャット応答が遅い**

   - ネットワーク状態確認
   - 複雑なリクエストを小さな単位に分解
   - 不要なコンテキスト除去

3. **コード提案が不正確**
   - .cursorrules ファイル点検
   - プロジェクト構造説明追加
   - より具体的な要求事項提供

---

次へ：[Cursor Rules 設定ガイド](./cursor-rules.md) →
