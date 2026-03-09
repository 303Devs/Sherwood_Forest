# Sherwood Forest

A React Native mobile banking and fintech application built by [303Devs](https://github.com/303Devs). Sherwood Forest delivers a modern financial app experience — covering account management, crypto portfolio tracking, investments, and money transfers — built entirely with Expo and React Native.

---

## Tech Stack

![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=flat-square&logo=clerk&logoColor=white)

| Category | Technology |
|---|---|
| Framework | Expo (latest) |
| Language | TypeScript |
| Navigation | Expo Router (file-based) |
| Authentication | Clerk (OTP + social auth) |
| Data Fetching | TanStack Query |
| State Management | Zustand |
| Local Storage | React Native MMKV |
| Animations | React Native Reanimated, React Native Gesture Handler |
| Charts | Victory Native |
| Graphics | @shopify/react-native-skia |
| Native Menus | Zeego |
| Media | expo-av |
| Haptics | expo-haptics |
| Blur Effects | expo-blur |
| Secure Storage | expo-secure-store |

---

## Features

- **Authentication** — Clerk-powered login, signup, and OTP phone verification flows
- **Home Dashboard** — Account overview and summary
- **Crypto Portfolio** — Browse cryptocurrency holdings and individual crypto detail screens
- **Investments** — Investment overview and management
- **Lifestyle / Spending** — Spending categories and lifestyle finance overview
- **Money Transfers** — In-app fund transfer flow
- **Modal Screens** — Native modal overlays for contextual actions
- **Native Menus** — Platform-native context menus via Zeego
- **Haptic Feedback** — Tactile responses on interactions using expo-haptics
- **Smooth Animations** — React Native Reanimated and Gesture Handler for fluid UI
- **Skia Graphics** — Custom visual rendering with Shopify's React Native Skia
- **Secure Storage** — Sensitive data stored with expo-secure-store and MMKV

---

## App Structure

```
sherwood-forest/
├── app/
│   ├── _layout.tsx                # Root layout
│   ├── index.tsx                  # Entry screen
│   ├── Login.tsx                  # Login screen
│   ├── Signup.tsx                 # Signup screen
│   ├── Help.tsx                   # Help / support screen
│   ├── verify/                    # OTP verification flow
│   └── (authenticated)/
│       ├── _layout.tsx
│       ├── (tabs)/
│       │   ├── home.tsx           # Home dashboard
│       │   ├── crypto.tsx         # Crypto portfolio
│       │   ├── invest.tsx         # Investments
│       │   ├── lifestyle.tsx      # Lifestyle / spending
│       │   └── transfers.tsx      # Money transfers
│       ├── (modals)/              # Modal screens
│       └── crypto/                # Crypto detail screens
├── components/                    # Shared UI components
├── constants/                     # App-wide constants
├── context/                       # React context providers
├── store/                         # Zustand state stores
├── interfaces/                    # TypeScript interfaces
├── assets/                        # Images, fonts, icons
├── cache.ts                       # MMKV cache configuration
└── app.json                       # Expo configuration
```

---

## Getting Started

### Prerequisites

- Node.js 18+
- Expo CLI: `npm install -g expo`
- A [Clerk](https://clerk.com) account and application
- iOS Simulator (macOS) or Android emulator, or the Expo Go app on a physical device

### Installation

```bash
git clone https://github.com/303Devs/Sherwood_Forest.git
cd Sherwood_Forest
npm install
```

### Environment Variables

Create a `.env` file at the project root with your Clerk credentials:

```bash
EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
```

Additional API keys may be required depending on the data sources used for crypto and investment screens.

### Running the App

```bash
npx expo start
```

Then press `i` for iOS simulator, `a` for Android emulator, or scan the QR code with the Expo Go app.

### Build

```bash
# EAS build (recommended for production)
npx eas build --platform ios
npx eas build --platform android
```

---

## Screenshots

<!-- Add screenshots here -->

---

## Status

Portfolio project — actively developed by 303Devs. Not currently published to the App Store or Google Play.

---

Built by [303Devs](https://github.com/303Devs)
