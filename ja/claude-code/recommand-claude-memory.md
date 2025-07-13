# Claude Memory Tips

20 年以上の経験を持つ熟練したフルスタックウェブ開発者として、Claude Code を効果的に使用するためのメモリ構成を提案いたします。

## ユーザーメモリ (`~/.claude/CLAUDE.md`)

_全プロジェクトに共通して適用される個人環境設定_

### コーディングスタイルと設定

- 2 スペースインデントを使用
- セミコロンを常に使用
- 関数型プログラミングスタイルを優先 (map, filter, reduce など)
- async/await を使用 (Promise.then の代わりに)
- TypeScript を優先
- ESLint と Prettier 設定を適用

### 個人ツールとワークフロー

- VS Code エディターを使用
- Git コミットメッセージ規約 (feat:, fix:, docs: など)
- ショートカットとスニペットの設定
- テストツールの設定 (Jest, Vitest, Cypress など)
- パッケージマネージャーの設定 (npm, yarn, pnpm)

### アーキテクチャと設計原則

- コンポーネントベースアーキテクチャ
- 単一責任原則の遵守
- 依存性注入パターン
- エラーハンドリングアプローチ
- ログとモニタリングアプローチ

### 例

```txt
# ユーザーメモリ - 個人開発環境設定

## コーディングスタイルと設定

### 基本フォーマット
- 2スペースインデントを使用（タブではなくスペース）
- セミコロンを常に使用
- シングルクォートを優先（'string' 形式）
- オブジェクトと配列でtrailing commaを使用
- 80文字の行長制限

### JavaScript/TypeScript スタイル
- 関数型プログラミングスタイルを優先 (map, filter, reduce など)
- async/await を使用 (Promise.then の代わりに)
- TypeScript を優先 (any 型を禁止)
- アロー関数を優先 (ただし、メソッドは function キーワードを使用)
- 分割代入を積極的に活用

### React コンポーネントスタイル
- 関数型コンポーネントを使用 (クラスコンポーネントを禁止)
- カスタムフックを積極的に活用
- PropTypes の代わりに TypeScript インターフェースを使用
- コンポーネントファイル名は PascalCase

## 個人ツールとワークフロー

### エディターと拡張機能
- VS Code エディターを使用
- Prettier、ESLint 自動フォーマット設定
- Auto Import 拡張機能を使用
- GitLens 拡張機能を使用

### Git コミット規約
- feat: 新機能追加
- fix: バグ修正
- docs: ドキュメント更新
- style: コードフォーマット
- refactor: コードリファクタリング
- test: テストコード追加/修正
- chore: ビルドプロセスや補助ツールの修正

### パッケージマネージャー
- pnpm を優先 (npm、yarn の代わりに)
- package.json scripts コマンドを標準化
- 依存関係を定期的に更新

### テストツール
- Jest + Testing Library の組み合わせを優先
- Vitest を使用 (Vite プロジェクトで)
- E2E テストは Playwright を使用
- テストカバレッジ 80% 以上を維持

## アーキテクチャと設計原則

### コンポーネント設計
- 単一責任原則に従う
- 再利用可能なコンポーネントを作成
- Props drilling を防ぐ (Context API または状態管理ライブラリを使用)
- コンポーネントは最大 200 行に制限

### 状態管理
- ローカル状態は useState を使用
- グローバル状態は Zustand を優先
- サーバー状態は React Query/TanStack Query を使用
- フォーム状態は React Hook Form を使用

### エラーハンドリング
- try-catch ブロックを積極的に使用
- エラーバウンダリコンポーネントを実装
- ユーザーフレンドリーなエラーメッセージを提供
- エラーログシステムを構築

### パフォーマンス最適化
- React.memo を適切に使用
- useMemo、useCallback は必要な時のみ使用
- コード分割を適用 (React.lazy)
- 画像最適化 (Next.js Image コンポーネントを使用)

## 開発環境設定

### 環境変数管理
- .env.local ファイルを使用
- 環境別設定を分離 (.env.development, .env.production)
- 機密情報は絶対にコミットしない

### デバッグツール
- React Developer Tools を使用
- Chrome DevTools を積極的に活用
- console.log の代わりに debugger を優先
- パフォーマンスプロファイリングツールを使用

### 開発サーバー設定
- ホットリロードを有効化
- プロキシ設定で CORS 問題を解決
- 開発環境で HTTPS を使用 (mkcert を活用)

## ドキュメントとコミュニケーション

### コードコメント
- JSDoc 形式のコメントを使用
- 複雑なロジックに対する説明を追加
- TODO、FIXME コメントを活用

### ドキュメント作成
- README.md ファイルを詳細に作成
- API ドキュメントは OpenAPI/Swagger を使用
- コンポーネント Storybook ドキュメントを作成
```

## プロジェクトメモリ (`./CLAUDE.md`)

_特定プロジェクトに対するチーム共有ガイドライン_

### プロジェクトアーキテクチャ

- プロジェクト構造とフォルダ構成
- 主要技術スタック (React, Next.js, Express など)
- データベース設計と接続方法
- API 設計原則 (RESTful, GraphQL など)
- 状態管理方法 (Redux, Zustand, Context API など)

### コーディング標準

- 命名規約 (変数、関数、クラス、ファイル名)
- コンポーネント作成ルール
- 型定義方法
- エラー処理と例外対応
- コードレビューチェックリスト

### 開発環境設定

- 環境変数管理
- ビルドとデプロイ設定
- テスト環境構成
- ローカル開発サーバー設定
- Docker コンテナ設定

### 外部サービス連携

- 認証/認可システム
- 決済システム
- メールサービス
- クラウドストレージ
- サードパーティ API 連携方法

### ワークフローとデプロイ

- Git ブランチ戦略
- CI/CD パイプライン
- デプロイ環境 (開発、ステージング、本番)
- モニタリングとアラート設定
- バックアップと復旧手順

### ドキュメントとコミュニケーション

- API ドキュメント作成方法
- コードコメントガイドライン
- 変更履歴管理
- チーム内コミュニケーションルール

### 例

```txt
# プロジェクトメモリ - E-Commerce ウェブアプリケーション

## プロジェクト概要
- **プロジェクト名**: ShopMate E-commerce Platform
- **技術スタック**: Next.js 14, TypeScript, Tailwind CSS, Prisma, PostgreSQL
- **デプロイ環境**: Vercel (フロントエンド), Railway (データベース)
- **チーム構成**: 3名 (フロントエンド 2名, バックエンド 1名)

## プロジェクトアーキテクチャ

### フォルダ構造
"""
├── src/
│   ├── app/                 # Next.js 13+ App Router
│   ├── components/          # 再利用可能なコンポーネント
│   │   ├── ui/             # 基本 UI コンポーネント
│   │   ├── forms/          # フォーム関連コンポーネント
│   │   └── layout/         # レイアウトコンポーネント
│   ├── lib/                # ユーティリティ関数と設定
│   ├── hooks/              # カスタムフック
│   ├── types/              # TypeScript 型定義
│   └── store/              # 状態管理 (Zustand)
├── prisma/                 # データベーススキーマ
├── public/                 # 静的ファイル
└── tests/                  # テストファイル
"""

### 技術スタック詳細
- **フロントエンド**: Next.js 14 (App Router), React 18, TypeScript 5.0
- **スタイリング**: Tailwind CSS 3.3, Headless UI, Radix UI
- **状態管理**: Zustand (グローバル状態), React Query (サーバー状態)
- **データベース**: PostgreSQL with Prisma ORM
- **認証**: NextAuth.js with Google, GitHub providers
- **決済**: Stripe Integration
- **テスト**: Jest, React Testing Library, Playwright

## コーディング標準

### 命名規約
- **コンポーネント**: PascalCase (`UserProfile.tsx`)
- **関数/変数**: camelCase (`getUserData`)
- **定数**: UPPER_SNAKE_CASE (`API_BASE_URL`)
- **ファイル名**: kebab-case (`user-profile.tsx`) または PascalCase (コンポーネント)
- **API エンドポイント**: kebab-case (`/api/user-profile`)

### コンポーネント作成ルール
- 最大 200 行制限 (超過時は分割)
- Props インターフェース定義必須
- デフォルト props 値を設定
- エラーバウンダリを適用
- アクセシビリティを考慮 (ARIA 属性、キーボードナビゲーション)

### TypeScript ルール
- `any` 型の使用を禁止
- すべての API レスポンスに対する型定義
- ユニオン型を積極的に活用
- ジェネリック型を活用 (再利用性向上)

## API 設計原則

### RESTful API ルール
- **GET** `/api/products` - 商品一覧取得
- **GET** `/api/products/[id]` - 特定商品取得
- **POST** `/api/products` - 商品作成
- **PUT** `/api/products/[id]` - 商品全体更新
- **PATCH** `/api/products/[id]` - 商品部分更新
- **DELETE** `/api/products/[id]` - 商品削除

### レスポンス形式標準化
"""typescript
interface ApiResponse<T> {
  success: boolean;
  data?: T;
  error?: string;
  message?: string;
}
"""

### エラーハンドリング
- HTTP ステータスコードを適切に使用
- 一貫したエラーメッセージ形式
- 開発環境で詳細なエラー情報を提供
- 本番環境で機密情報を隠す

## データベース設計

### 主要テーブル
- **User**: ユーザー情報
- **Product**: 商品情報
- **Category**: 商品カテゴリ
- **Order**: 注文情報
- **OrderItem**: 注文商品詳細
- **Cart**: ショッピングカート
- **Review**: 商品レビュー

### Prisma スキーマルール
- すべてのモデルに `id`、`createdAt`、`updatedAt` フィールドを含める
- リレーション設定時に cascade オプションを明示
- インデックスを適切に設定
- ソフトデリートを実装 (`deletedAt` フィールド使用)

## 状態管理

### Zustand ストア構造
"""
├── store/
│   ├── auth-store.ts       # ユーザー認証状態
│   ├── cart-store.ts       # ショッピングカート状態
│   ├── product-store.ts    # 商品フィルタリング状態
│   └── ui-store.ts         # UI 状態 (モーダル、ローディングなど)
"""

### React Query 使用ルール
- サーバー状態管理専用
- クエリキーを標準化 (`['products', 'list', filters]`)
- 適切なキャッシュ時間を設定
- 楽観的更新を適用

## スタイリングガイド

### Tailwind CSS 使用ルール
- ユーティリティクラスを優先使用
- カスタム CSS を最小化
- コンポーネントバリエーションのための className 条件適用
- ダークモード対応 (`dark:` プレフィックスを使用)

### コンポーネントスタイリング
- 基本コンポーネントは `components/ui/` ディレクトリに配置
- ビジネスロジックとスタイルを分離
- 再利用可能なスタイルパターンを定義

## 認証と認可

### NextAuth.js 設定
- Google、GitHub OAuth プロバイダーを使用
- JWT トークンを使用
- セッション管理と自動更新
- ロールベースアクセス制御 (RBAC)

### セキュリティルール
- すべての API エンドポイントに認証ミドルウェアを適用
- CSRF トークンを使用
- XSS 攻撃を防ぐ (入力検証とエスケープ)
- 環境変数で機密情報を管理

## 決済システム

### Stripe 連携
- 決済情報の安全な処理
- ウェブフックを通じた決済状態同期
- 返金とキャンセル処理ロジック
- 決済失敗時の再試行メカニズム

## テスト戦略

### ユニットテスト
- すべてのユーティリティ関数をテスト
- コンポーネントレンダリングテスト
- API エンドポイントテスト
- 最低 80% のコードカバレッジを維持

### 統合テスト
- ユーザーフローテスト
- API 統合テスト
- データベース接続テスト

### E2E テスト
- 主要ユーザーシナリオテスト
- 決済フローテスト
- クロスブラウザテスト

## デプロイと DevOps

### デプロイ戦略
- **開発**: Vercel Preview デプロイ
- **ステージング**: 別の Vercel プロジェクト
- **本番**: メインドメインデプロイ

### CI/CD パイプライン
- GitHub Actions を使用
- 自動テスト実行
- コード品質チェック (ESLint, Prettier)
- 自動デプロイ (テスト通過時)

### モニタリング
- Vercel Analytics を使用
- エラートラッキング (Sentry 連携)
- パフォーマンスモニタリング (Web Vitals)

## 環境設定

### 環境変数
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

### 開発環境設定
- Node.js 18.x 以上を使用
- pnpm パッケージマネージャーを使用
- VS Code 拡張機能推奨リストを提供
- 開発サーバーポート: 3000番を使用

## ドキュメントルール

### README.md 必須内容
- プロジェクト説明と機能
- インストールと実行方法
- 環境変数設定ガイド
- デプロイ方法
- 貢献ガイドライン

### コードドキュメント
- 複雑なビジネスロジックにはコメント必須
- API エンドポイントの JSDoc 作成
- コンポーネント PropTypes ドキュメント
- データベーススキーマ説明を追加
```
