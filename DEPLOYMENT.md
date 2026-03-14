# 🚀 AscendFit Deployment Guide

## Prerequisites

- **Node.js**: v18+ (v22.13.0 recommended)
- **npm**: v9+ or **pnpm**
- **Expo CLI**: Latest version
- **Git**: For version control

---

## Local Development Setup

### 1. Clone and Install

```bash
cd /home/ubuntu/ascendfit
npm install
```

### 2. Start Development Server

**Web (Browser)**
```bash
npm run web
# Opens at http://localhost:8081
```

**iOS (Mac only)**
```bash
npm run ios
```

**Android**
```bash
npm run android
```

---

## Project Structure

```
ascendfit/
├── app/                    # Main app screens
│   ├── (tabs)/            # Tab-based navigation
│   │   ├── index.tsx      # Home
│   │   ├── workouts.tsx   # Workouts
│   │   ├── library.tsx    # Exercise Library
│   │   ├── gamemode.tsx   # Game Mode
│   │   ├── planmode.tsx   # Plan Mode
│   │   ├── clans.tsx      # Clans
│   │   ├── progress.tsx   # Progress
│   │   ├── leaderboard.tsx # Leaderboard
│   │   ├── profile.tsx    # Profile
│   │   └── _layout.tsx    # Tab navigation
│   ├── signup.tsx         # Signup screen
│   ├── _layout.tsx        # Root layout
│   └── modal.tsx          # Modal template
├── stores/                # Zustand state management
│   ├── rankStore.ts       # Rank system
│   ├── userStore.ts       # User profile
│   ├── workoutStore.ts    # Workouts
│   ├── gameModeStore.ts   # Game mode
│   ├── advancedRankStore.ts # Advanced ranks
│   ├── clanStore.ts       # Clans
│   ├── progressStore.ts   # Progress
│   ├── leaderboardStore.ts # Leaderboard
│   └── planModeStore.ts   # Plan mode
├── components/            # Reusable components
│   └── FitnessIDCard.tsx  # ID card component
├── constants/             # Constants
├── hooks/                 # Custom hooks
├── assets/                # Images and media
├── package.json           # Dependencies
├── app.json               # Expo config
├── tsconfig.json          # TypeScript config
├── ASCENDFIT_README.md    # Main documentation
├── QUICK_START.md         # Quick start guide
├── FEATURES.md            # Feature list
└── DEPLOYMENT.md          # This file
```

---

## Dependencies

### Core Framework
- **expo**: ~54.0.33 - React Native framework
- **expo-router**: ~6.0.23 - Navigation
- **react-native**: Included with Expo
- **react**: ^18.2.0 - UI library

### Navigation
- **@react-navigation/native**: ^7.1.33
- **@react-navigation/bottom-tabs**: ^7.15.5
- **@react-navigation/stack**: ^7.8.4
- **react-native-screens**: ^4.0.1
- **react-native-safe-area-context**: ^4.12.0

### State Management
- **zustand**: ^4.5.5 - State management

### Animations
- **react-native-reanimated**: ^3.15.0
- **lottie-react-native**: ^6.7.2

### Camera & Media
- **expo-camera**: ^55.0.9
- **expo-av**: ^16.0.8
- **expo-permissions**: ^14.4.0

### UI & Styling
- **react-native-svg**: ^15.15.3
- **@expo/vector-icons**: ^15.0.3

### Utilities
- **axios**: ^1.13.6 - HTTP client
- **expo-constants**: ~18.0.13
- **expo-font**: ~14.0.11
- **expo-haptics**: ~15.0.8
- **expo-image**: ~3.0.11
- **expo-linking**: ~8.0.11

---

## Build Configuration

### app.json

```json
{
  "expo": {
    "name": "ascendfit",
    "slug": "ascendfit",
    "version": "1.0.0",
    "orientation": "portrait",
    "icon": "./assets/images/icon.png",
    "scheme": "ascendfit",
    "userInterfaceStyle": "automatic",
    "newArchEnabled": true,
    "plugins": [
      "expo-router",
      ["expo-splash-screen", {...}]
    ]
  }
}
```

### TypeScript Configuration

```json
{
  "compilerOptions": {
    "target": "ES2020",
    "useDefineForClassFields": true,
    "lib": ["ES2020", "DOM", "DOM.Iterable"],
    "module": "ESNext",
    "skipLibCheck": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "strict": true,
    "resolveJsonModule": true,
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "declaration": true,
    "declarationMap": true,
    "sourceMap": true,
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  }
}
```

---

## Environment Setup

### Development Environment

```bash
# Install Node.js (if not already installed)
# Using nvm (recommended)
nvm install 22.13.0
nvm use 22.13.0

# Install npm dependencies
npm install

# Verify installation
npm --version
node --version
```

### Expo Setup

```bash
# Install Expo CLI globally
npm install -g expo-cli

# Verify Expo installation
expo --version

# Login to Expo (optional, for publishing)
expo login
```

---

## Development Workflow

### 1. Start Development Server

```bash
npm run web
```

The app will be available at `http://localhost:8081`

### 2. Make Changes

Edit files in the `app/`, `stores/`, or `components/` directories. Changes will hot-reload automatically.

### 3. Test on Device

**iOS Simulator**
```bash
npm run ios
```

**Android Emulator**
```bash
npm run android
```

**Physical Device**
- Download Expo Go app
- Scan QR code from terminal
- App opens on device

### 4. Debug

**Browser DevTools**
- Press `w` in terminal to open web debugger
- Use Chrome DevTools for debugging

**React Native Debugger**
```bash
# Install React Native Debugger
npm install -g react-native-debugger

# Start debugger
react-native-debugger
```

---

## Building for Production

### Web Build

```bash
# Build for web
expo export --platform web

# Output in dist/ directory
# Deploy to hosting service (Vercel, Netlify, etc.)
```

### iOS Build

```bash
# Build for iOS
eas build --platform ios

# Requires Apple Developer account
# Output: .ipa file for TestFlight or App Store
```

### Android Build

```bash
# Build for Android
eas build --platform android

# Output: .apk or .aab file for Google Play Store
```

### Using EAS (Expo Application Services)

```bash
# Install EAS CLI
npm install -g eas-cli

# Configure project
eas build:configure

# Build for all platforms
eas build --platform all

# Submit to stores
eas submit --platform ios
eas submit --platform android
```

---

## Deployment Checklist

### Pre-Deployment

- [ ] All tests passing
- [ ] No console errors
- [ ] Performance optimized
- [ ] All features working
- [ ] Documentation updated
- [ ] Version number bumped
- [ ] Changelog updated
- [ ] Assets optimized
- [ ] Secrets configured
- [ ] Analytics enabled

### Deployment Steps

1. **Update Version**
   ```json
   {
     "version": "1.0.1"
   }
   ```

2. **Build**
   ```bash
   eas build --platform all
   ```

3. **Test Build**
   - Test on iOS TestFlight
   - Test on Android beta
   - Verify all features

4. **Submit**
   ```bash
   eas submit --platform ios
   eas submit --platform android
   ```

5. **Monitor**
   - Check crash reports
   - Monitor user feedback
   - Track analytics

---

## Hosting Options

### Web Hosting

**Vercel** (Recommended)
```bash
npm install -g vercel
vercel
```

**Netlify**
```bash
npm install -g netlify-cli
netlify deploy
```

**Firebase Hosting**
```bash
npm install -g firebase-tools
firebase deploy
```

### App Store Distribution

**iOS App Store**
- Use Xcode or EAS
- Requires Apple Developer account ($99/year)
- Review process: 24-48 hours

**Google Play Store**
- Use Android Studio or EAS
- Requires Google Play Developer account ($25 one-time)
- Review process: 2-3 hours

---

## Performance Optimization

### Code Splitting

```typescript
// Dynamic imports for code splitting
const GameMode = lazy(() => import('./gamemode'));
const PlanMode = lazy(() => import('./planmode'));
```

### Image Optimization

```typescript
// Use Expo Image for optimization
import { Image } from 'expo-image';

<Image
  source={require('./image.png')}
  style={{ width: 200, height: 200 }}
  contentFit="cover"
  transition={1000}
/>
```

### Bundle Size

```bash
# Analyze bundle size
expo export --platform web
npm install -g source-map-explorer
source-map-explorer 'dist/**/*.js'
```

---

## Monitoring & Analytics

### Crash Reporting

```typescript
// Example: Sentry integration
import * as Sentry from 'sentry-expo';

Sentry.init({
  dsn: 'YOUR_DSN',
  enableInExpoDevelopment: true,
  tracesSampleRate: 1.0,
});
```

### Analytics

```typescript
// Example: Firebase Analytics
import { Analytics } from '@react-native-firebase/analytics';

await Analytics().logEvent('workout_completed', {
  rank: 'A',
  xp_earned: 20,
});
```

---

## Troubleshooting

### Port Already in Use

```bash
# Use different port
npm run web -- --port 8082

# Or kill process using port 8081
lsof -ti:8081 | xargs kill -9
```

### Build Errors

```bash
# Clear cache
rm -rf .expo
rm -rf node_modules
npm install

# Reset project
npm run reset-project
```

### Dependency Issues

```bash
# Update dependencies
npm update

# Check for conflicts
npm audit

# Fix vulnerabilities
npm audit fix
```

### Metro Bundler Issues

```bash
# Clear Metro cache
expo start --clear

# Or manually
rm -rf .expo
expo start
```

---

## Maintenance

### Regular Updates

```bash
# Check for updates
npm outdated

# Update dependencies
npm update

# Update major versions
npm install expo@latest
```

### Security

```bash
# Check for vulnerabilities
npm audit

# Fix vulnerabilities
npm audit fix --force
```

### Backups

```bash
# Backup project
git commit -am "Backup before update"
git push origin main
```

---

## Support & Resources

- **Expo Documentation**: https://docs.expo.dev
- **React Native Docs**: https://reactnative.dev
- **Zustand Docs**: https://github.com/pmndrs/zustand
- **TypeScript Docs**: https://www.typescriptlang.org

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0.0 | 2024-03-12 | Initial release |

---

## License

AscendFit © 2024. All rights reserved.

---

## Contact

For deployment issues or questions, contact the development team.

**Status**: Production Ready  
**Last Updated**: March 12, 2024
