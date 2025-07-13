# Agile Development Strategy

## 🌊 Managing Uncertainty

### User Story-Based Approach

#### Value-Centered Instead of Technical Specifications

```bash
# Technical-centered approach (avoid)
"Create a PostgreSQL table with user fields and indexes"

# User Story-centered approach (recommended)
"As a user, I want to create an account
so that I can save my preferences and order history

Acceptance Criteria:
- User can sign up with email/password
- Email verification is required
- Profile is created automatically after signup"
```

#### Request Solution Suggestions from Claude

```bash
"Given this user story: [User Story content]
Suggest:
1. Technical implementation approach
2. Required components
3. Potential challenges
4. MVP vs full feature comparison"
```

### MVP (Minimum Viable Product) First

#### Step-by-Step Feature Expansion

```markdown
## Sprint 1: Basic Authentication (MVP)

"Create simple email/password login:

- No social login
- Basic session management
- Simple error messages"

## Sprint 2: Enhanced Security

"Add to existing auth:

- Password strength requirements
- Account lockout after failed attempts
- Session timeout"

## Sprint 3: User Experience

"Enhance auth flow:

- Social login options
- Remember me functionality
- Password reset flow"
```

### Exploratory Prototyping

```bash
# Exploring uncertain requirements
"Create 3 different UI prototypes for the dashboard:
1. Card-based layout with summary metrics
2. Table-focused design for data analysis
3. Visual charts and graphs approach

Each should handle the same data but present differently"

# Exploring technical approaches
"Implement user notifications using 3 approaches:
1. WebSocket implementation
2. Server-Sent Events
3. Polling mechanism

Include pros/cons and resource usage for each"
```

## 📅 Sprint Planning and Execution

### Sprint 0: Discovery & Setup

```markdown
## Week 1: Discovery Sprint

### Day 1-2: Technical Validation

"Create proof of concepts for:

- Authentication flow with NextAuth
- Database connection with Prisma
- Real-time updates with Socket.io"

### Day 3-4: UI/UX Exploration

"Create wireframes for main user flows:

- Onboarding process
- Main dashboard
- Key feature interactions"

### Day 5: Architecture Decisions

"Based on POCs, create:

- System architecture diagram
- Technology stack decision document
- Development environment setup guide"
```

### Sprint 1-2: Core Feature Implementation

```markdown
## Sprint 1: Foundation (Week 2-3)

### User Authentication Epic

Day 1-3: "Implement basic auth:

- Registration with email verification
- Login/logout functionality
- Protected route wrapper"

Day 4-5: "Add user profile:

- Profile creation after registration
- Basic profile edit functionality
- Avatar upload"

### Sprint Review & Planning

"Create demo for:

- User registration flow
- Login and access protected area
- Basic profile management"
```

### Daily Standup Utilization

```bash
# Yesterday's Work
"Implemented user registration API endpoint
Blocker: Email service configuration"

# Today's Plan - Claude Request
"Help me implement email service:
- Use SendGrid API
- Template for verification emails
- Queue system for reliability
- Error handling and retry logic"

# Impediments Resolution
"The email service is failing with rate limit errors
Suggest solutions for:
- Implementing queue with Bull
- Rate limiting strategy
- Fallback email provider"
```

## 🔄 Iterative Improvement Strategy

### Incremental Feature Enhancement

```markdown
## Task List Feature Evolution

### Iteration 1: Basic Functionality

"Create a simple task list component:

- Add new tasks
- Display task list
- Delete tasks"

### Iteration 2: Task Status

"Enhance task list with:

- Checkbox to mark complete
- Visual distinction for completed tasks
- Task count summary"

### Iteration 3: Task Organization

"Add task management features:

- Priority levels (High, Medium, Low)
- Due dates
- Category tags"

### Iteration 4: Advanced Features

"Implement productivity features:

- Drag-and-drop reordering
- Bulk operations
- Keyboard shortcuts
- Task templates"
```

### Spikes for Technical Exploration

```bash
# Resolving technical uncertainty
"Research spike: Implement real-time collaboration
Time-boxed to 1 day, explore:
- Operational Transformation approach
- CRDT implementation
- Simple locking mechanism

Provide recommendation with POC code"
```

## 📊 Story Points and Estimation

### Work Size Standards

```markdown
## Story Point Reference

### 1 Point - 2-4 hours

- Simple UI component
- Basic CRUD endpoint
- Utility function
- Minor bug fix

Example: "Create a LoadingSpinner component"

### 2 Points - 4-8 hours

- Complex component with state
- API endpoint with validation
- Integration between components
- Unit test suite

Example: "Implement form with validation"

### 3 Points - 1-2 days

- Complete feature slice
- Multiple integrated components
- Database schema changes
- Complex business logic

Example: "User profile management"

### 5 Points - 2-3 days

- Multi-step workflows
- Third-party integrations
- Performance optimizations
- System refactoring

Example: "Payment processing integration"

### 8 Points - 3-5 days

- Major architectural changes
- Complex features with many edge cases
- Full subsystem implementation

Example: "Real-time notification system"
```

## 🎯 Uncertainty Response Patterns

### 1. Interface-First Design

```typescript
// Define interfaces before implementation
"Define TypeScript interfaces for a user management system:
- User entity
- Repository interface
- Service layer interface
- API response types

Don't implement yet, just define contracts"
```

### 2. Mock Data Utilization

```bash
"Create mock API responses for:
- User CRUD operations
- Product catalog
- Order processing

Use realistic data that covers edge cases
Include delay simulation for loading states"
```

### 3. Feature Toggle Implementation

```bash
"Implement feature toggle system:
- Environment-based flags
- User-specific flags
- Gradual rollout capability
- Runtime toggle without deploy"
```

### 4. A/B Testing Preparation

```bash
"Set up A/B testing framework:
- User segmentation logic
- Metric tracking
- Results analysis
- Easy experiment creation"
```

## 🔍 Feedback Loop Optimization

### Rapid Prototype → Validation → Improvement

```markdown
## Rapid Prototyping Cycle

### Hour 1-2: Quick Prototype

"Create basic working version of [feature]
Focus on happy path only"

### Hour 3: User Feedback

- Demo to stakeholders
- Collect immediate feedback
- Identify missing requirements

### Hour 4-8: Iterate

"Based on feedback:

- Add error handling
- Improve UX
- Handle edge cases"
```

### Continuous Improvement Requests

```bash
# Week 1: Basic Implementation
"Create user dashboard with mock data"

# Week 2: Real Data Integration
"Connect dashboard to actual API endpoints"

# Week 3: Performance
"Optimize dashboard rendering:
- Implement virtual scrolling
- Add pagination
- Cache API responses"

# Week 4: Polish
"Add finishing touches:
- Loading skeletons
- Error boundaries
- Empty states
- Animations"
```

## ✅ Agile Practice Checklist

Sprint-by-sprint checklist:

### Sprint Planning

- [ ] Do user stories provide clear value?
- [ ] Are acceptance criteria testable?
- [ ] Have technical uncertainties been identified?
- [ ] Are spike items determined?

### Daily Execution

- [ ] Has work been broken down into small units?
- [ ] Are deployable increments created daily?
- [ ] Are blockers resolved quickly?
- [ ] Is progress shared with the team?

### Sprint Review

- [ ] Has working software been demonstrated?
- [ ] Has user feedback been collected?
- [ ] Have next priorities been adjusted?
- [ ] Are improvements documented?

---

Next: [Task Unit Guide](./task-units.md) →
