# Carvey

Carvey is an independent mobile app for tracking and managing your vehicles. It runs fully on-device — no account required, no cloud sync, no subscription.

## What it does

- Manage multiple vehicles with photos and details
- Log fuel fill-ups, maintenance, repairs, purchases, and MOT/inspection tests
- Set reminders for upcoming services and renewals
- Organise workshops and service categories
- Export and back up your data locally

## Platform

Built with [Expo](https://expo.dev) (v56) and React Native, targeting:

- **iOS** — iPhone and iPad
- **Android** — phones and tablets
- **Web** — static export via Metro bundler

## Tech stack

| Layer | Library |
|---|---|
| Framework | Expo ~56 / React Native 0.85 |
| Navigation | Expo Router ~56 (file-based) |
| Styling | NativeWind 4 + Tailwind CSS 3 |
| Local database | expo-sqlite |
| Biometric auth | expo-local-authentication |
| Secure storage | expo-secure-store |
| Animations | react-native-reanimated 4 |
| Icons | lucide-react-native |

## Getting started

```bash
npm install
npm start          # Expo dev server
npm run android    # open on Android
npm run ios        # open on iOS (macOS required)
npm run web        # open in browser
```

Requires Node 18+ and the [Expo CLI](https://docs.expo.dev/get-started/installation/).

## Building

Builds are managed with EAS Build. Profiles defined in [eas.json](eas.json):

- `development` — internal APK with dev client
- `preview` — internal APK for testing
- `production` — Android App Bundle / iOS archive

```bash
eas build --profile preview --platform android
```

## Data & privacy

All data is stored locally on your device using SQLite. Nothing is sent to any server. Backups are exported as local files that you control.
