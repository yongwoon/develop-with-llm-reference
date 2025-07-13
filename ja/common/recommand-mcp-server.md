# フルスタック開発者のための MCP サーバー推奨ガイド

## 🚀 フルスタック開発者のための推奨優先順位

### 1 段階（必須インストール）

1. **GitHub MCP Server** - コード管理の核心
2. **Filesystem MCP Server** - ファイルシステム操作
3. **Git MCP Server** - バージョン管理
4. **PostgreSQL MCP Server** - データベース管理
5. **Fetch MCP Server** - API 開発とテスト
6. **Playwright MCP Server** - モダンウェブテスト自動化

### 2 段階（高級開発）

7. **Supabase MCP Server** - モダンバックエンドサービス
8. **Brave Search MCP Server** - 技術リサーチ
9. **Memory MCP Server** - プロジェクト状態管理
10. **Docker MCP Server** - コンテナ管理
11. **Kubernetes MCP Server** - クラスター管理
12. **Context7 MCP Server** - 高級コンテキスト管理
13. **Task-Master-AI MCP Server** - AI ベースタスク管理

### 3 段階（特化機能）

14. **Figma Context MCP Server** - デザイン連動
15. **Terraform MCP Server** - インフラ管理
16. **Slack MCP Server** - チーム協業
17. **Pandoc MCP Server** - ドキュメント自動化
18. **Tavily MCP Server** - AI 検索
19. **Sequential-Thinking MCP Server** - 論理的問題解決

---

## 🚀 必須 MCP サーバー（優先度高）

### 1. GitHub MCP Server

- **用途**: Git リポジトリ管理、イシュートラッキング、PR 管理
- **インストール**: `npx -y @modelcontextprotocol/server-github`
- **環境変数**: `GITHUB_TOKEN`
- **推奨理由**: 20 年以上の経験を持つフルスタック開発者に必須的なバージョン管理ツール

### 2. Filesystem MCP Server

- **用途**: ローカルファイルシステム操作、ファイル検索、メタデータ分析
- **インストール**: `npx -y @mcp/filesystem` または `npx -y @modelcontextprotocol/server-filesystem`
- **推奨理由**: すべての開発作業の基礎となるファイル管理

### 3. Git MCP Server

- **用途**: Git コマンド実行、ブランチ管理、コミット履歴照会
- **インストール**: `npx -y @modelcontextprotocol/server-git`
- **推奨理由**: バージョン管理と協業のための核心ツール

## 🗄️ データベース連動（フルスタック開発必須）

### 4. PostgreSQL MCP Server

- **用途**: データベースクエリ、スキーマ管理、データ分析
- **インストール**: `npx -y @modelcontextprotocol/server-postgres`
- **環境変数**: データベース接続情報
- **推奨理由**: エンタープライズ級データベース作業

### 5. SQLite MCP Server

- **用途**: 軽量データベースクエリと管理
- **インストール**: `npx -y @modelcontextprotocol/server-sqlite`
- **推奨理由**: プロトタイピングと開発環境で有用

### 6. MySQL MCP Server

- **用途**: MySQL データベース作業
- **インストール**: `npx -y mcp-server-mysql`
- **推奨理由**: レガシーシステム連動時に必要

## 🌐 ウェブ開発特化 MCP サーバー

### 7. Fetch MCP Server

- **用途**: HTTP リクエスト、REST API テストとデバッグ
- **インストール**: `npx -y @modelcontextprotocol/server-fetch`
- **推奨理由**: API 開発とテストに必須

### 8. Puppeteer/Playwright MCP Server

- **用途**: ウェブスクレイピング、E2E テスト、ブラウザ自動化
- **インストール**: `npx -y @modelcontextprotocol/server-puppeteer` または `npx -y mcp-server-playwright`
- **推奨理由**: ウェブアプリケーションテスト自動化

### 9. Firecrawl MCP Server

- **用途**: ウェブスクレイピング、競合他社リサーチ、データ抽出
- **インストール**: `npx -y @firecrawl/mcp-server`
- **環境変数**: `FIRECRAWL_API_KEY`
- **推奨理由**: 高級ウェブスクレイピング機能

### 10. Browserbase MCP Server

- **用途**: ブラウザ自動化、ウェブアプリケーションテスト、スクリーンショット撮影
- **環境変数**: `BROWSERBASE_API_KEY`, `BROWSERBASE_PROJECT_ID`
- **推奨理由**: クラウドベースブラウザ自動化

## 🎨 デザイン＆協業ツール

### 11. Figma Context MCP Server

- **用途**: Figma デザイン統合、デザイン仕様確認、コンポーネント関係把握
- **インストール**: `npx -y figma-context-mcp`
- **環境変数**: `FIGMA_ACCESS_TOKEN`
- **推奨理由**: デザインと開発間の円滑な連結

### 12. Slack MCP Server

- **用途**: Slack ワークスペース連動、チーム協業
- **インストール**: `npx -y mcp-server-slack`
- **推奨理由**: チームコミュニケーション自動化

## 📊 データ処理＆文書化

### 13. Excel MCP Server

- **用途**: Excel スプレッドシート処理、データ分析、レポート生成
- **インストール**: `npx -y excel-mcp-server`
- **推奨理由**: ビジネスデータ処理

### 14. Pandoc MCP Server

- **用途**: ドキュメントフォーマット変換（マークダウン、PDF、HTML、DOCX）
- **インストール**: `npx -y mcp-pandoc`
- **前提条件**: Pandoc システムインストール必要
- **推奨理由**: ドキュメント自動化

### 15. Google Drive MCP Server

- **用途**: クラウドストレージ統合、チーム協業、ドキュメント管理
- **インストール**: `npx -y @mcp/gdrive`
- **環境変数**: Google OAuth 認証情報
- **推奨理由**: クラウドベースドキュメント管理

### 16. Pandas MCP Server

- **用途**: データ分析と処理
- **インストール**: `npx -y mcp-server-pandas`
- **推奨理由**: データサイエンス作業

## 🔍 リサーチ＆検索

### 17. Brave Search MCP Server

- **用途**: プライバシー中心ウェブ検索、技術リサーチ
- **インストール**: `npx -y @mcp/brave-search`
- **環境変数**: `BRAVE_API_KEY`
- **推奨理由**: リアルタイム技術文書検索

### 18. Tavily MCP Server

- **用途**: AI ベース検索、文脈的検索結果
- **インストール**: `npx -y mcp-server-tavily`
- **環境変数**: `TAVILY_API_KEY`
- **推奨理由**: 高級 AI 検索機能

## 🏗️ インフラ＆DevOps（Infrastructure as Code）

### 19. AWS Terraform MCP Server（公式）

- **用途**: AWS ベストプラクティス、IaC パターン、Checkov セキュリティコンプライアンス
- **提供**: AWS Labs 公式サポート
- **機能**: CDK、Terraform などのワークフロー自動化
- **リポジトリ**: awslabs/mcp

### 20. HashiCorp Terraform MCP Server（公式）

- **用途**: Terraform Registry API 統合、IaC 開発自動化
- **機能**: Terraform レジストリデータを活用した設定作成支援
- **リポジトリ**: hashicorp/terraform-mcp-server

### 21. Terraform Cloud MCP Server

- **用途**: Terraform Cloud API 統合、ワークスペースと実行管理
- **機能**: 自然言語でインフラ管理、計画と適用
- **リポジトリ**: severity1/terraform-cloud-mcp

### 22. Kubernetes MCP Server

- **用途**: Kubernetes クラスター接続と管理
- **機能**: kubeconfig 自動感知、すべての K8s/OpenShift リソース管理
- **リポジトリ**: Flux159/mcp-server-kubernetes または manusa/kubernetes-mcp-server

### 23. Docker MCP Server

- **用途**: Docker コンテナとコンポーズスタック管理
- **機能**: Claude AI を通じたコンテナ作業自動化
- **リポジトリ**: QuantGeekDev/docker-mcp または ckreiling/mcp-server-docker

## 🛠️ 追加開発ツール

### 24. Memory MCP Server

- **用途**: セッション間コンテキスト維持、プロジェクト状態保存、メモリ状態モニタリング
- **推奨理由**: 長期プロジェクト管理に有用

### 25. Time MCP Server

- **用途**: 時間関連作業とスケジューリング
- **推奨理由**: 作業スケジューリングと時間管理

### 26. Magic MCP Server

- **用途**: AI ベース画像生成、テキスト変換、コード生成
- **インストール**: `npx -y @21st/magic-mcp`
- **環境変数**: `OPENAI_API_KEY`
- **推奨理由**: AI ベースコンテンツ生成

### 27. Mindmap MCP Server

- **用途**: アイデア視覚化、プロジェクトアーキテクチャ計画
- **インストール**: `npx -y mindmap-mcp-server`
- **推奨理由**: プロジェクト設計とアイデア整理

### 28. Context7 MCP Server

- **用途**: 高級コンテキスト管理、プロジェクト状態追跡
- **推奨理由**: 複雑なプロジェクトのコンテキスト維持

### 29. Sequential-Thinking MCP Server

- **用途**: 順次思考プロセス、論理的問題解決
- **推奨理由**: 複雑な開発問題の体系的アプローチ

### 30. Playwright MCP Server

- **用途**: ウェブスクレイピング、E2E テスト、ブラウザ自動化
- **インストール**: `npx -y mcp-server-playwright`
- **推奨理由**: モダンウェブテスト自動化（Puppeteer の進化型）

### 31. Task-Master-AI MCP Server

- **用途**: AI ベースタスク管理、プロジェクト計画自動化
- **推奨理由**: 開発作業の知的管理

### 32. Supabase MCP Server

- **用途**: Supabase バックエンドサービス連動、リアルタイムデータベース管理
- **推奨理由**: モダンバックエンドサービス統合

## 📝 インストールと設定例

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/path/to/your/project"
      ]
    },
    "git": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-git",
        "--repository",
        "/path/to/repo"
      ]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "your-github-token"
      }
    },
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "POSTGRES_CONNECTION_STRING": "postgresql://user:password@localhost:5432/database"
      }
    },
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

## 📚 追加リソース

- **Anthropic MCP 公式文書**: https://docs.anthropic.com
- **Claude Code サポート**: https://support.anthropic.com
- **コミュニティ MCP サーバー**: GitHub で「mcp-server」検索

20 年以上の経験を持つフルスタック開発者なら、上記の MCP サーバーを段階的に導入して Claude Code と共に生産性を最大化できます。特に 1 段階必須サーバーから始めて、プロジェクト要求事項に合わせて拡張していくことをお勧めします。
