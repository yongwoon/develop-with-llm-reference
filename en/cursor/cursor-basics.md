# Cursor Basic Usage

## 📥 Installation and Initial Setup

### 1. Cursor Installation

```bash
# macOS
brew install --cask cursor

# Or download from official website
# https://cursor.sh/
```

### 2. Initial Setup

#### Account Connection

- Create account or login after launching Cursor
- GitHub account integration recommended (improves project context)

#### Basic Settings

- **Language**: Set to English (optional)
- **Theme**: Choose preferred theme
- **Font**: Set coding font (Fira Code, JetBrains Mono, etc.)

## 🎯 Core Features

### 1. AI Auto-completion (Tab)

```typescript
// Auto-completion with Tab key during typing
function calculateTotal(items: Product[]) {
  // Tab key - AI automatically completes
  return items.reduce((sum, item) => sum + item.price, 0);
}
```

### 2. Chat Interface (Cmd+L)

```bash
# Natural language requests in chat
"Create a React component for user profile card with avatar, name, and bio"

# Request code explanation
"Explain this function and suggest improvements"

# Request bug fixes
"Fix the performance issue in this component"
```

### 3. Code Editing (Cmd+K)

```bash
# Modify selected code block
"Convert this to TypeScript"
"Add error handling"
"Optimize for performance"
"Add comprehensive comments"
```

## ⌨️ Essential Shortcuts

### Basic Shortcuts

- **Cmd+L**: Start new chat
- **Cmd+K**: Inline code editing
- **Cmd+I**: Code generation (in working file)
- **Tab**: Accept AI suggestion
- **Esc**: Cancel AI suggestion

### Advanced Shortcuts

- **Cmd+Shift+L**: Chat history
- **Cmd+/**: Quick question
- **Cmd+Enter**: Add selection to chat
- **Cmd+Shift+Enter**: Add entire file to chat

## 🔧 Project Setup

### 1. Create .cursorrules file in project root

```bash
# .cursorrules file example
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

### 2. Project-specific Settings

#### package.json Check

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

#### tsconfig.json Optimization

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

## 💬 Effective Prompt Writing

### 1. Specific Requirements

```bash
# ❌ Vague request
"Make a login form"

# ✅ Specific request
"Create a React login form component with:
- Email and password fields
- Form validation using Zod
- Submit handler with loading state
- Error message display
- Tailwind CSS styling
- TypeScript types"
```

### 2. Provide Context

```bash
# Explain current project structure
"Given our Next.js project structure with:
- App Router
- Prisma for database
- NextAuth for authentication

Create a protected route wrapper component that:
- Checks authentication status
- Redirects to login if not authenticated
- Shows loading spinner during check"
```

### 3. Provide Example Code

````bash
# Reference existing code style
"Following the pattern used in components/ui/Button.tsx:

```typescript
// Existing Button component style
````

Create a similar Input component with validation states"

````

## 🎨 Interface Understanding

### 1. Editor Area
- **Main Editor**: Code writing and editing
- **AI Suggestion Overlay**: Real-time auto-completion display
- **Inline Editing**: Editing mode activated with Cmd+K

### 2. Sidebar
- **File Explorer**: Project file structure
- **Search**: File and code search
- **Git Integration**: Version control status

### 3. Chat Panel
- **Conversation History**: Previous chat records
- **Code Blocks**: Generated code preview
- **Apply Button**: Apply suggested code

## 🚀 Getting Started Workflow

### 1. New Project Setup
```bash
# 1. Create project
npx create-next-app@latest my-project --typescript --tailwind --app

# 2. Open project in Cursor
cursor my-project

# 3. Create .cursorrules file
# 4. Explain project structure in chat
````

### 2. First Component Creation

```bash
# Request in chat
"Create a header component with:
- Logo on the left
- Navigation menu in the center
- User profile dropdown on the right
- Responsive design
- TypeScript with proper types"
```

### 3. Feature Implementation

```bash
# Incremental feature addition
"Add search functionality to the header:
- Search input with icon
- Dropdown with search results
- Keyboard navigation (arrow keys, enter)"
```

## 📋 Setup Checklist

Pre-Cursor usage checklist:

- [ ] Install and login to Cursor
- [ ] Open project and understand structure
- [ ] Create .cursorrules file
- [ ] Set up development environment (Node.js, Git, etc.)
- [ ] Learn essential shortcuts
- [ ] Test first chat
- [ ] Test auto-completion feature
- [ ] Test code editing feature

## 🔍 Troubleshooting

### Common Issues

1. **Auto-completion not working**

   - Check internet connection
   - Restart Cursor
   - Verify account login status

2. **Slow chat responses**

   - Check network status
   - Break complex requests into smaller units
   - Remove unnecessary context

3. **Inaccurate code suggestions**
   - Check .cursorrules file
   - Add project structure explanation
   - Provide more specific requirements

---

Next: [Cursor Rules Setup Guide](./cursor-rules.md) →
