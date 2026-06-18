# PhotoMed Request Tracker

A professional request tracking web application for managing clinical software integration requests. Features a modern dashboard interface with real-time statistics, search/filtering capabilities, and persistent data storage.

## Live Demo

[https://photomed.netlify.app/](https://photomed.netlify.app/)

## Features

- **Request Submission**: Submit bugs, feature requests, feedback, and partnership inquiries
- **Status Management**: Track requests through New, In Review, Resolved, and Rejected statuses
- **Search & Filter**: Search by name/email and filter by status
- **Statistics Dashboard**: Real-time overview of request metrics
- **Edit & Delete**: Full CRUD operations with confirmation dialogs
- **Data Persistence**: Automatic save to browser localStorage
- **Responsive Design**: Mobile-friendly interface

## Technology Stack

- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript
- localStorage API
- Google Fonts (Inter)
- Material Symbols

## Getting Started

### Local Development

1. Clone the repository:
```bash
git clone <repository-url>
cd PhotoMed
```

2. Open `index.html` in your browser, or use a local server:
```bash
# Python
python -m http.server 8000

# Node.js
npx http-server
```

3. Navigate to `http://localhost:8000`

## Project Structure

```
PhotoMed/
├── index.html       # Single-file application
├── netlify.toml     # Netlify deployment config
└── README.md        # Documentation
```

## Usage

1. **Submit a Request**: Fill out the form on the left sidebar with name, email, product, type, priority, and message
2. **View Requests**: All requests appear in the main list sorted by date
3. **Update Status**: Use the dropdown on each request card to change status
4. **Search**: Use the search bar to find requests by name or email
5. **Filter**: Use the status filter to show specific request types
6. **Edit/Delete**: Click the edit or delete icons on each request card

## Deployment

The application is deployed on Netlify. To deploy your own version:

1. Push code to GitHub
2. Connect repository to Netlify
3. Deploy with default settings (no build command needed)

## License

All rights reserved.
