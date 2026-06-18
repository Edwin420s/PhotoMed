# PhotoMed Request Tracker

A professional request tracking web application for managing clinical software integration requests across the PhotoMed ecosystem. Built as a software engineering assessment submission.

## Project Overview

The Request Tracker is a full-functional web application that allows users to submit, manage, and track requests including bugs, feature requests, feedback, and partnership inquiries. The application features a professional dashboard interface with real-time statistics, search/filtering capabilities, and persistent data storage.

## Features Implemented

### Core Requirements
- **Request Submission Form**: Collects name, email, product, request type, priority, and message
- **Request List**: Dynamically renders all submitted requests with full details
- **Status Management**: Supports New, In Review, Resolved, and Rejected statuses with dropdown controls
- **Filtering**: Status-based filtering (All, New, In Review, Resolved, Rejected)
- **Data Persistence**: Uses localStorage to save requests across browser sessions
- **Responsive Design**: Mobile-first approach using Tailwind CSS

### Bonus Features
- **Search Functionality**: Search requests by name or email
- **Statistics Dashboard**: Real-time counts for Total, New, In Review, and Resolved requests
- **Edit Requests**: Modal-based editing with pre-filled data
- **Delete Requests**: With confirmation dialog
- **Empty State Handling**: User-friendly message when no requests match filters
- **Form Validation**: Inline error messages for required fields
- **Professional UI**: Clean, modern dashboard interface with Material Design icons

## Technology Stack

- **HTML5**: Semantic markup
- **Tailwind CSS**: Utility-first CSS framework (via CDN with forms and container-queries plugins)
- **Vanilla JavaScript**: No frameworks, pure JavaScript for all functionality
- **localStorage API**: Client-side data persistence
- **Google Fonts**: Inter font family for typography
- **Material Symbols**: Google's icon library for UI icons

## How to Run Locally

### Option 1: Direct File Opening
1. Clone or download this repository
2. Open `index.html` in any modern web browser
3. The application will work immediately with no build process required

### Option 2: Local Server (Recommended)
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## Project Structure

```
PhotoMed/
├── index.html          # Single-file application with embedded CSS and JavaScript
└── README.md          # This file
```

The application is intentionally structured as a single HTML file for simplicity and ease of deployment, as permitted by the assessment requirements.

## What Was Completed

All mandatory requirements have been implemented:
- Request submission form with all required fields
- Dynamic request list displaying all submitted details
- Status management with all four required statuses
- Working status filter
- Data persistence using localStorage
- Responsive, professional UI

Additionally implemented bonus features:
- Search functionality
- Statistics dashboard
- Edit and delete capabilities
- Improved validation UX with inline error messages
- Professional dashboard design

## What Was Not Completed

No features were left incomplete. All core requirements and several optional improvements have been implemented.

## Challenges Faced

1. **Initial Design Complexity**: Started with a complex UI that needed simplification while maintaining professional appearance. Resolved by focusing on core dashboard functionality and clean card-based layout.

2. **State Management**: Ensuring localStorage synchronization across all UI components (stats, list, filters). Resolved by implementing a centralized `fullRefreshUI()` function that updates all components when data changes.

3. **Form Validation UX**: Initially used browser `alert()` which felt unprofessional. Replaced with inline error messages that appear dynamically above the form.

## Future Improvements

If given more time, I would enhance the application with:

1. **Backend Integration**: Replace localStorage with a proper database (PostgreSQL, MongoDB, or Supabase) for multi-user support
2. **Authentication**: Add user login and role-based access control
3. **Email Notifications**: Send email alerts when request status changes
4. **File Attachments**: Allow users to attach screenshots or documents to requests
5. **Advanced Filtering**: Add filters by request type, priority, and date range
6. **Export Functionality**: CSV export for reporting
7. **Unit Tests**: Add Jest or Vitest for code coverage
8. **Performance Optimization**: Implement virtual scrolling for large request lists
9. **Accessibility**: Enhanced ARIA labels and keyboard navigation
10. **Dark Mode**: Complete dark mode implementation (currently supported but not fully styled)

## Deployment

The application is deployed on Netlify: [Live URL]

To deploy your own version:

### Netlify Deployment
1. Push your code to GitHub
2. Log in to [Netlify](https://netlify.com)
3. Click "Add new site" → "Import an existing project"
4. Connect your GitHub repository
5. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `.` (root)
   - Click "Deploy site"

### Alternative Deployment Options
- **Vercel**: Similar process to Netlify
- **GitHub Pages**: Enable GitHub Pages in repository settings
- **Cloudflare Pages**: Connect GitHub repository and deploy

## Code Quality

The code follows these principles:
- **Clean Code**: Clear function names, minimal comments where code is self-documenting
- **Separation of Concerns**: Data model, UI rendering, and event handling are separated
- **Security**: HTML escaping to prevent XSS attacks
- **Performance**: Efficient DOM updates with targeted re-rendering
- **Maintainability**: Modular functions that can be easily tested or modified

## Assessment Compliance

This project meets all assessment requirements:
- Functional web application with working form and request list
- Status management with all required statuses
- At least one working filter (status filter implemented)
- Data persistence using localStorage
- Clean, readable, and organized code
- Professional UI/UX design
- Responsive design for mobile devices
- Comprehensive documentation

## Contact

For questions about this project, please contact:
- **Name**: Edwin Mwiti
- **Email**: eduedwyn5@gmail.com
- **GitHub**: [Your GitHub Profile]

## License

This project was created as a software engineering assessment submission for PhotoMed. All rights reserved.
