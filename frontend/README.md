# Frontend - Electron Desktop App

This is the Electron.js desktop application for the surveillance system, providing an admin dashboard and monitoring interface.

## Features

- Admin dashboard for system management
- User authentication interface
- Camera monitoring and control
- Real-time video streaming
- Cross-platform desktop application (Windows, macOS, Linux)

## Prerequisites

- Node.js 16 or higher
- npm (Node package manager)

## Installation

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Usage

1. Start the Electron application:
   ```bash
   npm start
   ```

   This will launch the desktop application.

2. The app will connect to the Django backend API (ensure the backend is running).

## Project Structure

- `main.js` - Electron main process
- `admin_dashboard.html/js` - Admin dashboard interface
- `dashboard.html/js` - User dashboard
- `login.html/js` - Authentication interface
- `forgot_password.html/js` - Password recovery
- `styles.css` - Application styling

## Configuration

- Update API endpoints in the JavaScript files to match your Django backend URL
- Customize styling in `styles.css` as needed

## Building for Production

To build the application for distribution:

1. Install electron-builder:
   ```bash
   npm install -g electron-builder
   ```

2. Build the app:
   ```bash
   electron-builder
   ```

This will create distributable packages for your platform.

## Dependencies

- Electron 33+
- @electron/remote for IPC communication

## Troubleshooting

- Ensure the Django backend is running and accessible
- Check network connectivity for API calls
- Verify Node.js version compatibility