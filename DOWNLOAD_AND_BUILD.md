# 📥 AscendFit - Download & Build Instructions

## 🔗 **DOWNLOAD LINK**

### **Complete Source Code (1.2 MB)**
```
https://files.manuscdn.com/user_upload_by_module/session_file/310519663413896338/sUXVVmDPvpjTDLer.gz
```

**Direct Download**: [Click here to download](https://files.manuscdn.com/user_upload_by_module/session_file/310519663413896338/sUXVVmDPvpjTDLer.gz)

---

## 🛠️ **Quick Build Steps**

### **Step 1: Extract Files**
```bash
# Extract the downloaded file
tar -xzf sUXVVmDPvpjTDLer.gz
cd ascendfit
```

### **Step 2: Install Dependencies**
```bash
npm install
```

### **Step 3: Prebuild Android**
```bash
npx expo prebuild --platform android --clean
```

### **Step 4: Build APK**

**Option A: Debug APK (for testing)**
```bash
cd android
./gradlew assembleDebug
```

**Option B: Release APK (for production)**
```bash
cd android
./gradlew assembleRelease
```

### **Step 5: Find Your APK**

**Debug APK Location:**
```
android/app/build/outputs/apk/debug/app-debug.apk
```

**Release APK Location:**
```
android/app/build/outputs/apk/release/app-release.apk
```

---

## 📋 **Prerequisites**

Before building, make sure you have:

1. **Node.js v18+**
   ```bash
   node --version  # Should be v18 or higher
   ```

2. **Java 17+**
   ```bash
   java -version  # Should show Java 17 or higher
   ```

3. **Android SDK**
   - Download from: https://developer.android.com/studio
   - Or use Android Studio

4. **Environment Variables** (if needed)
   ```bash
   export ANDROID_HOME=$HOME/Android/Sdk
   export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
   ```

---

## 💻 **System Requirements**

- **OS**: Windows, Mac, or Linux
- **Disk Space**: 10 GB minimum
- **RAM**: 4 GB minimum (8 GB recommended)
- **Time**: 30-45 minutes for first build

---

## 📱 **Install on Android Phone**

Once you have the APK:

1. **Transfer APK to phone**
   - USB cable
   - Email
   - Cloud storage
   - Bluetooth

2. **Enable Unknown Sources**
   - Settings → Security → Unknown Sources
   - Toggle ON

3. **Install APK**
   - Open file manager
   - Navigate to Downloads
   - Tap the APK file
   - Tap "Install"

4. **Launch App**
   - Find "AscendFit" in app drawer
   - Tap to open
   - Enjoy!

---

## 🎮 **First Time Setup**

When you open AscendFit:

1. **Signup Screen**
   - Enter your name
   - Select age (16+)
   - Choose gender
   - Enter height (cm) and weight (kg)
   - Select fitness goal

2. **Personalized Plan**
   - App generates your custom workout plan
   - Based on your goal and experience level

3. **Start Training**
   - Complete daily quests
   - Earn XP and rank up
   - Compete in Game Mode
   - Track progress

---

## 🐛 **Troubleshooting**

### Build Fails - "Java not found"
```bash
# Install Java 17
# Windows: Download from oracle.com
# Mac: brew install java17
# Linux: sudo apt-get install openjdk-17-jdk
```

### Build Fails - "Android SDK not found"
```bash
# Download Android Studio from:
# https://developer.android.com/studio
# Or set ANDROID_HOME:
export ANDROID_HOME=$HOME/Android/Sdk
```

### Build Takes Too Long
- First build takes 30-45 minutes
- Subsequent builds are faster (5-10 minutes)
- Ensure you have good internet connection

### APK Won't Install
- Check Android version (minimum API 24)
- Enable "Unknown Sources" in settings
- Try deleting old version first

---

## 📊 **Build Output**

### Debug APK
- **Size**: 80-100 MB
- **Purpose**: Testing and development
- **Installation**: Direct on device
- **Signing**: Automatic debug key

### Release APK
- **Size**: 50-70 MB
- **Purpose**: Production/App Store
- **Installation**: Direct on device
- **Signing**: Requires keystore (see below)

---

## 🔐 **Release Build with Signing**

For production release, create a keystore:

```bash
# Generate keystore
keytool -genkey -v -keystore ascendfit.keystore \
  -keyalg RSA -keysize 2048 -validity 10000 \
  -alias ascendfit

# Build signed release
cd android
./gradlew assembleRelease \
  -Pandroid.injected.signing.store.file=../ascendfit.keystore \
  -Pandroid.injected.signing.store.password=YOUR_PASSWORD \
  -Pandroid.injected.signing.key.alias=ascendfit \
  -Pandroid.injected.signing.key.password=YOUR_PASSWORD
```

---

## 📈 **Next Steps After Installation**

1. **Complete Signup**
   - Personalize your profile
   - Get custom workout plan

2. **Try All Modes**
   - Normal Mode: Daily quests
   - Game Mode: Boss battles
   - Plan Mode: AI trainer

3. **Join a Clan**
   - Create your own
   - Or join existing clan

4. **Track Progress**
   - Log weight weekly
   - Take progress photos
   - Monitor streaks

5. **Compete**
   - Challenge friends
   - Climb leaderboard
   - Participate in clan wars

---

## 🎯 **Tips for Success**

- ✅ Complete daily quests for streak bonuses
- ✅ Focus on form over speed
- ✅ Use Plan Mode for structured training
- ✅ Join a clan for community support
- ✅ Track progress with photos
- ✅ Participate in Game Mode for fun

---

## 📞 **Support**

- **Expo Docs**: https://docs.expo.dev
- **React Native**: https://reactnative.dev
- **Android Docs**: https://developer.android.com

---

## 🎉 **Ready to Build?**

1. Download from link above
2. Extract files
3. Follow build steps
4. Install on phone
5. Start your fitness journey!

**ASCENDA!** 🚀✨

---

**Version**: 1.0.0  
**Last Updated**: March 13, 2024  
**Status**: Ready to Build
