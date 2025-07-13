# Task Unit Guide

## 📏 Task Size Definition

### Level 1: Single Function/Component (30 minutes-1 hour)

#### Utility Functions

```javascript
// Email validation function
"Create a function that validates email format:
- Accept email string as parameter
- Return true/false
- Handle edge cases (empty string, null)
- Follow RFC 5322 standard"

// Date formatting function
"Create a date formatting utility:
- Input: Date object or timestamp
- Output: 'YYYY-MM-DD' format
- Handle timezone considerations
- Include unit tests"
```

#### Single React Component

```javascript
// Button component
"Create a Button component:
- Props: label, onClick, variant (primary/secondary/danger)
- Loading state support
- Disabled state
- Tailwind CSS styling
- TypeScript props interface"

// Card component
"Create a Card component:
- Header, body, footer slots
- Optional shadow and border
- Responsive padding
- Click handler support"
```

#### Single API Endpoint

```javascript
// User lookup
"Create GET /api/users/:id endpoint:
- Fetch user by ID from database
- Return 404 if not found
- Include related data (profile)
- Add response caching headers"

// Health check
"Create health check endpoint:
- Check database connection
- Check external service availability
- Return status and response time
- Format: { status: 'ok', services: {...} }"
```

### Level 2: Feature Module (2-4 hours)

#### Authentication Module

```javascript
// Complete authentication module
"Create authentication module with:
- login(email, password) - returns token
- logout() - clears session
- isAuthenticated() - checks current status
- refreshToken() - renews expired token
- Store token securely (httpOnly cookie)
- Handle token expiration"

// User session management
"Implement session management:
- Create session on login
- Session timeout after 30 min inactivity
- Refresh session on activity
- Multiple device session tracking
- Session revocation functionality"
```

#### Form System

```javascript
// Form component set
"Create form component system:
- FormInput with validation display
- FormSelect with search capability
- FormTextarea with character count
- FormError component
- Form wrapper with validation logic
- Integrate with React Hook Form"

// Validation system
"Build validation system:
- Email, phone, URL validators
- Custom validation rules
- Async validation support
- Error message localization
- Validation schema builder"
```

#### Data Table

```javascript
// Table component
"Create DataTable component:
- Column configuration
- Sorting functionality
- Pagination controls
- Row selection
- Search/filter capability
- Export to CSV feature"
```

### Level 3: Complete Feature (1-2 days)

#### User Management System

```javascript
// Full CRUD implementation
"Implement complete user management:
Frontend:
- User list page with search and filters
- User detail modal
- Add/Edit user form with validation
- Bulk operations (delete, export)
- Role assignment UI

Backend:
- GET /api/users (paginated)
- GET /api/users/:id
- POST /api/users
- PUT /api/users/:id
- DELETE /api/users/:id
- Batch operations endpoint

Include error handling and loading states"
```

#### File Upload System

```javascript
// Complete file upload
"Create file upload system:
- Drag & drop interface
- Multiple file selection
- Progress indicators
- File type validation
- Size restrictions (max 10MB)
- Image preview generation
- S3 integration for storage
- Database record creation
- Cleanup for failed uploads"
```

#### Notification System

```javascript
// Real-time notifications
"Build notification system:
- Real-time notifications via WebSocket
- Notification types (info, warning, error)
- Persistent notification storage
- Mark as read functionality
- Notification preferences
- Email notification option
- Push notification support
- Notification history page"
```

## 🎯 Story Point Allocation Guide

### 1 Point (2-4 hours)

```markdown
Characteristics:

- Single responsibility
- Clear input/output
- Minimal external dependencies
- Few edge cases

Examples:

- "Add loading spinner to button"
- "Create formatCurrency utility"
- "Add validation to email field"
- "Update color scheme in header"
```

### 2 Points (4-8 hours)

```markdown
Characteristics:

- 2-3 component integration
- Basic state management
- API connection included
- Standard error handling

Examples:

- "Create login form with API integration"
- "Add sorting to data table"
- "Implement search functionality"
- "Create user profile card"
```

### 3 Points (1-2 days)

```markdown
Characteristics:

- Complete feature unit
- Frontend + Backend
- Complex business logic
- Various error scenarios

Examples:

- "User registration flow"
- "Shopping cart functionality"
- "Comment system with replies"
- "Dashboard with multiple widgets"
```

### 5 Points (2-3 days)

```markdown
Characteristics:

- System integration
- Complex state management
- Performance optimization needed
- Extensive testing required

Examples:

- "Payment gateway integration"
- "Real-time collaboration feature"
- "Advanced search with filters"
- "Report generation system"
```

### 8 Points (3-5 days)

```markdown
Characteristics:

- Architecture-level changes
- Multiple system integration
- Migration included
- High complexity

Examples:

- "Microservice extraction"
- "Database migration system"
- "Complete authentication overhaul"
- "Multi-tenant implementation"
```

## 📋 Specific Task Breakdown Examples

### E-commerce Shopping Cart Feature (5 points)

```markdown
## Main Task: Shopping Cart Implementation

### Subtask 1: Cart State Management (1 point)

"Create cart state management:

- Add/remove items
- Update quantities
- Calculate totals
- Persist to localStorage"

### Subtask 2: Cart API Endpoints (1 point)

"Create cart API:

- GET /api/cart
- POST /api/cart/items
- PUT /api/cart/items/:id
- DELETE /api/cart/items/:id"

### Subtask 3: Cart UI Components (2 points)

"Build cart components:

- CartIcon with item count
- CartDrawer slide-out panel
- CartItem component
- CartSummary with totals"

### Subtask 4: Integration & Testing (1 point)

"Complete cart integration:

- Connect UI to API
- Add optimistic updates
- Error handling
- E2E tests"
```

### Real-time Chat Feature (8 points)

```markdown
## Main Task: Real-time Chat System

### Subtask 1: WebSocket Infrastructure (2 points)

"Set up WebSocket server:

- Socket.io integration
- Connection management
- Room-based channels
- Reconnection logic"

### Subtask 2: Message Database Schema (1 point)

"Design message storage:

- Message table schema
- Indexes for performance
- Soft delete support
- Read receipts tracking"

### Subtask 3: Chat UI Components (2 points)

"Create chat interface:

- MessageList component
- MessageInput with typing indicator
- UserList sidebar
- ChatRoom container"

### Subtask 4: Real-time Features (2 points)

"Implement real-time features:

- Message delivery
- Typing indicators
- Online status
- Read receipts
- Message notifications"

### Subtask 5: History & Search (1 point)

"Add chat history features:

- Load previous messages
- Infinite scroll
- Message search
- Date separators"
```

## 🔧 Task Size Estimation Tools

### Complexity Checklist

```markdown
Task complexity assessment:

□ Technical Complexity

- [ ] New technology stack required
- [ ] Complex algorithm implementation
- [ ] Performance optimization needed
- [ ] Many security considerations

□ Integration Complexity

- [ ] External service integration
- [ ] Multiple system communication
- [ ] Data migration
- [ ] Backward compatibility maintenance

□ Business Complexity

- [ ] Complex business rules
- [ ] Many edge cases
- [ ] Regulatory compliance needed
- [ ] Multi-language support

□ UI/UX Complexity

- [ ] Complex interactions
- [ ] Responsive design
- [ ] Accessibility requirements
- [ ] Animations/transitions
```

### Task Breakdown Template

```markdown
# Feature: [Feature Name]

## Total Estimate: [X] points

### Technical Tasks

- [ ] Database schema design (X points)
- [ ] API endpoint implementation (X points)
- [ ] Business logic layer (X points)

### Frontend Tasks

- [ ] UI component development (X points)
- [ ] State management setup (X points)
- [ ] API integration (X points)

### Quality Assurance

- [ ] Unit test coverage (X points)
- [ ] Integration tests (X points)
- [ ] E2E test scenarios (X points)

### Documentation

- [ ] API documentation (X points)
- [ ] User guide (X points)
- [ ] Technical documentation (X points)
```

## 📊 Velocity Tracking

### Sprint Velocity Records

```markdown
## Team Velocity Tracking

### Sprint 1

- Committed: 21 points
- Completed: 18 points
- Carry-over: 3 points
- Notes: Authentication took longer than expected

### Sprint 2

- Committed: 20 points
- Completed: 22 points
- Carry-over: 0 points
- Notes: Team getting familiar with codebase

### Sprint 3

- Committed: 22 points
- Completed: 21 points
- Carry-over: 1 point
- Notes: Stable velocity achieved

Average Velocity: 20.3 points/sprint
```

## ✅ Task Estimation Best Practices

1. **Prevent Underestimation**

   - Include test writing time
   - Consider code review time
   - Include deployment and monitoring

2. **Secure Buffer Time**

   - Handle unexpected issues
   - Resolve technical debt
   - Documentation time

3. **Team Consensus**

   - Use Planning Poker
   - Reference historical data
   - Continuous adjustment

4. **Clear Completion Criteria**
   - Code completion
   - Tests passing
   - Documentation updated
   - PR approved

---

Next: [Specification Writing Guide](./specification-guide.md) →
