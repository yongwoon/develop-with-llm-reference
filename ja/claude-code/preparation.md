# 準備事項と環境設定

## 🛠 プロジェクト構造設定

### 基本ディレクトリ構造

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

### 環境設定ファイル

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

#### 2. 基本`package.json`構造

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

## 📋 明確な要求事項定義

### 1. 機能仕様書テンプレート

```markdown
# Feature: [機能名]

## 概要

[機能の簡単な説明]

## ユーザーストーリー

As a [ユーザータイプ]
I want to [実行したい作業]
So that [得たい価値]

## 受け入れ基準

- [ ] [テスト可能な条件 1]
- [ ] [テスト可能な条件 2]
- [ ] [テスト可能な条件 3]

## 技術要件

- Framework: [使用フレームワーク]
- Dependencies: [必要なライブラリ]
- API Integration: [連携する API]

## 制約

- Performance: [パフォーマンス要件]
- Security: [セキュリティ要件]
- Browser Support: [サポートブラウザ]
```

### 2. 技術スタック文書化

```markdown
# 技術スタック

## フロントエンド

- Framework: Next.js 14
- Language: TypeScript 5.x
- Styling: Tailwind CSS
- State Management: Zustand
- Form Handling: React Hook Form
- Validation: Zod

## バックエンド

- Runtime: Node.js 18+
- Framework: Express.js
- Database: PostgreSQL
- ORM: Prisma
- Authentication: JWT

## 開発ツール

- Package Manager: pnpm
- Linter: ESLint
- Formatter: Prettier
- Testing: Jest + React Testing Library
- E2E Testing: Playwright
```

### 3. API 仕様定義

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

## 🔧 開発環境準備

### 1. 必須ツールインストール

```bash
# Node.js (LTSバージョン推奨)
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs

# pnpmインストール
npm install -g pnpm

# プロジェクト依存関係インストール
pnpm install
```

### 2. VS Code 拡張機能

- ESLint
- Prettier
- TypeScript and JavaScript Language Features
- Tailwind CSS IntelliSense
- GitLens
- Error Lens

### 3. Git 設定

```bash
# 基本設定
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# 便利なエイリアス設定
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

## 📐 コーディング標準設定

### ESLint 設定 (`.eslintrc.json`)

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

### Prettier 設定 (`.prettierrc`)

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

## ✅ チェックリスト

プロジェクト開始前の確認事項：

- [ ] プロジェクトディレクトリ構造作成
- [ ] Git リポジトリ初期化
- [ ] 必須開発ツールインストール
- [ ] 環境設定ファイル準備
- [ ] 技術スタック文書作成
- [ ] コーディング標準設定
- [ ] CI/CD パイプライン構成（選択事項）
- [ ] README.md 作成

---

次: [効率的な開発段階](./development-stages.md) →
