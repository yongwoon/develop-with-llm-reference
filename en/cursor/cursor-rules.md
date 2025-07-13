# Cursor Rules Configuration Guide

## 🎯 .cursorrules File Overview

The `.cursorrules` file is a configuration file that helps Cursor understand your project's context and generate appropriate code.

### Basic Structure

```markdown
# .cursorrules File Location

project-root/
├── .cursorrules # Project-wide rules
├── src/
│ └── .cursorrules # Source code specific rules
└── docs/
└── .cursorrules # Documentation specific rules
```

## 📋 Basic Templates

### 1. Minimal Configuration Template

```markdown
You are an expert developer helping with this project.

## Project Context

- Language: TypeScript
- Framework: React
- Styling: CSS Modules

## Code Style

- Use functional components
- Prefer const over let
- Use descriptive variable names
```

### 2. Complete Configuration Template

```markdown
You are an expert full-stack developer with deep knowledge of TypeScript, React, and Node.js.

## Project Overview

This is a [description of your project] built with modern web technologies.

## Tech Stack

- **Frontend**: Next.js 14 (App Router), React 18, TypeScript
- **Styling**: Tailwind CSS, shadcn/ui components
- **State Management**: Zustand for client state, TanStack Query for server state
- **Backend**: Node.js, Express.js, PostgreSQL
- **Database**: Prisma ORM
- **Authentication**: NextAuth.js
- **Testing**: Jest, React Testing Library, Playwright
- **Build**: Turbo for monorepo management

## File Structure
```

src/
├── app/ # Next.js App Router pages
├── components/ # Reusable UI components
│ ├── ui/ # Base UI components (shadcn/ui)
│ └── features/ # Feature-specific components
├── hooks/ # Custom React hooks
├── lib/ # Utility libraries and configurations
├── types/ # TypeScript type definitions
├── utils/ # Helper functions
└── styles/ # Global styles and Tailwind config

```

## Coding Standards

### TypeScript
- Use strict mode (`"strict": true`)
- Prefer interfaces over types for object shapes
- Use utility types (Pick, Omit, Partial) when appropriate
- Always define return types for functions
- Use const assertions for immutable data

### React
- Use functional components with hooks
- Implement proper error boundaries
- Use React.memo for performance optimization when needed
- Prefer custom hooks for complex logic
- Use proper key props for lists

### Code Style
- Use descriptive variable and function names
- Follow consistent naming conventions:
  - camelCase for variables and functions
  - PascalCase for components and types
  - UPPER_CASE for constants
- Add JSDoc comments for public APIs
- Keep functions small and focused (max 20 lines)
- Use early returns to reduce nesting

### File Naming
- Components: PascalCase (e.g., `UserProfile.tsx`)
- Hooks: camelCase starting with 'use' (e.g., `useAuth.ts`)
- Utilities: camelCase (e.g., `formatDate.ts`)
- Types: PascalCase (e.g., `UserTypes.ts`)

## Development Practices

### Error Handling
- Use proper error boundaries in React
- Implement graceful error handling in async operations
- Use Result pattern for functions that can fail
- Always handle loading and error states in components

### Performance
- Use React.memo for expensive re-renders
- Implement proper key props for lists
- Use useCallback and useMemo appropriately
- Lazy load components and routes when possible

### Testing
- Write unit tests for utility functions
- Write integration tests for API endpoints
- Write component tests for complex UI logic
- Follow AAA pattern (Arrange, Act, Assert)

### Security
- Validate all user inputs
- Use environment variables for sensitive data
- Implement proper CORS configuration
- Use HTTPS in production

## API Design
- Use RESTful conventions
- Implement proper HTTP status codes
- Use consistent response formats
- Include proper error messages
- Implement rate limiting

## Database
- Use Prisma schema for type safety
- Implement proper indexing
- Use transactions for related operations
- Follow naming conventions for tables and columns

## Deployment
- Use environment-specific configurations
- Implement proper logging
- Use CI/CD pipelines
- Monitor application performance

## Code Generation Guidelines
When generating code, please:
1. Follow the established patterns in the codebase
2. Include proper TypeScript types
3. Add error handling where appropriate
4. Include relevant tests
5. Follow the project's naming conventions
6. Use existing utility functions when possible
7. Ensure accessibility compliance (WCAG 2.1)
8. Include proper documentation
```

## 🔧 Project Type Templates

### React + TypeScript Project

````markdown
You are an expert React and TypeScript developer.

## Project Context

- Framework: React 18 with TypeScript
- Build Tool: Vite
- Styling: Styled Components
- State Management: React Query + Zustand
- Testing: Jest + React Testing Library

## Code Preferences

- Use functional components exclusively
- Prefer custom hooks for stateful logic
- Use proper TypeScript generics
- Implement proper error boundaries
- Follow React best practices

## Component Structure

```typescript
// Preferred component structure
interface ComponentProps {
  // Props definition
}

export function Component({ prop1, prop2 }: ComponentProps) {
  // Hooks
  // Handler functions
  // Render logic
}
```
````

## Naming Conventions

- Components: PascalCase
- Hooks: camelCase with 'use' prefix
- Constants: UPPER_CASE
- Types/Interfaces: PascalCase

````

### Node.js + Express Project

```markdown
You are an expert Node.js and Express developer.

## Project Context
- Runtime: Node.js 18+
- Framework: Express.js
- Database: PostgreSQL with Prisma
- Authentication: JWT
- Testing: Jest + Supertest

## Code Style
- Use ES6+ features
- Prefer async/await over promises
- Use proper error handling middleware
- Implement input validation
- Follow RESTful API design

## Error Handling
- Use custom error classes
- Implement global error handler
- Return consistent error responses
- Log errors appropriately

## Security
- Validate all inputs
- Use helmet for security headers
- Implement rate limiting
- Use CORS appropriately
````

### Next.js Project

```markdown
You are an expert Next.js developer.

## Project Context

- Framework: Next.js 14 with App Router
- Language: TypeScript
- Styling: Tailwind CSS
- Database: PostgreSQL with Prisma
- Authentication: NextAuth.js

## Next.js Specific

- Use App Router conventions
- Implement proper loading.tsx and error.tsx
- Use Server Components by default
- Add 'use client' only when necessary
- Follow Next.js performance best practices

## File Structure
```

app/
├── (auth)/ # Route groups
├── api/ # API routes
├── globals.css # Global styles
├── layout.tsx # Root layout
└── page.tsx # Home page

```

## SEO & Performance
- Implement proper metadata
- Use Next.js Image component
- Optimize fonts and assets
- Implement proper caching strategies
```

## 🎨 Advanced Configuration Examples

### 1. Internationalization Project

````markdown
## Internationalization

- Use react-i18next for translations
- Store translations in `/locales` directory
- Support languages: en, ko, ja
- Use proper locale routing

## Translation Keys

- Use nested keys for organization
- Follow format: `namespace.section.key`
- Use interpolation for dynamic content
- Implement proper pluralization

Example:

```typescript
// translations/en.json
{
  "auth": {
    "login": {
      "title": "Sign In",
      "email": "Email Address",
      "password": "Password"
    }
  }
}
```
````

## Accessibility

- Use semantic HTML elements
- Implement proper ARIA labels
- Support keyboard navigation
- Test with screen readers

````

### 2. E-commerce Project

```markdown
## E-commerce Specific
- Implement proper product catalog structure
- Use optimistic updates for cart operations
- Implement proper inventory management
- Follow PCI DSS compliance for payments

## Product Data Structure
```typescript
interface Product {
  id: string;
  name: string;
  price: number;
  currency: string;
  inventory: number;
  categories: Category[];
  variants: ProductVariant[];
}
````

## Payment Integration

- Use Stripe for payment processing
- Implement proper error handling for payments
- Store minimal payment information
- Use webhooks for payment confirmation

````

### 3. Dashboard Project

```markdown
## Dashboard Specific
- Implement proper data visualization
- Use Chart.js or D3.js for charts
- Implement real-time updates with WebSocket
- Use proper caching for dashboard data

## Chart Components
- Create reusable chart components
- Support different chart types (line, bar, pie)
- Implement proper responsive design
- Add accessibility for charts

## Performance
- Implement virtual scrolling for large datasets
- Use proper pagination
- Implement data caching strategies
- Optimize chart rendering
````

## 📊 Rule Writing Best Practices

### 1. Specific and Clear Guidelines

```markdown
# ❌ Vague rule

"Write good code"

# ✅ Specific rule

"Use descriptive variable names with minimum 3 characters.
Avoid abbreviations except for commonly known ones (id, url, api).
Use camelCase for variables and functions."
```

### 2. Include Example Code

````markdown
## Error Handling Pattern

Always use this pattern for async operations:

```typescript
try {
  const result = await apiCall();
  return { success: true, data: result };
} catch (error) {
  console.error("API call failed:", error);
  return { success: false, error: error.message };
}
```
````

````

### 3. Explain Project Context

```markdown
## Business Context
This is a healthcare management system that handles sensitive patient data.

## Compliance Requirements
- HIPAA compliance for patient data
- Audit logging for all data access
- Data encryption at rest and in transit
- Role-based access control
````

## 🔄 Rule Update Management

### 1. Version Control

```markdown
# .cursorrules

# Version: 2.1

# Last Updated: 2024-03-15

# Author: Development Team

## Version History

- v2.1: Added TypeScript strict mode requirements
- v2.0: Updated to Next.js 14 App Router
- v1.0: Initial rules setup
```

### 2. Team Collaboration

```markdown
## Team Conventions

- Code reviews required for all changes
- Follow conventional commits format
- Use linear history (rebase preferred)
- Maximum PR size: 400 lines

## Branch Naming

- Feature: `feature/user-authentication`
- Bug fix: `fix/login-validation-error`
- Hotfix: `hotfix/critical-security-patch`
```

## ✅ Rule Validation Checklist

Items to verify when writing new `.cursorrules` files:

### Basic Information

- [ ] Project overview and purpose description
- [ ] Technology stack specification
- [ ] File structure definition
- [ ] Development environment setup

### Coding Style

- [ ] Language-specific coding conventions
- [ ] Naming rules
- [ ] File structure and organization
- [ ] Comment and documentation rules

### Quality Assurance

- [ ] Test writing guidelines
- [ ] Error handling patterns
- [ ] Performance optimization rules
- [ ] Security considerations

### Project Specific

- [ ] Business logic rules
- [ ] External service integration methods
- [ ] Database usage rules
- [ ] Deployment and operation guide

---

Next: [Claude Code vs Cursor Comparison](./comparison.md) →
