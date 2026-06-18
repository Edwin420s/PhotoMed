# PhotoMed Request Tracker

A professional request tracking web application for managing clinical software integration requests across the PhotoMed ecosystem. Built as a software engineering assessment submission, this application demonstrates modern frontend development practices with a focus on clean code, user experience, and functional completeness.

## Live Demo

[https://photomed.netlify.app/](https://photomed.netlify.app/)

## Project Overview

The Request Tracker is a fully functional single-page application that allows users to submit, manage, and track requests including bugs, feature requests, feedback, and partnership inquiries. The application features a professional dashboard interface with real-time statistics, search/filtering capabilities, and persistent data storage using browser localStorage.

This project was built as a software engineering assessment submission for PhotoMed, demonstrating problem-solving approach, code organization, attention to user experience, and ability to deliver a complete, working application.

## Features

### Core Requirements (Mandatory)
- **Request Submission Form**: Collects name, email, product, request type, priority, and message with validation
- **Dynamic Request List**: Renders all submitted requests with full details in a card-based layout
- **Status Management**: Supports New, In Review, Resolved, and Rejected statuses with dropdown controls on each request
- **Status Filtering**: Filter requests by status (All, New, In Review, Resolved, Rejected)
- **Data Persistence**: Uses localStorage to save requests across browser sessions
- **Responsive Design**: Mobile-first approach using Tailwind CSS for optimal viewing on all devices

### Bonus Features Implemented
- **Search Functionality**: Real-time search by name or email with instant filtering
- **Statistics Dashboard**: Real-time overview showing Total, New, In Review, and Resolved request counts
- **Edit Requests**: Modal-based editing with pre-filled data for all request fields
- **Delete Requests**: Delete functionality with confirmation dialog
- **Empty State Handling**: User-friendly message when no requests match current filters
- **Form Validation**: Inline error messages for required fields (replaced browser alerts)
- **Professional UI**: Clean, modern dashboard interface inspired by SaaS products like Jira, Zendesk, and Linear
- **Color-coded Status**: Visual indicators for different request statuses
- **Priority Badges**: Color-coded priority levels (High, Medium, Low)
- **Date Formatting**: Human-readable date display
- **XSS Protection**: HTML escaping to prevent cross-site scripting attacks

## Technology Stack

### Frontend
- **HTML5**: Semantic markup with proper structure and accessibility
- **Tailwind CSS**: Utility-first CSS framework (via CDN with forms and container-queries plugins)
- **Google Fonts**: Inter font family for clean, modern typography
- **Material Symbols**: Google's icon library for consistent UI icons

### JavaScript & Data
- **Vanilla JavaScript**: No frameworks, pure JavaScript for all functionality
- **localStorage API**: Client-side data persistence for request storage
- **ES6+ Features**: Modern JavaScript syntax including arrow functions, template literals, destructuring

### Deployment
- **Netlify**: Cloud hosting platform for static sites with automatic HTTPS
- **Git**: Version control for code management and deployment

## Architecture

### Application Structure
The application follows a single-file architecture with clear separation of concerns:

1. **HTML Structure**: Semantic markup with header, main content, sidebar, and footer
2. **CSS Styling**: Tailwind CSS utility classes with custom configuration for PhotoMed brand colors
3. **JavaScript Logic**: Modular functions organized by responsibility:
   - Data Model: Request array and localStorage management
   - UI Rendering: Dynamic HTML generation for requests and statistics
   - Event Handling: User interaction processing
   - State Management: Centralized state updates and UI refresh

### Data Flow
```
User Input → Form Validation → Request Object → localStorage → UI Update
User Action (Edit/Delete/Status Change) → Data Update → localStorage → UI Refresh
Search/Filter Input → Filter Logic → Filtered Data → UI Render
```

### Key Functions
- `loadInitialData()`: Loads requests from localStorage or seeds with example data
- `persistRequests()`: Saves current request state to localStorage
- `addNewRequest()`: Handles form submission and creates new requests
- `renderRequestsList()`: Dynamically generates request cards
- `renderStats()`: Updates statistics dashboard
- `getFilteredRequests()`: Applies search and filter logic
- `updateRequestStatus()`: Changes request status
- `deleteRequest()`: Removes requests with confirmation
- `openEditModal()`: Opens edit modal with pre-filled data
- `handleEditSubmit()`: Saves edited request data
- `escapeHtml()`: Security helper to prevent XSS attacks

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools or dependencies required
- Optional: Local server for development (Python, Node.js, or PHP)

### Local Development

#### Option 1: Direct File Opening (Simplest)
1. Clone or download this repository
2. Open `index.html` in any modern web browser
3. The application will work immediately with no setup required

#### Option 2: Local Server (Recommended for Development)
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

### Project Structure
```
PhotoMed/
├── index.html          # Single-file application with embedded CSS and JavaScript
├── netlify.toml        # Netlify deployment configuration
└── README.md          # This documentation file
```

The application is intentionally structured as a single HTML file for simplicity and ease of deployment, as permitted by the assessment requirements.

## Usage Guide

### Submitting a Request
1. Fill out the "Submit New Request" form on the left sidebar
2. Required fields: Full Name, Professional Email, Message
3. Optional fields: Product, Request Type, Priority
4. Click "Submit Request" to add your request to the list
5. The request will appear immediately in the main list with "New" status

### Managing Requests
1. **View Requests**: All requests appear in the main list sorted by date (newest first)
2. **Update Status**: Use the status dropdown on each request card to change status
3. **Search**: Use the search bar to find requests by name or email (real-time filtering)
4. **Filter**: Use the status filter dropdown to show specific request types
5. **Edit**: Click the edit icon (pencil) to modify request details in a modal
6. **Delete**: Click the delete icon (trash) to remove a request (with confirmation)

### Understanding Status Colors
- **New**: Blue border and badge - Requires action
- **In Review**: Orange border and badge - Under evaluation
- **Resolved**: Green border and badge - Successfully closed
- **Rejected**: Gray border and badge - Not pursued

### Priority Levels
- **High**: Red badge - Urgent attention needed
- **Medium**: Gray badge - Normal priority
- **Low**: Blue badge - Low priority

## Deployment

### Current Deployment
The application is deployed on Netlify: [https://photomed.netlify.app/](https://photomed.netlify.app/)

### Deploy Your Own Version

#### Method 1: Netlify Drag & Drop (Fastest)
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Sign up or log in
3. Drag your project folder (containing index.html) into the drop zone
4. Get your live URL instantly

#### Method 2: Netlify + GitHub (Recommended)
1. Push your code to GitHub repository
2. Log in to [Netlify](https://netlify.com)
3. Click "Add new site" → "Import an existing project"
4. Connect your GitHub repository
5. Deploy settings (no build command needed):
   - Build command: (leave empty)
   - Publish directory: `.` (root)
6. Click "Deploy site"

#### Method 3: Alternative Platforms
- **Vercel**: Similar process to Netlify
- **GitHub Pages**: Enable in repository settings
- **Cloudflare Pages**: Connect GitHub repository

## Assessment Compliance

This project meets all assessment requirements:

### Mandatory Requirements
- Request submission form with all required fields (name, email, type, priority, message)
- Request list displaying submitted details
- Status management (New, In Review, Resolved, Rejected)
- At least one working filter (status filter implemented)
- Data persistence using localStorage
- Clean, readable, and organized code
- Professional UI/UX design
- Responsive design for mobile devices

### Optional Improvements Implemented
- Search functionality (bonus)
- Statistics dashboard (bonus)
- Edit and delete capabilities (bonus)
- Improved validation UX with inline error messages (bonus)
- Professional dashboard design (bonus)

### Code Quality
- **Clean Code**: Clear function names, minimal comments where code is self-documenting
- **Separation of Concerns**: Data model, UI rendering, and event handling are separated
- **Security**: HTML escaping to prevent XSS attacks
- **Performance**: Efficient DOM updates with targeted re-rendering
- **Maintainability**: Modular functions that can be easily tested or modified

## What Was Completed

All mandatory requirements have been fully implemented:
- Request submission form with validation
- Dynamic request list displaying all submitted details
- Status management with all four required statuses
- Working status filter
- Data persistence using localStorage
- Responsive, professional UI

Additionally implemented bonus features:
- Search functionality by name and email
- Statistics dashboard with real-time metrics
- Edit and delete capabilities with confirmation dialogs
- Improved validation UX with inline error messages
- Professional dashboard design with color-coded statuses
- Empty state handling for better UX

## What Was Not Completed

No features were left incomplete. All core requirements and several optional improvements have been implemented. The application is fully functional and ready for production use.

## Challenges Faced

### 1. Initial Design Complexity
**Challenge**: Started with a complex UI that needed simplification while maintaining professional appearance.

**Solution**: Focused on core dashboard functionality and clean card-based layout, removing unnecessary elements while preserving the professional SaaS-like feel.

### 2. State Management
**Challenge**: Ensuring localStorage synchronization across all UI components (stats, list, filters).

**Solution**: Implemented a centralized `fullRefreshUI()` function that updates all components when data changes, ensuring consistency across the application.

### 3. Form Validation UX
**Challenge**: Initially used browser `alert()` which felt unprofessional and disruptive to user experience.

**Solution**: Replaced with inline error messages that appear dynamically above the form, providing immediate feedback without interrupting the user flow.

### 4. Real-time Search Performance
**Challenge**: Implementing search that updates instantly without performance issues.

**Solution**: Used efficient array filtering with debounced input handling to ensure smooth real-time search even with larger datasets.

## Future Improvements

If given more time, I would enhance the application with:

### Backend & Database
- **Database Integration**: Replace localStorage with PostgreSQL, MongoDB, or Supabase for multi-user support
- **Authentication**: Add user login and role-based access control (admin vs regular users)
- **API Development**: RESTful API for backend operations

### Advanced Features
- **Email Notifications**: Send email alerts when request status changes
- **File Attachments**: Allow users to attach screenshots or documents to requests
- **Advanced Filtering**: Add filters by request type, priority, and date range
- **Export Functionality**: CSV export for reporting and analysis
- **Comments System**: Allow comments on requests for collaboration
- **Assignment System**: Assign requests to specific team members

### Technical Improvements
- **Unit Tests**: Add Jest or Vitest for code coverage and reliability
- **Performance Optimization**: Implement virtual scrolling for large request lists
- **Accessibility**: Enhanced ARIA labels and keyboard navigation
- **Dark Mode**: Complete dark mode implementation with user preference persistence
- **PWA Support**: Progressive Web App features for offline capability

### UI/UX Enhancements
- **Success Toasts**: Visual feedback after successful operations
- **Request Counter**: Display "Showing X requests" for better context
- **Status Badges**: Colored pills for status on request cards
- **Charts**: Visual charts for request trends and analytics
- **Bulk Actions**: Select multiple requests for bulk status updates

## Code Documentation

### Key Design Patterns

**Module Pattern**: Functions are organized by responsibility (data, UI, events) for maintainability.

**State Management**: Centralized state with localStorage persistence ensures data consistency.

**Event Delegation**: Dynamic event listeners attached after DOM updates for interactive elements.

**Security First**: All user input is escaped before rendering to prevent XSS attacks.

### Performance Considerations

- **Efficient DOM Updates**: Only re-render necessary components when data changes
- **Event Delegation**: Minimize event listeners by attaching to parent containers
- **localStorage Caching**: Data persists across sessions without server calls
- **CDN Resources**: Styles and fonts loaded from CDN for faster initial load

## Contact

For questions about this project, please contact:

- **Name**: Edwin Mwiti
- **Email**: eduedwyn5@gmail.com
- **Phone**: +254 748 750 912
- **LinkedIn**: [linkedin.com/in/edwinmwiti234](https://linkedin.com/in/edwinmwiti234)
- **GitHub**: [github.com/Edwin420s/PhotoMed](https://github.com/Edwin420s/PhotoMed)

## License

This project was created as a software engineering assessment submission for PhotoMed. All rights reserved.

## Acknowledgments

This project was developed as part of the PhotoMed Software Engineering Attachment assessment process. The assessment provided an excellent opportunity to demonstrate frontend development skills, problem-solving abilities, and attention to user experience.

Special thanks to the PhotoMed recruitment team for the clear requirements and supportive assessment process.
