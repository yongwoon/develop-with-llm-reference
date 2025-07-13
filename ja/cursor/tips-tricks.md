# Cursor 活用ヒント

## 🚀 生産性向上のヒント

### 1. スマート自動補完の活用

#### コンテキストベース補完

```typescript
// 既存パターン学習
const UserCard = ({ user }) => {
  // Tabキーで既存スタイルパターンを自動適用
  return (
    <div className="card user-card">
      <img src={user.avatar} alt={user.name} />
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
};

// 新しいコンポーネント作成時に自動で類似パターンを提案
const ProductCard = ({ product }) => {
  // CursorがUserCardパターンを学習して自動提案
  return (
    <div className="card product-card">
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <p>{product.price}</p>
    </div>
  );
};
```

#### 型ベース自動補完

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
  // CursorがUser型を分析して正確なプロパティを提案
  const updatedUser = {
    ...user,
    preferences: {
      ...user.preferences,
      theme: "dark", // 自動で'light' | 'dark'型を提案
    },
  };

  return updatedUser;
}
```

### 2. チャットインターフェース最適化

#### 具体的なリクエスト作成

```bash
# ❌ 曖昧なリクエスト
"コンポーネント作って"

# ✅ 具体的なリクエスト
"ユーザープロフィールカードコンポーネントを作成してください：
- Props: user（User型）
- アバター画像（丸型）
- 名前とメール表示
- 編集ボタン（右上）
- Tailwind CSS使用
- ホバー効果含む"
```

#### コードコンテキスト提供

````bash
# 既存コード参照
"現在のButtonコンポーネントと同じスタイルでModalコンポーネントを作成してください：

```typescript
// 既存Buttonコンポーネント
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

Modal も同じデザインシステムに従うようにしてください。"

````

### 3. ファイル管理最適化

#### 関連ファイルの同時オープン
```bash
# 関連ファイルを一緒に開くとより正確な提案
components/
├── UserProfile.tsx     # メインコンポーネント
├── UserCard.tsx        # 参照コンポーネント
├── Button.tsx          # 共通コンポーネント
types/
├── User.ts            # 型定義
hooks/
├── useAuth.ts         # 関連フック
utils/
├── validation.ts      # ユーティリティ関数
````

#### ファイル構造の一貫性

```typescript
// 一貫したファイル構造でより良い提案を受ける
// components/UserProfile/index.tsx
export { UserProfile } from "./UserProfile";
export { UserCard } from "./UserCard";
export { UserForm } from "./UserForm";

// components/UserProfile/UserProfile.tsx
import { UserCard } from "./UserCard";
import { UserForm } from "./UserForm";
```

## 🎯 高度な機能活用

### 1. コード編集（Cmd+K）をマスターする

#### 選択的リファクタリング

```typescript
// 既存コード
function calculateTotal(items) {
  let total = 0;
  for (let i = 0; i < items.length; i++) {
    total += items[i].price;
  }
  return total;
}

// Cmd+Kで選択後「TypeScriptに変換して最適化してください」
function calculateTotal(items: Item[]): number {
  return items.reduce((total, item) => total + item.price, 0);
}
```

#### エラーハンドリング追加

```typescript
// 既存コード
async function fetchUser(id: string) {
  const response = await fetch(`/api/users/${id}`);
  return response.json();
}

// Cmd+Kで選択後「エラーハンドリングを追加してください」
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

### 2. マルチカーソルと AI の組み合わせ

#### 繰り返し作業の自動化

```typescript
// 複数行選択後パターン適用
const user1 = { id: "1", name: "John" };
const user2 = { id: "2", name: "Jane" };
const user3 = { id: "3", name: "Bob" };

// Cmd+Kで「各ユーザーに対してvalidation関数生成」
const validateUser1 = (user: User) => user.id === "1" && user.name === "John";
const validateUser2 = (user: User) => user.id === "2" && user.name === "Jane";
const validateUser3 = (user: User) => user.id === "3" && user.name === "Bob";
```

### 3. プロジェクト全体分析活用

#### コードベースパターン学習

```typescript
// Cursorがプロジェクト全体からパターンを学習
// 1. 既存API呼び出しパターン
const useUser = (id: string) => {
  return useQuery(["user", id], () => fetchUser(id));
};

// 2. 新しいフック生成時に自動で同じパターンを提案
const useProduct = (id: string) => {
  return useQuery(["product", id], () => fetchProduct(id));
};
```

## 🛠 ワークフロー最適化

### 1. 開発段階別活用

#### プロトタイピング段階

```bash
# 迅速なコンポーネント生成
"シンプルなログインフォームを作成してください：
- メールとパスワード入力
- ログインボタン
- 基本スタイリング
- 状態管理はuseStateを使用"
```

#### 実装段階

```bash
# 詳細な機能実装
"ログインフォームを以下のように改善してください：
- React Hook Form使用
- Zodスキーマvalidation
- ローディング状態表示
- エラーメッセージ表示
- 自動フォーカス機能"
```

#### 最適化段階

```bash
# パフォーマンス最適化
"現在のコンポーネントのパフォーマンスを最適化してください：
- 不要な再レンダリング防止
- メモ化適用
- バンドルサイズ最適化
- アクセシビリティ改善"
```

### 2. チーム協業ワークフロー

#### コンベンション統一

```markdown
# .cursorrules ファイルでチームコンベンション統一

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

#### コードレビュー最適化

```bash
# コードレビュー用説明生成
"この関数が何をするかを説明し、
潜在的な問題点と改善案を提示してください"

# テストコード生成
"このコンポーネントのJestテストを作成してください：
- レンダリングテスト
- ユーザーインタラクションテスト
- エラー状況テスト"
```

### 3. デバッグワークフロー

#### エラー分析

```typescript
// エラー発生コード
const UserList = ({ users }) => {
  return (
    <div>
      {users.map(user => (
        <UserCard key={user.id} user={user} />
      ))}
    </div>
  );
};

// Cursorにエラー分析リクエスト
"このコードで'Cannot read property map of undefined'エラーが発生します。
原因と解決方法を教えてください"
```

#### ログ追加

```bash
# デバッグ用ログ追加
"この関数に適切なログを追加してください：
- 関数入出力ログ
- 重要な変数状態ログ
- エラー発生時詳細ログ"
```

## 🎨 コード品質向上

### 1. 自動リファクタリング

#### コードクリーンアップ

```typescript
// 複雑なコード
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

// Cmd+Kで「このコードをより綺麗にリファクタリングしてください」
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

### 2. 型安全性強化

#### 型ガード生成

```typescript
// 既存コード
function handleUserData(data: unknown) {
  // 型検証なしで使用
  console.log(data.name);
}

// Cursorに「型安全性のための型ガード追加」
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
    console.log(data.name); // 型安全
  }
}
```

### 3. パフォーマンス最適化

#### メモ化適用

```typescript
// 最適化前
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

// Cmd+Kで「パフォーマンス最適化適用」
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

## 🔧 トラブルシューティングガイド

### 1. 自動補完が動作しない場合

#### チェックリスト

```bash
# 1. ネットワーク接続確認
curl -I https://api.cursor.sh/health

# 2. ファイル拡張子確認
.js, .jsx, .ts, .tsxなど対応拡張子か確認

# 3. プロジェクトルート確認
package.jsonや.gitフォルダがあるディレクトリで作業

# 4. メモリ使用量確認
大きなファイルや複雑なプロジェクトでメモリ不足の可能性
```

#### 解決方法

```bash
# 1. Cursor再起動
Cmd+Shift+P → "Reload Window"

# 2. キャッシュクリア
Cmd+Shift+P → "Clear Cache"

# 3. 設定初期化
~/.cursor/User/settings.json削除後再起動
```

### 2. 不正確な提案が出る場合

#### コンテキスト改善

```bash
# 1. .cursorrulesファイル更新
より具体的なプロジェクトルール追加

# 2. 関連ファイルを開く
参照するファイルをエディタで開いておく

# 3. 型定義明確化
TypeScript型をより正確に定義
```

### 3. パフォーマンス問題解決

#### 最適化設定

```json
// settings.json
{
  "cursor.ai.maxTokens": 2000,
  "cursor.ai.temperature": 0.3,
  "cursor.ai.contextWindow": 8000
}
```

#### リソース管理

```bash
# 1. 不要なファイル除外
.gitignoreに大容量ファイル追加

# 2. プロジェクトサイズ最適化
node_modules、dist、buildなど除外

# 3. ファイル数制限
同時に多くのファイルを開かない
```

## ✅ 効率性チェックリスト

### 基本設定

- [ ] .cursorrules ファイル作成
- [ ] プロジェクト構造整理
- [ ] 必須ショートカット習得
- [ ] 関連ファイルグループ化

### 作業方式

- [ ] 具体的なリクエスト作成
- [ ] コンテキストファイル事前オープン
- [ ] 段階的アプローチ使用
- [ ] 定期的なコードレビュー

### 品質管理

- [ ] 型安全性確認
- [ ] エラーハンドリング実装
- [ ] テストコード作成
- [ ] パフォーマンス最適化適用

### チーム協業

- [ ] コンベンション文書化
- [ ] 共通ルール設定
- [ ] コードレビュープロセス
- [ ] 知識共有セッション

---

[← 前へ：Claude Code vs Cursor 比較](./comparison.md) | [ホーム →](./README.md)
