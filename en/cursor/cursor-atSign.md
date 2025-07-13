# Cursor @ Symbol Usage Guide

Using the @ symbol in Cursor allows you to provide various contexts to AI, enabling more accurate and effective code generation. This guide details the usage and application scenarios of each @ function.

## 📋 @ Symbol Overview

The @ symbol is a powerful tool in Cursor for referencing specific contexts to AI. You can navigate suggestions with arrow keys and select with `Enter`. When you select a category (e.g., Files), related items within that category are filtered and displayed.

## 🔧 Key @ Functions

### 1. **@Files** - File Reference

#### Usage

```
@filename.js
@package.json
@README.md
```

#### When to Use

- When AI needs to reference specific file contents
- When generating code based on file structure or configuration
- When maintaining consistency with existing files

#### Usage Examples

```
Reference @package.json to create an npm install command for adding a new dependency
Write database connection code based on @config.js settings
```

#### Advantages

- Fast selection with file auto-completion
- Code generation based on accurate file contents

#### Disadvantages

- Large files may include unnecessary context

---

### 2. **@Folders** - Folder Reference

#### Usage

```
@utils/
@components/
@src/services/
```

#### When to Use

- When AI needs to understand the entire folder structure
- When working with most files in a folder
- When creating new files that match folder patterns

#### Usage Examples

```
Reference @components/ folder structure to create a new Button component
Write a new utility function following @utils/ folder patterns
```

#### Advantages

- Provides entire folder context at once
- Maintains consistent code style and structure

#### Disadvantages

- Large folders may cause performance degradation due to excessive context

---

### 3. **@Code** - Code Symbol Reference

#### Usage

```
@functionName
@ClassName
@CONSTANT_NAME
@variableName
```

#### When to Use

- When referencing specific function or class implementations
- When writing new code following existing code patterns
- When refactoring or extending work

#### Usage Examples

```
Reference @LRUCachedFunction implementation to create a similar caching function
Write AdminModel class based on @UserModel class
```

#### Advantages

- Very precise code reference
- Provides accurate context for specific symbols

#### Disadvantages

- Requires deep understanding of codebase
- Need to know exact symbol names

---

### 4. **@Docs** - Documentation Reference

#### Usage

```
@React
@Express
@TypeScript
@Docs → Add new doc (add custom documentation)
```

#### When to Use

- When referencing specific library or framework documentation
- When utilizing team internal documentation or guidelines
- When checking latest API usage

#### Usage Examples

```
Reference @React documentation to write data fetching code using useEffect hook
Create middleware function based on @Express documentation
```

#### Advantages

- Utilizes accurate information from official documentation
- Reflects latest API usage

#### Disadvantages

- Supported libraries may be limited

---

### 5. **@Git** - Git History Reference

#### Usage

```
@Git
```

#### When to Use

- When referencing recent changes
- When working based on code history
- When fixing bugs or performing rollbacks

#### Usage Examples

```
Reference @Git recent commits to write test code for changed parts
Check @Git history to learn how to rollback to previous version
```

#### Advantages

- Utilizes code change history
- Understanding other developers' changes during collaboration

---

### 6. **@Past Chats** - Previous Conversation Reference

#### Usage

```
@Past Chats
```

#### When to Use

- When continuing context from previous conversations
- When reusing past solutions
- When maintaining consistent development direction

#### Usage Examples

```
Continue implementing the authentication system discussed in @Past Chats
Create API based on database schema designed in previous conversation
```

#### Advantages

- Maintains conversation continuity
- Utilizes previous decisions

---

### 7. **@Cursor Rules** - Cursor Rules Reference

#### Usage

```
@Cursor Rules
```

#### When to Use

- When applying project coding conventions
- When maintaining consistent code style
- When writing code following team rules

#### Usage Examples

```
Write a new component following @Cursor Rules
Refactor this function according to project rules
```

#### Advantages

- Maintains consistent code style
- Automatically applies team conventions

---

### 8. **@Web** - Web Search Reference

#### Usage

```
@Web React 18 new features
@Web TypeScript 5.0 changes
@Web Next.js latest updates
```

#### When to Use

- When latest information is needed
- When checking new technologies or updates
- When real-time information is required

#### Usage Examples

```
Create routing example using @Web Next.js 14 App Router
Improve this component by applying @Web latest React performance optimization techniques
```

#### Advantages

- Utilizes latest information
- Reflects real-time technology trends

#### Disadvantages

- Requires internet connection
- Need to verify accuracy of search results

---

### 9. **@Link** - Link Reference

#### Usage

```
@Link (paste URL)
```

#### When to Use

- When referencing specific web pages or documents
- When writing code based on external resources
- When referencing API documentation or guides

#### Usage Examples

```
Reference @Link https://api.example.com/docs to write client code for this API documentation
```

#### Advantages

- Accurate external resource reference
- Utilizes specific documents or guides

---

### 10. **@Recent Changes** - Recent Changes Reference

#### Usage

```
@Recent Changes
```

#### When to Use

- When working based on recent changes
- When working on code related to changes
- When doing code reviews or testing

#### Usage Examples

```
Reference @Recent Changes to write unit tests for changed parts
Check if recent changes affect other parts
```

#### Advantages

- Immediately reflects latest changes
- Analyzes impact of changes

---

### 11. **@Linter Errors** - Linter Error Reference (Chat Only)

#### Usage

```
@Linter Errors
```

#### When to Use

- When fixing linter errors
- When improving code quality
- When adhering to style guides

#### Usage Examples

```
Reference @Linter Errors to fix all errors
Write code to resolve linter warnings
```

#### Advantages

- Automatic error correction
- Improves code quality

---

## 🎯 Effective @ Symbol Usage Strategies

### 1. **Context Combination**

```
Reference @package.json @src/config/ @Web "Node.js environment configuration best practices"
to create production environment settings
```

### 2. **Step-by-Step Approach**

1. First check related files with `@Files`
2. Reference specific functions or classes with `@Code`
3. Check official documentation with `@Docs`
4. Supplement with latest information using `@Web`

### 3. **Project Phase Usage**

- **Initial Setup**: `@package.json`, `@Docs`, `@Web`
- **During Development**: `@Code`, `@Files`, `@Cursor Rules`
- **Debugging**: `@Linter Errors`, `@Recent Changes`, `@Git`
- **Refactoring**: `@Past Chats`, `@Code`, `@Folders`

## 💡 Usage Tips

### 1. **Provide Specific Context**

❌ Bad Example: `@utils`
✅ Good Example: `Reference the formatDate function in @utils/dateHelper.js`

### 2. **Reference Only What's Needed**

- Reference specific functions or classes rather than large files
- Select related files rather than entire folders

### 3. **Use Combinations**

```
Reference @components/Button.tsx @Cursor Rules to create
a new IconButton component
```

### 4. **Utilize Real-time Information**

```
Reference @Web "React 18 Suspense usage" to create
a component that handles loading states
```

## 🚀 Advanced Use Cases

### 1. **Complete Feature Development**

```
Reference @package.json @src/types/ @components/ @Web "Next.js 14 Server Actions"
to implement user authentication system
```

### 2. **Code Review and Improvement**

```
Reference @Recent Changes @Linter Errors @Cursor Rules to improve
recent changes according to code style
```

### 3. **Documentation and Testing**

```
Reference @src/api/ @Past Chats to write test code and documentation
for API endpoints
```

## 📝 Precautions

1. **Context Size Management**: Too much context can cause performance degradation.
2. **Relevance Check**: Ensure referenced context is actually related to the task.
3. **Utilize Latest Information**: Use `@Web` to reflect latest technology trends.
4. **Follow Team Rules**: Use `@Cursor Rules` to maintain consistent code style.

## 🎉 Conclusion

The @ symbol is a powerful tool for maximizing Cursor's AI capabilities. By selecting and combining appropriate @ symbols for each situation, you can achieve more accurate and efficient code development.

We recommend starting with basic `@Files` and `@Code`, then gradually learning other functions.
