# Claude Memory Tips

20년 넘은 숙련된 풀스택 웹개발자로서 Claude Code를 효과적으로 사용하기 위한 메모리 구성을 제안드리겠습니다.

## 사용자 메모리 (`~/.claude/CLAUDE.md`)

_모든 프로젝트에 공통적으로 적용되는 개인 환경 설정_

### 코딩 스타일 및 선호도

- 2칸 들여쓰기 사용
- 세미콜론 항상 사용
- 함수형 프로그래밍 스타일 선호 (map, filter, reduce 등)
- async/await 사용 (Promise.then 대신)
- TypeScript 사용 선호
- ESLint와 Prettier 설정 적용

### 개인 도구 및 워크플로우

- VS Code 에디터 사용
- Git 커밋 메시지 컨벤션 (feat:, fix:, docs: 등)
- 단축키 및 스니펫 선호도
- 테스트 도구 선호도 (Jest, Vitest, Cypress 등)
- 패키지 매니저 선호도 (npm, yarn, pnpm)

### 아키텍처 및 설계 원칙

- 컴포넌트 기반 아키텍처
- 단일 책임 원칙 준수
- 의존성 주입 패턴
- 에러 핸들링 방식
- 로깅 및 모니터링 접근법

### Example

```txt
# User Memory - Personal Development Environment Settings

## Coding Style and Preferences

### Basic Formatting
- Use 2-space indentation (spaces instead of tabs)
- Always use semicolons
- Prefer single quotes ('string' format)
- Use trailing commas in objects and arrays
- 80-character line length limit

### JavaScript/TypeScript Style
- Prefer functional programming style (map, filter, reduce, etc.)
- Use async/await (instead of Promise.then)
- Prefer TypeScript (prohibit any type)
- Prefer arrow functions (but use function keyword for methods)
- Actively use destructuring assignment

### React Component Style
- Use functional components (prohibit class components)
- Actively use custom hooks
- Use TypeScript interfaces instead of PropTypes
- Component file names in PascalCase

## Personal Tools and Workflow

### Editor and Extensions
- Use VS Code editor
- Prettier, ESLint automatic formatting setup
- Use Auto Import extension
- Use GitLens extension

### Git Commit Convention
- feat: Add new feature
- fix: Bug fix
- docs: Documentation update
- style: Code formatting
- refactor: Code refactoring
- test: Add/modify test code
- chore: Build process or auxiliary tool modifications

### Package Manager
- Prefer pnpm (instead of npm, yarn)
- Standardize package.json scripts commands
- Regularly update dependencies

### Testing Tools
- Prefer Jest + Testing Library combination
- Use Vitest (for Vite projects)
- Use Playwright for E2E testing
- Maintain 80%+ test coverage

## Architecture and Design Principles

### Component Design
- Follow single responsibility principle
- Write reusable components
- Prevent props drilling (use Context API or state management library)
- Limit components to maximum 200 lines

### State Management
- Use useState for local state
- Prefer Zustand for global state
- Use React Query/TanStack Query for server state
- Use React Hook Form for form state

### Error Handling
- Actively use try-catch blocks
- Implement error boundary components
- Provide user-friendly error messages
- Build error logging system

### Performance Optimization
- Appropriate use of React.memo
- Use useMemo, useCallback only when necessary
- Apply code splitting (React.lazy)
- Image optimization (use Next.js Image component)

## Development Environment Setup

### Environment Variable Management
- Use .env.local file
- Separate settings by environment (.env.development, .env.production)
- Never commit sensitive information

### Debugging Tools
- Use React Developer Tools
- Actively use Chrome DevTools
- Prefer debugger over console.log
- Use performance profiling tools

### Development Server Setup
- Enable hot reloading
- Resolve CORS issues with proxy settings
- Use HTTPS in development environment (utilize mkcert)

## Documentation and Communication

### Code Comments
- Use JSDoc format comments
- Add explanations for complex logic
- Use TODO, FIXME comments

### Document Writing
- Write detailed README.md files
- Use OpenAPI/Swagger for API documentation
- Write component Storybook documentation
```

## Project Memory (`./CLAUDE.md`)

_Team shared guidelines for specific projects_

### Project Architecture

- Project structure and folder organization
- Main technology stack (React, Next.js, Express, etc.)
- Database design and connection methods
- API design principles (RESTful, GraphQL, etc.)
- State management approaches (Redux, Zustand, Context API, etc.)

### Coding Standards

- Naming conventions (variables, functions, classes, file names)
- Component writing rules
- Type definition methods
- Error handling and exception responses
- Code review checklist

### Development Environment Setup

- Environment variable management
- Build and deployment configuration
- Test environment setup
- Local development server configuration
- Docker container setup

### External Service Integration

- Authentication/authorization systems
- Payment systems
- Email services
- Cloud storage
- Third-party API integration methods

### Workflow and Deployment

- Git branching strategy
- CI/CD pipeline
- Deployment environments (development, staging, production)
- Monitoring and alert setup
- Backup and recovery procedures

### Documentation and Communication

- API documentation writing methods
- Code comment guidelines
- Change log management
- Team communication rules

### Example

```txt
# Project Memory - E-Commerce Web Application

## Project Overview
- **Project Name**: ShopMate E-commerce Platform
- **Tech Stack**: Next.js 14, TypeScript, Tailwind CSS, Prisma, PostgreSQL
- **Deployment Environment**: Vercel (Frontend), Railway (Database)
- **Team Composition**: 3 members (2 Frontend, 1 Backend)

## Project Architecture

### Folder Structure
"""
├── src/
│   ├── app/                 # Next.js 13+ App Router
│   ├── components/          # Reusable components
│   │   ├── ui/             # Basic UI components
│   │   ├── forms/          # Form-related components
│   │   └── layout/         # Layout components
│   ├── lib/                # Utility functions and configurations
│   ├── hooks/              # Custom hooks
│   ├── types/              # TypeScript type definitions
│   └── store/              # State management (Zustand)
├── prisma/                 # Database schema
├── public/                 # Static files
└── tests/                  # Test files
"""

### Technology Stack Details
- **Frontend**: Next.js 14 (App Router), React 18, TypeScript 5.0
- **Styling**: Tailwind CSS 3.3, Headless UI, Radix UI
- **State Management**: Zustand (global state), React Query (server state)
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js with Google, GitHub providers
- **Payment**: Stripe Integration
- **Testing**: Jest, React Testing Library, Playwright

## Coding Standards

### Naming Convention
- **Components**: PascalCase (`UserProfile.tsx`)
- **Functions/Variables**: camelCase (`getUserData`)
- **Constants**: UPPER_SNAKE_CASE (`API_BASE_URL`)
- **File Names**: kebab-case (`user-profile.tsx`) or PascalCase (components)
- **API Endpoints**: kebab-case (`/api/user-profile`)

### Component Writing Rules
- Maximum 200 lines limit (split if exceeded)
- Props interface definition required
- Set default props values
- Apply error boundaries
- Consider accessibility (ARIA attributes, keyboard navigation)

### TypeScript Rules
- Prohibit `any` type usage
- Define types for all API responses
- Actively use union types
- Utilize generic types (improve reusability)

## API Design Principles

### RESTful API Rules
- **GET** `/api/products` - Retrieve product list
- **GET** `/api/products/[id]` - Retrieve specific product
- **POST** `/api/products` - Create product
- **PUT** `/api/products/[id]` - Full product update
- **PATCH** `/api/products/[id]` - Partial product update
- **DELETE** `/api/products/[id]` - Delete product

### Response Format Standardization
"""typescript
interface ApiResponse<T> {
  success: boolean;
  data?: T;
  error?: string;
  message?: string;
}
"""

### Error Handling
- Appropriate use of HTTP status codes
- Consistent error message format
- Provide detailed error information in development environment
- Hide sensitive information in production environment

## Database Design

### Main Tables
- **User**: User information
- **Product**: Product information
- **Category**: Product categories
- **Order**: Order information
- **OrderItem**: Order product details
- **Cart**: Shopping cart
- **Review**: Product reviews

### Prisma Schema Rules
- Include `id`, `createdAt`, `updatedAt` fields in all models
- Specify cascade options when setting relationships
- Set appropriate indexes
- Implement soft delete (`deletedAt` field usage)

## State Management

### Zustand Store Structure
"""
├── store/
│   ├── auth-store.ts       # User authentication state
│   ├── cart-store.ts       # Shopping cart state
│   ├── product-store.ts    # Product filtering state
│   └── ui-store.ts         # UI state (modal, loading, etc.)
"""

### React Query Usage Rules
- Dedicated to server state management
- Standardize query keys (`['products', 'list', filters]`)
- Set appropriate caching time
- Apply optimistic updates

## Styling Guide

### Tailwind CSS Usage Rules
- Prioritize utility classes
- Minimize custom CSS
- Conditional className application for component variants
- Support dark mode (use `dark:` prefix)

### Component Styling
- Place basic components in `components/ui/` directory
- Separate business logic and styling
- Define reusable style patterns

## Authentication and Authorization

### NextAuth.js Setup
- Use Google, GitHub OAuth providers
- Use JWT tokens
- Session management and automatic renewal
- Role-based access control (RBAC)

### Security Rules
- Apply authentication middleware to all API endpoints
- Use CSRF tokens
- Prevent XSS attacks (input validation and escaping)
- Manage sensitive information with environment variables

## Payment System

### Stripe Integration
- Secure payment information processing
- Payment status synchronization through webhooks
- Refund and cancellation processing logic
- Retry mechanism for payment failures

## Testing Strategy

### Unit Testing
- Test all utility functions
- Component rendering tests
- API endpoint tests
- Maintain minimum 80% code coverage

### Integration Testing
- User flow testing
- API integration testing
- Database connection testing

### E2E Testing
- Main user scenario testing
- Payment flow testing
- Cross-browser testing

## Deployment and DevOps

### Deployment Strategy
- **Development**: Vercel Preview deployment
- **Staging**: Separate Vercel project
- **Production**: Main domain deployment

### CI/CD Pipeline
- Use GitHub Actions
- Automatic test execution
- Code quality checks (ESLint, Prettier)
- Automatic deployment (when tests pass)

### Monitoring
- Use Vercel Analytics
- Error tracking (Sentry integration)
- Performance monitoring (Web Vitals)

## Environment Configuration

### Environment Variables
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

### Development Environment Setup
- Use Node.js 18.x or higher
- Use pnpm package manager
- Provide recommended VS Code extensions list
- Development server port: use 3000

## Documentation Rules

### README.md Required Contents
- Project description and features
- Installation and execution methods
- Environment variable setup guide
- Deployment methods
- Contribution guidelines

### Code Documentation
- Comments required for complex business logic
- Write JSDoc for API endpoints
- Document component PropTypes
- Add database schema descriptions
```
