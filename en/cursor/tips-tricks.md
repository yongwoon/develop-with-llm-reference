# Cursor Tips & Tricks

## 🚀 Productivity Enhancement Tips

### 1. Leveraging Smart Autocomplete

#### Context-Based Completion

```typescript
// Learning existing patterns
const UserCard = ({ user }) => {
  // Tab key automatically applies existing style patterns
  return (
    <div className="card user-card">
      <img src={user.avatar} alt={user.name} />
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
};

// When writing new components, automatically suggests similar patterns
const ProductCard = ({ product }) => {
  // Cursor learns from UserCard pattern and auto-suggests
  return (
    <div className="card product-card">
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <p>{product.price}</p>
    </div>
  );
};
```

#### Type-Based Autocomplete

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
  // Cursor analyzes User type and suggests accurate properties
  const updatedUser = {
    ...user,
    preferences: {
      ...user.preferences,
      theme: "dark", // Automatically suggests 'light' | 'dark' type
    },
  };

  return updatedUser;
}
```

### 2. Optimizing Chat Interface

#### Writing Specific Requests

```bash
# ❌ Vague request
"Create a component"

# ✅ Specific request
"Create a user profile card component:
- Props: user (User type)
- Avatar image (rounded)
- Display name and email
- Edit button (top right)
- Use Tailwind CSS
- Include hover effects"
```

#### Providing Code Context

````bash
# Referencing existing code
"Create a Modal component with the same style as the current Button component:

```typescript
// Existing Button component
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
```

Make the Modal follow the same design system."
````

### 3. Optimizing File Management

#### Opening Related Files Simultaneously

```bash
# Opening related files together provides more accurate suggestions
components/
├── UserProfile.tsx     # Main component
├── UserCard.tsx        # Reference component
├── Button.tsx          # Common component
types/
├── User.ts            # Type definitions
hooks/
├── useAuth.ts         # Related hooks
utils/
├── validation.ts      # Utility functions
```

#### File Structure Consistency

```typescript
// Consistent file structure for better suggestions
// components/UserProfile/index.tsx
export { UserProfile } from "./UserProfile";
export { UserCard } from "./UserCard";
export { UserForm } from "./UserForm";

// components/UserProfile/UserProfile.tsx
import { UserCard } from "./UserCard";
import { UserForm } from "./UserForm";
```

## 🎯 Advanced Feature Utilization

### 1. Mastering Code Editing (Cmd+K)

#### Selective Refactoring

```typescript
// Original code
function calculateTotal(items) {
  let total = 0;
  for (let i = 0; i < items.length; i++) {
    total += items[i].price;
  }
  return total;
}

// Select with Cmd+K and ask "Convert to TypeScript and optimize"
function calculateTotal(items: Item[]): number {
  return items.reduce((total, item) => total + item.price, 0);
}
```

#### Adding Error Handling

```typescript
// Original code
async function fetchUser(id: string) {
  const response = await fetch(`/api/users/${id}`);
  return response.json();
}

// Select with Cmd+K and ask "Add error handling"
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

### 2. Combining Multi-cursor with AI

#### Automating Repetitive Tasks

```typescript
// Select multiple lines and apply patterns
const user1 = { id: "1", name: "John" };
const user2 = { id: "2", name: "Jane" };
const user3 = { id: "3", name: "Bob" };

// Use Cmd+K to "Generate validation function for each user"
const validateUser1 = (user: User) => user.id === "1" && user.name === "John";
const validateUser2 = (user: User) => user.id === "2" && user.name === "Jane";
const validateUser3 = (user: User) => user.id === "3" && user.name === "Bob";
```

### 3. Utilizing Project-Wide Analysis

#### Learning Codebase Patterns

```typescript
// Cursor learns patterns from entire project
// 1. Existing API call pattern
const useUser = (id: string) => {
  return useQuery(["user", id], () => fetchUser(id));
};

// 2. When creating new hooks, automatically suggests same pattern
const useProduct = (id: string) => {
  return useQuery(["product", id], () => fetchProduct(id));
};
```

## 🛠 Workflow Optimization

### 1. Stage-by-Stage Utilization

#### Prototyping Stage

```bash
# Quick component creation
"Create a simple login form:
- Email and password inputs
- Login button
- Basic styling
- Use useState for state management"
```

#### Implementation Stage

```bash
# Detailed feature implementation
"Improve the login form as follows:
- Use React Hook Form
- Zod schema validation
- Show loading state
- Display error messages
- Auto-focus functionality"
```

#### Optimization Stage

```bash
# Performance optimization
"Optimize the current component for performance:
- Prevent unnecessary re-renders
- Apply memoization
- Optimize bundle size
- Improve accessibility"
```

### 2. Team Collaboration Workflow

#### Unifying Conventions

```markdown
# Unify team conventions with .cursorrules file

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

#### Optimizing Code Reviews

```bash
# Generate explanations for code reviews
"Explain what this function does,
and suggest potential issues and improvements"

# Generate test code
"Write Jest tests for this component:
- Rendering tests
- User interaction tests
- Error scenario tests"
```

### 3. Debugging Workflow

#### Error Analysis

```typescript
// Error-prone code
const UserList = ({ users }) => {
  return (
    <div>
      {users.map(user => (
        <UserCard key={user.id} user={user} />
      ))}
    </div>
  );
};

// Ask Cursor for error analysis
"This code throws 'Cannot read property map of undefined' error.
Please explain the cause and solution"
```

#### Adding Logs

```bash
# Add debugging logs
"Add appropriate logs to this function:
- Function entry/exit logs
- Important variable state logs
- Detailed error logs"
```

## 🎨 Improving Code Quality

### 1. Automatic Refactoring

#### Code Cleanup

```typescript
// Complex code
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

// Use Cmd+K to "Refactor this code to be cleaner"
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

### 2. Strengthening Type Safety

#### Generating Type Guards

```typescript
// Original code
function handleUserData(data: unknown) {
  // Using without type validation
  console.log(data.name);
}

// Ask Cursor to "Add type guard for type safety"
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
    console.log(data.name); // Type safe
  }
}
```

### 3. Performance Optimization

#### Applying Memoization

```typescript
// Before optimization
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

// Use Cmd+K to "Apply performance optimization"
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

## 🔧 Troubleshooting Guide

### 1. When Autocomplete Doesn't Work

#### Checklist

```bash
# 1. Check network connection
curl -I https://api.cursor.sh/health

# 2. Check file extension
Ensure it's a supported extension like .js, .jsx, .ts, .tsx

# 3. Check project root
Work in directory with package.json or .git folder

# 4. Check memory usage
Large files or complex projects may cause memory issues
```

#### Solutions

```bash
# 1. Restart Cursor
Cmd+Shift+P → "Reload Window"

# 2. Clear cache
Cmd+Shift+P → "Clear Cache"

# 3. Reset settings
Delete ~/.cursor/User/settings.json and restart
```

### 2. When Getting Inaccurate Suggestions

#### Improve Context

```bash
# 1. Update .cursorrules file
Add more specific project rules

# 2. Open related files
Keep reference files open in editor

# 3. Clarify type definitions
Define TypeScript types more accurately
```

### 3. Solving Performance Issues

#### Optimization Settings

```json
// settings.json
{
  "cursor.ai.maxTokens": 2000,
  "cursor.ai.temperature": 0.3,
  "cursor.ai.contextWindow": 8000
}
```

#### Resource Management

```bash
# 1. Exclude unnecessary files
Add large files to .gitignore

# 2. Optimize project size
Exclude node_modules, dist, build, etc.

# 3. Limit file count
Don't open too many files simultaneously
```

## ✅ Efficiency Checklist

### Basic Setup

- [ ] Write .cursorrules file
- [ ] Organize project structure
- [ ] Learn essential shortcuts
- [ ] Group related files

### Working Method

- [ ] Write specific requests
- [ ] Open context files in advance
- [ ] Use step-by-step approach
- [ ] Regular code reviews

### Quality Management

- [ ] Verify type safety
- [ ] Implement error handling
- [ ] Write test code
- [ ] Apply performance optimization

### Team Collaboration

- [ ] Document conventions
- [ ] Set common rules
- [ ] Code review process
- [ ] Knowledge sharing sessions

---

[← Previous: Claude Code vs Cursor Comparison](./comparison.md) | [Home →](./README.md)
