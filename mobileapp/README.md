# Mobile App - React Native

This is the React Native mobile application for the surveillance system, built with Expo for cross-platform deployment.

## Features

- User authentication (login, register, forgot password)
- Video streaming from surveillance cameras
- Profile management
- Change password functionality
- Cross-platform (iOS, Android, Web)

## Prerequisites

- Node.js 16 or higher
- Expo CLI
- React Native development environment
- For iOS: Xcode (macOS only)
- For Android: Android Studio and SDK

## Installation

1. Navigate to the mobileapp directory:
   ```bash
   cd mobileapp
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Install Expo CLI globally (if not already installed):
   ```bash
   npm install -g @expo/cli
   ```

## Usage

1. Start the Expo development server:
   ```bash
   npm start
   ```

   Or use Expo CLI:
   ```bash
   npx expo start
   ```

2. Scan the QR code with Expo Go app on your device, or use an emulator/simulator.

## Configuration

- Update API base URL in the app configuration files
- Configure environment variables in `.env` file if needed
- Customize theme in `constants/theme.js`

## Dependencies

- React Native 0.79+
- Expo SDK 53+
- React Navigation for navigation
- Axios for API calls
- React Native Paper for UI components
- React Native Vector Icons for icons
- AsyncStorage for local storage

## Environment Variables

Create a `.env` file in the mobileapp directory with:
```
API_BASE_URL=http://your-django-backend-url:8000
```