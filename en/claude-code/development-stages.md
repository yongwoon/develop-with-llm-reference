# Efficient Development Stages

## 🚀 Development Process Overview

### Stage 1: Start with Small Units

#### Basic Principles

- Don't request the entire project at once
- Start with independently testable components
- Verify at each stage before proceeding

#### Example: Building Express Server

```bash
# Bad example
"Create a complete e-commerce backend with user management,
product catalog, order processing, and payment integration"

# Good example - Step-by-step approach
Step 1: "Create a basic Express server with a health check endpoint"
Step 2: "Add middleware for CORS, body parsing, and error handling"
Step 3: "Implement user registration endpoint with validation"
Step 4: "Add JWT authentication middleware"
```

### Stage 2: Incremental Feature Addition

#### Building on Existing Codebase

```bash
# Request with context provided
"Given the existing Express server in app.js,
add a user authentication middleware that:
- Validates JWT tokens
- Attaches user info to req.user
- Returns 401 for invalid tokens"
```

#### Include Integration Testing

```bash
"Add unit tests for the authentication middleware
using Jest and supertest, covering:
- Valid token scenarios
- Expired token handling
- Malformed token handling"
```

### Stage 3: Provide Context

#### Explain Project Structure

```bash
"Project structure:
- src/models/User.js contains Mongoose user schema
- src/middleware/ for all middleware functions
- Using ES6 modules (import/export)

Create a user controller with CRUD operations
following this structure and coding style"
```

### Stage 4: Test-Driven Development

```bash
# Request test writing first
"Write Jest tests for a UserService class that should:
- Create new users with hashed passwords
- Validate unique email addresses
- Handle database errors gracefully

Then implement the UserService to pass these tests"
```

## 📝 Effective Prompt Writing

### 1. Specific Requirements

#### ❌ Bad Examples

```
"Make a login page"
"Add authentication"
"Create a dashboard"
```

#### ✅ Good Examples

```
"Create a React login component with:
- Email and password input fields
- Client-side validation (email format, password minimum 8 chars)
- Loading state during submission
- Error message display
- Submit handler that posts to /api/auth/login
- Redirect to /dashboard on success
Using Tailwind CSS for styling and React Hook Form for form handling"
```

### 2. Specify Technical Constraints

```bash
"Implement the password reset feature:
- Use TypeScript with strict mode
- Follow existing ESLint configuration
- Compatible with Node.js 18+
- Use Prisma ORM for database operations
- Include JSDoc comments for all public methods
- Handle errors using the existing error middleware pattern"
```

### 3. Describe Expected Results

```bash
"Create a data fetching hook that:
- Returns { data, error, isLoading } object
- Handles race conditions with cleanup
- Implements exponential backoff for retries
- Caches results for 5 minutes
- TypeScript generic for type safety

Example usage:
const { data, error, isLoading } = useAPI<User[]>('/api/users')"
```

## 🔄 Iterative Improvement Process

### Initial Implementation → Refactoring → Optimization

#### Phase 1: Working Code

```bash
"Create a function that fetches user data from the API"
```

#### Phase 2: Add Error Handling

```bash
"Add error handling to the user fetching function:
- Network errors
- 404 responses
- Timeout after 10 seconds"
```

#### Phase 3: Performance Optimization

```bash
"Optimize the user fetching function:
- Add caching with 5-minute TTL
- Implement request deduplication
- Add loading and error states"
```

#### Phase 4: Type Safety

```bash
"Add TypeScript types to the user fetching function:
- Generic type for response data
- Proper error types
- Type guards for runtime validation"
```

## 🏗 Real Workflow Example

### Full-Stack Feature Implementation (User Profile)

#### Step 1: Data Model

```bash
"Create a Prisma schema for user profiles with:
- Basic info (name, bio, avatar)
- Social links (optional)
- Privacy settings
- Timestamps (createdAt, updatedAt)"
```

#### Step 2: API Endpoints

```bash
"Create Express routes for user profile:
GET /api/profile/:userId - Public profile view
GET /api/profile - Get own profile (authenticated)
PUT /api/profile - Update own profile
Include validation middleware and error handling"
```

#### Step 3: Frontend Components

```bash
"Create a ProfileForm React component:
- Form fields matching the profile schema
- Image upload for avatar
- Real-time validation
- Optimistic updates
- Success/error notifications"
```

#### Step 4: Integration and Testing

```bash
"Create integration tests for the profile feature:
- Test complete flow from form submission to database
- Test validation errors
- Test authorization (can only edit own profile)
- Test image upload handling"
```

## 🛡 Code Quality Management

### 1. Code Review Requests

```bash
"Review this authentication middleware for:
- Security vulnerabilities
- Performance issues
- Error handling completeness
- Code style consistency
Suggest improvements with explanations"
```

### 2. Refactoring Requests

```bash
"Refactor this component to:
- Extract business logic to custom hooks
- Improve type safety
- Reduce cognitive complexity
- Follow SOLID principles
Maintain all existing functionality"
```

### 3. Performance Optimization

```bash
"Optimize this React component for performance:
- Identify unnecessary re-renders
- Implement proper memoization
- Lazy load heavy dependencies
- Optimize bundle size
Provide before/after comparison"
```

## 📊 Progress Tracking

### Git Commit Strategy

```bash
# Feature branch
git checkout -b feature/user-authentication

# Meaningful commit messages
git commit -m "feat: add JWT authentication middleware"
git commit -m "test: add auth middleware unit tests"
git commit -m "docs: update API documentation for auth endpoints"
```

### Documentation Requests

```bash
"Add comprehensive documentation:
- JSDoc comments for all functions
- README with setup instructions
- API endpoint documentation
- Architecture decision records (ADRs)"
```

## ✅ Development Stage Checklist

Checklist for each feature implementation:

- [ ] Requirements clearly defined
- [ ] Work broken down into small units
- [ ] Tests written for each stage
- [ ] Code review performed
- [ ] Documentation completed
- [ ] Performance optimization reviewed
- [ ] Security vulnerabilities checked
- [ ] Error handling verified

---

Next: [Agile Development Strategy](./agile-strategy.md) →
