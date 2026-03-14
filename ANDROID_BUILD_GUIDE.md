# 📱 AscendFit Android APK Build Guide

Since the sandbox environment doesn't have Android SDK configured, here are several ways to build and get the APK:

---

## **Option 1: Use EAS Build (Easiest - Recommended)**

EAS (Expo Application Services) handles the build for you in the cloud.

### Prerequisites
- Expo account (free): https://expo.dev
- Node.js and npm installed

### Steps

1. **Install EAS CLI**
   ```bash
   npm install -g eas-cli
   ```

2. **Login to Expo**
   ```bash
   eas login
   ```

3. **Build Android APK**
   ```bash
   cd /home/ubuntu/ascendfit
   eas build --platform android
   ```

4. **Download APK**
   - EAS will provide a download link
   - Or check your Expo dashboard at https://expo.dev

**Time**: ~15-20 minutes  
**Cost**: Free tier available

---

## **Option 2: Build on Your Machine**

### Prerequisites
- Node.js v18+
- Android SDK (API 24+)
- Java 17+
- 10GB free disk space

### Steps

1. **Extract the source code**
   ```bash
   tar -xzf ascendfit-android-source.tar.gz
   cd ascendfit
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Prebuild Android**
   ```bash
   npx expo prebuild --platform android --clean
   ```

4. **Build APK**
   ```bash
   cd android
   ./gradlew assembleDebug
   ```

5. **Find APK**
   ```bash
   # Debug APK (for testing)
   android/app/build/outputs/apk/debug/app-debug.apk
   
   # Release APK (for production)
   ./gradlew assembleRelease
   android/app/build/outputs/apk/release/app-release.apk
   ```

**Time**: ~30-45 minutes (first build)  
**Cost**: Free

---

## **Option 3: Use GitHub Actions (Free CI/CD)**

### Steps

1. **Push code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/ascendfit.git
   git push -u origin main
   ```

2. **Create `.github/workflows/build-android.yml`**
   ```yaml
   name: Build Android APK
   
   on:
     push:
       branches: [main]
   
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - uses: actions/setup-node@v3
           with:
             node-version: '18'
         - run: npm install
         - run: npx expo prebuild --platform android --clean
         - run: cd android && ./gradlew assembleDebug
         - uses: actions/upload-artifact@v3
           with:
             name: app-debug
             path: android/app/build/outputs/apk/debug/app-debug.apk
   ```

3. **Push and wait for build**
   - GitHub Actions will automatically build
   - Download APK from "Artifacts"

**Time**: ~20-30 minutes  
**Cost**: Free (2000 minutes/month)

---

## **Option 4: Use Appetize.io (Web Preview)**

Test the app in browser without building APK:

1. **Upload to Appetize**
   ```bash
   npm install -g appetize-cli
   appetize upload --platform android
   ```

2. **Test in browser**
   - Get a shareable link
   - Test on any device

**Time**: ~5 minutes  
**Cost**: Free tier available

---

## **Option 5: Use Codemagic (Free Tier)**

Cloud CI/CD with free tier:

1. **Sign up**: https://codemagic.io
2. **Connect GitHub repo**
3. **Select "React Native" template**
4. **Build and download APK**

**Time**: ~15-20 minutes  
**Cost**: Free tier available

---

## **Installation Instructions**

Once you have the APK file:

### On Android Phone

1. **Download APK** to your phone
2. **Enable Unknown Sources**
   - Settings → Security → Unknown Sources (Enable)
3. **Install APK**
   - Open file manager
   - Find `app-debug.apk` or `app-release.apk`
   - Tap to install
4. **Launch AscendFit**
   - Find app in app drawer
   - Tap to open

### On Android Emulator

1. **Open Android Emulator**
2. **Drag APK into emulator window**
3. **App installs automatically**
4. **Tap to launch**

---

## **Recommended Approach**

**For Quick Testing**: Use **Option 1 (EAS Build)**
- Easiest
- No local setup needed
- Free tier available
- Takes ~15-20 minutes

**For Production**: Use **Option 2 (Local Build)**
- Full control
- Can optimize for release
- Faster builds after first one
- Requires setup

**For CI/CD**: Use **Option 3 (GitHub Actions)**
- Automated builds
- Free
- Great for teams
- Requires GitHub

---

## **Troubleshooting**

### "Android SDK not found"
```bash
# Set Android SDK path
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```

### "Java version mismatch"
```bash
# Ensure Java 17+
java -version
# Should show: openjdk version "17.0.x" or higher
```

### "Gradle build fails"
```bash
# Clean and rebuild
cd android
./gradlew clean
./gradlew assembleDebug
```

### "Out of memory"
```bash
# Increase heap size
export GRADLE_OPTS="-Xmx4096m -XX:MaxPermSize=1024m"
```

---

## **File Sizes**

- **Debug APK**: ~80-100 MB
- **Release APK**: ~50-70 MB (optimized)

---

## **Next Steps**

1. **Choose a build method** from options above
2. **Build the APK**
3. **Install on your Android device**
4. **Launch AscendFit**
5. **Enjoy your fitness RPG!**

---

## **Support**

- **Expo Docs**: https://docs.expo.dev
- **React Native Docs**: https://reactnative.dev
- **EAS Build Docs**: https://docs.expo.dev/build/introduction/

---

## **Quick Reference**

| Method | Time | Cost | Difficulty |
|--------|------|------|------------|
| EAS Build | 15-20 min | Free | Easy |
| Local Build | 30-45 min | Free | Medium |
| GitHub Actions | 20-30 min | Free | Medium |
| Appetize | 5 min | Free | Easy |
| Codemagic | 15-20 min | Free | Easy |

---

**Status**: Ready to Build  
**Version**: 1.0.0  
**Last Updated**: March 13, 2024

🚀 **Happy Building!**
